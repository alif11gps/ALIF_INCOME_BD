<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <title>ALIF_INCOME_BD - অফিসিয়াল আর্নিং প্ল্যাটফর্ম</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { font-family: 'Hind Siliguri', sans-serif; background-color: #0f172a; color: #1e293b; user-select: none; display: flex; justify-content: center; align-items: center; min-height: 100vh; margin: 0; }
        .app-container { width: 100%; max-width: 420px; height: 100vh; background-color: #f8fafc; display: flex; flex-direction: column; position: relative; overflow: hidden; box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5); }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body>

<div class="app-container">
    <header class="bg-white border-b border-slate-200 px-4 py-3 flex items-center justify-between shadow-sm">
        <div class="flex items-center gap-2">
            <div class="w-8 h-8 bg-indigo-600 rounded-full flex items-center justify-center text-white font-bold">ALIF</div>
            <span class="text-sm font-black text-slate-800">ALIF_INCOME_BD</span>
        </div>
        <div class="bg-indigo-50 px-3 py-1 rounded-full text-indigo-700 font-bold text-sm">
            ৳ <span id="nav-balance">0.00</span>
        </div>
    </header>

    <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 space-y-4">
        <section id="home" class="tab-content active space-y-4">
            <div class="bg-gradient-to-r from-indigo-600 to-blue-600 p-6 rounded-3xl text-white shadow-lg">
                <p class="text-indigo-100 text-xs">বর্তমান ব্যালেন্স</p>
                <h2 class="text-4xl font-black">৳<span id="home-balance">0.00</span></h2>
            </div>
            <div class="grid grid-cols-2 gap-3">
                <div class="bg-white p-4 rounded-2xl border shadow-sm">
                    <p class="text-[10px] text-slate-400">মোট ভিডিও</p>
                    <p class="text-lg font-bold" id="total-video-count">0 / 200</p>
                </div>
                <div class="bg-white p-4 rounded-2xl border shadow-sm">
                    <p class="text-[10px] text-slate-400">সফল রেফার</p>
                    <p class="text-lg font-bold" id="home-refer-count">0 / 20</p>
                </div>
            </div>
        </section>

        <section id="tasks" class="tab-content space-y-4">
            <div class="bg-white p-5 rounded-2xl border text-center shadow-sm">
                <h3 class="font-bold text-slate-800 mb-2">ভিডিও টাস্ক (প্রতিটি ৳১০)</h3>
                <p class="text-xs text-slate-500 mb-4">আজকের ১০টি ভিডিও শেষ করুন।</p>
                <div class="w-full bg-slate-100 h-3 rounded-full mb-4">
                    <div id="task-progress-bar" class="bg-indigo-600 h-full w-[0%] rounded-full transition-all"></div>
                </div>
                <button onclick="watchVideoAd()" class="w-full bg-rose-500 text-white font-bold py-3 rounded-xl">বিজ্ঞাপন দেখুন</button>
            </div>
        </section>

        <section id="wallet" class="tab-content space-y-4">
            <div class="bg-amber-50 border border-amber-200 p-4 rounded-2xl">
                <h4 class="text-xs font-bold text-amber-800 mb-2">⚠️ উত্তোলনের শর্তাবলী:</h4>
                <ul class="text-[11px] text-slate-600 list-disc pl-4 space-y-1">
                    <li>সর্বনিম্ন উত্তোলন: ৳১৫০০</li>
                    <li>শর্ত ১: ২০০টি ভিডিও দেখা</li>
                    <li>শর্ত ২: ২০টি রেফার সম্পন্ন করা</li>
                </ul>
            </div>
            <select id="withdraw-method" class="w-full bg-slate-100 p-3 rounded-xl font-bold">
                <option value="বিকাশ">বিকাশ (Bkash)</option>
                <option value="নগদ">নগদ (Nagad)</option>
            </select>
            <input id="withdraw-number" type="text" placeholder="আপনার নম্বর" class="w-full bg-slate-100 p-3 rounded-xl">
            <input id="withdraw-amount" type="number" placeholder="৳১৫০০ বা তার বেশি" class="w-full bg-slate-100 p-3 rounded-xl">
            <button onclick="processWithdraw()" class="w-full bg-indigo-600 text-white font-bold py-3 rounded-xl">উত্তোলন করুন</button>
        </section>
    </main>

    <nav class="bg-white border-t p-3 flex justify-around">
        <button onclick="switchTab('home')" class="text-indigo-600 font-bold text-xs">🏠 হোম</button>
        <button onclick="switchTab('tasks')" class="text-slate-400 font-bold text-xs">📋 কাজ</button>
        <button onclick="switchTab('wallet')" class="text-slate-400 font-bold text-xs">💳 ওয়ালেট</button>
    </nav>
</div>

<script>
    let currentBalance = 0.00, todayVideosWatched = 0, totalVideosWatched = 0, totalRefers = 0;

    function updateAppUI() {
        document.getElementById('nav-balance').innerText = currentBalance.toFixed(2);
        document.getElementById('home-balance').innerText = currentBalance.toFixed(2);
        document.getElementById('total-video-count').innerText = totalVideosWatched + " / 200";
        document.getElementById('home-refer-count').innerText = totalRefers + " / 20";
        document.getElementById('task-progress-bar').style.width = (todayVideosWatched / 10) * 100 + "%";
    }

    function switchTab(tabId) {
        document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
        document.getElementById(tabId).classList.add('active');
    }

    function watchVideoAd() {
        if (todayVideosWatched >= 10) { alert("আজকের লিমিট শেষ!"); return; }
        alert("ভিডিও চলছে...");
        setTimeout(() => {
            todayVideosWatched++; totalVideosWatched++; currentBalance += 10;
            updateAppUI(); alert("৳১০ যোগ হয়েছে!");
        }, 1000);
    }

    function processWithdraw() {
        const amount = parseFloat(document.getElementById('withdraw-amount').value);
        if (amount < 1500 || currentBalance < amount) { alert("শর্ত মানুন অথবা পর্যাপ্ত ব্যালেন্স নেই।"); return; }
        if (totalVideosWatched >= 200 && totalRefers >= 20) {
            alert("সফল! আপনার রিকোয়েস্টটি পেন্ডিং এ আছে।");
        } else {
            alert("শর্ত পূরণ হয়নি! ২০০ ভিডিও এবং ২০ রেফার বাধ্যতামূলক।");
        }
    }
</script>
</body>
</html>
