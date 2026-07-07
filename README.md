<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ALIF_INCOME_BD - অফিসিয়াল আর্নিং প্ল্যাটফর্ম</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #0f172a;
            color: #1e293b;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }
        .app-container {
            width: 100%;
            max-width: 420px;
            height: 100vh;
            max-height: 850px;
            background-color: #f8fafc;
            display: flex;
            flex-direction: column;
            position: relative;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
            border-radius: 0px;
        }
        @media (min-width: 450px) {
            .app-container {
                border-radius: 30px;
                border: 8px solid #334155;
                height: 90vh;
            }
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body>

    <div class="app-container">

        <!-- ================= APP HEADER ================= -->
        <header class="bg-white border-b border-slate-200 px-4 py-3 flex items-center justify-between sticky top-0 z-50 shadow-sm shrink-0">
            <div class="flex items-center gap-2">
                <div class="w-7 h-7 bg-indigo-600 rounded-lg flex items-center justify-center text-white text-sm font-bold">💼</div>
                <span class="text-base font-black text-slate-800 tracking-wider">ALIF_INCOME_BD</span>
            </div>
            
            <div class="flex items-center gap-2">
                <div class="bg-indigo-50 px-3 py-1 rounded-full border border-indigo-100 flex items-center gap-1.5">
                    <span class="text-indigo-600 text-xs font-bold">৳</span>
                    <span id="nav-balance" class="font-bold text-indigo-700 text-sm">0.00</span>
                </div>
                <div class="w-8 h-8 rounded-full bg-slate-200 flex items-center justify-center font-bold text-slate-700 text-xs border border-slate-300">
                    MD
                </div>
            </div>
        </header>

        <!-- ================= MAIN CONTENT AREA ================= -->
        <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 pb-24 space-y-4">
            
            <!-- --- TAB 1: হোম ড্যাশবোর্ড --- -->
            <section id="home" class="tab-content active space-y-4">
                <div class="bg-white p-4 rounded-3xl border border-slate-100 shadow-sm flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-full border-2 border-indigo-500 p-0.5">
                            <div class="w-full h-full rounded-full bg-indigo-100 flex items-center justify-center text-lg">👤</div>
                        </div>
                        <div>
                            <div class="flex items-center gap-1">
                                <h3 class="font-bold text-slate-800 text-sm">MD</h3>
                                <span class="text-blue-500 text-xs">✓</span>
                            </div>
                            <p class="text-[11px] text-slate-400">মেম্বার প্রোফাইল</p>
                        </div>
                    </div>
                    <button class="bg-slate-100 text-slate-700 text-xs font-bold px-3 py-1.5 rounded-xl">
                        Log Out
                    </button>
                </div>

                <div class="bg-gradient-to-br from-indigo-700 via-indigo-800 to-slate-900 p-6 rounded-3xl text-white shadow-md relative overflow-hidden">
                    <p class="text-indigo-200 text-xs font-semibold tracking-wide">বর্তমান ব্যালেন্স</p>
                    <h2 class="text-4xl font-black mt-2 flex items-baseline gap-1">
                        <span class="text-2xl font-bold">৳</span><span id="home-balance">0.00</span>
                    </h2>
                    <div class="absolute right-4 bottom-4 opacity-10 text-6xl">💸</div>
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-white p-3.5 rounded-2xl border border-slate-100 shadow-sm flex items-center gap-3">
                        <div class="w-10 h-10 bg-indigo-50 text-indigo-600 rounded-xl flex items-center justify-center text-lg font-bold">⚡</div>
                        <div>
                            <span class="text-[11px] text-slate-400 block font-semibold">মোট ভিডিও টাস্ক</span>
                            <span id="total-video-count" class="text-base font-bold text-slate-800">0 / 200</span>
                        </div>
                    </div>
                    <div class="bg-white p-3.5 rounded-2xl border border-slate-100 shadow-sm flex items-center gap-3">
                        <div class="w-10 h-10 bg-emerald-50 text-emerald-600 rounded-xl flex items-center justify-center text-lg font-bold">👥</div>
                        <div>
                            <span class="text-[11px] text-slate-400 block font-semibold">সফল রেফার</span>
                            <span id="home-refer-count" class="text-base font-bold text-slate-800">0 / 20</span>
                        </div>
                    </div>
                </div>

                <button onclick="switchTab('tasks')" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3.5 rounded-2xl shadow-sm transition">
                    টাস্ক ওয়ার্ক শুরু করুন
                </button>
            </section>

            <!-- --- TAB 2: ভিডিও কাজ (Tasks) --- -->
            <section id="tasks" class="tab-content space-y-4">
                <div class="bg-white border border-slate-100 p-4 rounded-2xl shadow-sm text-center space-y-3">
                    <h3 class="text-base font-bold text-slate-800">📹 বিজ্ঞাপন দেখে আয়</h3>
                    <p class="text-xs text-slate-500">প্রতিটি ভিডিওর জন্য আপনি পাবেন নিশ্চিত <span class="text-emerald-600 font-bold">৳১০.০০ ইনকাম</span>। প্রতিদিন ১৫টি করে টাস্ক পাবেন।</p>
                    
                    <div class="bg-indigo-50 text-indigo-700 font-semibold text-xs py-2 px-4 rounded-xl inline-block">
                        🎁 রিওয়ার্ড: ৳১০.০০ টাকা
                    </div>

                    <div class="space-y-1.5 pt-2">
                        <div class="flex justify-between text-[11px] font-bold text-slate-500">
                            <span>আজকের ভিডিও সম্পন্ন</span>
                            <span id="today-task-count">0 / 15</span>
                        </div>
                        <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden">
                            <div id="task-progress-bar" class="bg-indigo-600 h-full w-[0%] transition-all duration-300"></div>
                        </div>
                    </div>

                    <button onclick="watchVideoAd()" class="w-full bg-rose-500 hover:bg-rose-600 text-white font-bold py-3 rounded-xl shadow-sm transition mt-2">
                        বিজ্ঞাপন দেখুন
                    </button>
                </div>
            </section>

            <!-- --- TAB 3: রেফার (Invite) --- -->
            <section id="invite" class="tab-content space-y-4">
                <div class="bg-slate-900 text-white p-5 rounded-3xl space-y-4 shadow-lg">
                    <div class="space-y-1.5">
                        <h3 class="text-lg font-bold text-white">বন্ধুকে রেফার করুন</h3>
                        <p class="text-xs text-slate-400 leading-relaxed">আপনার রেফার লিংক শেয়ার করুন। বন্ধু সাইন আপ করলেই আপনার অ্যাকাউন্টে <span class="text-amber-400 font-bold">৳৫০.০০ TAKA</span> বোনাস যোগ হবে।</p>
                    </div>
                    
                    <div class="bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-xs py-2 px-4 rounded-xl inline-block font-bold">
                        😊 প্রতি রেফারে ৳৫০.০০ TAKA বোনাস
                    </div>

                    <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 flex justify-between items-center gap-2">
                        <span class="text-xs font-mono text-slate-300 overflow-hidden truncate">https://t.me/AlifIncomeBdBot?start=ref</span>
                        <button onclick="addDemoRefer()" class="p-2 bg-fuchsia-600 text-white rounded-lg text-xs font-bold shrink-0">📋</button>
                    </div>
                </div>
                <p class="text-center text-[10px] text-slate-400">💡 (টেস্ট করার জন্য উপরের বেগুনী 📋 বাটনে চাপলে ১টি করে রেফার যোগ হবে)</p>
            </section>

            <!-- --- TAB 4: ওয়ালেট ও উইথড্র (Wallet) --- -->
            <section id="wallet" class="tab-content space-y-4">
                <button onclick="openWithdrawModal()" class="w-full bg-gradient-to-r from-indigo-500 to-purple-600 text-white font-bold py-3.5 rounded-2xl shadow flex items-center justify-center gap-2 text-sm">
                    <span>💰</span> উত্তোলন করুন
                </button>

                <!-- উত্তোলনের নতুন শর্তাবলী কার্ড -->
                <div class="bg-amber-50 border border-amber-200 p-4 rounded-2xl space-y-3">
                    <h4 class="text-xs font-bold text-amber-800 flex items-center gap-1">⚠️ উত্তোলনের শর্তাবলী (ALIF_INCOME_BD)</h4>
                    <p class="text-[11px] text-amber-700 leading-relaxed">টাকা উইথড্র করার জন্য নিচে দেওয়া যেকোনো **একটি শর্ত** অবশ্যই পূরণ করতে হবে:</p>
                    
                    <ul class="text-[11px] text-slate-600 space-y-1.5 list-disc pl-4 font-semibold">
                        <li>অন্তত <span class="text-indigo-600 font-bold">২০০টি বিজ্ঞাপন/ভিডিও</span> দেখতে হবে। (আপনার বর্তমান: <span id="wallet-video-count">0</span>/200)</li>
                        <li><span class="text-slate-800 font-bold">অথবা</span> অন্তত <span class="text-emerald-600 font-bold">২০টি সফল রেফার</span> করতে হবে। (আপনার বর্তমান: <span id="wallet-refer-count">0</span>/20)</li>
                        <li>সর্বনিম্ন উত্তোলনের পরিমাণ: <span class="text-rose-600 font-bold">৳১৫০০.০০ টাকা</span>।</li>
                    </ul>
                </div>
            </section>

            <!-- --- TAB 5: কাস্টমার সাপোর্ট --- -->
            <section id="support" class="tab-content space-y-4 text-center py-6">
                <div class="bg-white border border-slate-100 p-6 rounded-3xl shadow-sm space-y-4">
                    <h3 class="text-base font-bold text-slate-800">সাহায্য প্রয়োজন?</h3>
                    <div class="w-full bg-rose-500 text-white p-6 rounded-2xl space-y-3">
                        <div class="text-4xl">✈️</div>
                        <h4 class="text-lg font-black">কাস্টমার সার্ভিস</h4>
                        <p class="text-xs text-rose-100">যেকোনো সমস্যা সমাধানের জন্য টেলিগ্রামে যোগাযোগ করুন</p>
                        <div class="bg-white text-slate-900 py-2 px-4 rounded-xl font-bold inline-block text-xs mt-1">
                            @AlifIncomeBDSupport
                        </div>
                    </div>
                </div>
            </section>

        </main>

        <!-- ================= WITHDRAWAL MODAL SYSTEM ================= -->
        <div id="withdraw-modal" class="absolute inset-0 bg-black/50 z-50 hidden flex items-end justify-center">
            <div class="bg-white w-full rounded-t-3xl p-5 space-y-4 shadow-2xl">
                <div class="flex justify-between items-center border-b border-slate-100 pb-3">
                    <h3 class="text-base font-bold text-slate-800">📤 ব্যালেন্স উত্তোলন (Withdraw)</h3>
                    <button onclick="document.getElementById('withdraw-modal').classList.add('hidden')" class="text-slate-400 font-bold text-lg">✕</button>
                </div>

                <div class="space-y-3 text-xs">
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">পেইমেন্ট মেথড</label>
                        <select id="withdraw-method" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-3 text-slate-700 font-bold outline-none text-sm">
                            <option value="বিকাশ">বিকাশ (Bkash)</option>
                            <option value="নগদ">নগদ (Nagad)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">উত্তোলন নাম্বার</label>
                        <input id="withdraw-number" type="text" placeholder="আপনার ফোন নম্বরটি লিখুন" class="w-full bg-slate-50 border border-slate-200 text-slate-700 font-bold rounded-xl px-3 py-3 outline-none text-sm">
                    </div>
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">পরিমাণ (৳)</label>
                        <input id="withdraw-amount" type="number" placeholder="নূন্যতম ৳১৫০০" class="w-full bg-slate-50 border border-slate-200 text-indigo-600 font-bold rounded-xl px-3 py-3 outline-none text-sm">
                    </div>
                </div>

                <button onclick="processWithdraw()" class="w-full bg-indigo-600 text-white font-bold py-3.5 rounded-xl text-sm">
                    উত্তোলন রিকোয়েস্ট পাঠান
                </button>
            </div>
        </div>

        <!-- ================= APP NAVIGATION BOTTOM BAR ================= -->
        <nav class="absolute bottom-0 left-0 right-0 bg-white border-t border-slate-200 px-2 py-2 flex justify-around items-center z-50 shadow-[0_-2px_10px_rgba(0,0,0,0.03)] shrink-0">
            <button onclick="switchTab('home')" class="nav-btn flex flex-col items-center gap-1 text-indigo-600 font-bold text-[10px] flex-1">
                <span class="text-lg">🏠</span> হোম
            </button>
            <button onclick="switchTab('tasks')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">📋</span> কাজ
            </button>
            <button onclick="switchTab('invite')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">👥</span> রেফার
            </button>
            <button onclick="switchTab('wallet')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">💳</span> ওয়ালেট
            </button>
            <button onclick="switchTab('support')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">🎧</span> সাপোর্ট
            </button>
        </nav>

    </div>

    <!-- ================= JAVASCRIPT STATE & LOGIC SYSTEM ================= -->
    <script>
        // গ্লোবাল ডাটা স্টেট
        let currentBalance = 0.00;
        let todayVideosWatched = 0;
        let totalVideosWatched = 0;
        let totalRefers = 0;

        // ইউজার ইন্টারফেস (UI) আপডেট করার ফাংশন
        function updateAppUI() {
            // ব্যালেন্স আপডেট
            document.getElementById('nav-balance').innerText = currentBalance.toFixed(2);
            document.getElementById('home-balance').innerText = currentBalance.toFixed(2);
            
            // ভিডিও টাস্ক পরিসংখ্যান আপডেট
            document.getElementById('total-video-count').innerText = totalVideosWatched + " / 200";
            document.getElementById('today-task-count').innerText = todayVideosWatched + " / 15";
            document.getElementById('wallet-video-count').innerText = totalVideosWatched;
            
            // প্রোগ্রেস বার অ্যানিমেশন
            let progressPercent = (todayVideosWatched / 15) * 100;
            document.getElementById('task-progress-bar').style.width = progressPercent + "%";
            
            // রেফার পরিসংখ্যান আপডেট
            document.getElementById('home-refer-count').innerText = totalRefers + " / 20";
            document.getElementById('wallet-refer-count').innerText = totalRefers;
        }

        // ট্যাব পরিবর্তনের ফাংশন
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('text-indigo-600');
                btn.classList.add('text-slate-400');
            });
            
            const activeIndex = { 'home': 0, 'tasks': 1, 'invite': 2, 'wallet': 3, 'support': 4 }[tabId];
            if(activeIndex !== undefined) {
                document.querySelectorAll('.nav-btn')[activeIndex].classList.add('text-indigo-600');
                document.querySelectorAll('.nav-btn')[activeIndex].classList.remove('text-slate-400');
            }
        }

        // প্রতিদিন ১৫টি ভিডিও দেখার মূল ফাংশন
        function watchVideoAd() {
            if (todayVideosWatched >= 15) {
                alert("আপনার আজকের ১৫টি ভিডিও দেখার লিমিট শেষ! আগামীকাল আবার নতুন টাস্ক পাবেন।");
                return;
            }

            alert("ভিডিও লোড হচ্ছে... অনুগ্রহ করে ৫ সেকেন্ড অপেক্ষা করুন।");
            
            setTimeout(() => {
                todayVideosWatched++;
                totalVideosWatched++;
                currentBalance += 10.00; // প্রতি ভিডিওতে ১০ টাকা ইনকাম
                updateAppUI();
                alert("টাস্ক সফল! আপনার ওয়ালেটে ৳১০.০০ টাকা যোগ করা হয়েছে।");
            }, 1000);
        }

        // ডেমো রেফার যোগ করার ফাংশন (টেস্টিং পারপাস)
        function addDemoRefer() {
            totalRefers++;
            currentBalance += 50.00; // প্রতি রেফারে ৫০ টাকা বোনাস
            updateAppUI();
            alert("১টি সফল রেফার যুক্ত হয়েছে এবং ৳৫০.০০ বোনাস দেওয়া হয়েছে!");
        }

        // উইথড্রাল মোডাল ওপেন করা
        function openWithdrawModal() {
            document.getElementById('withdraw-modal').classList.remove('hidden');
        }

        // টাকা উত্তোলনের লজিক ও শর্ত ভেরিফিকেশন
        function processWithdraw() {
            const number = document.getElementById('withdraw-number').value.trim();
            const amount = parseFloat(document.getElementById('withdraw-amount').value);

            if (!number || isNaN(amount)) {
                alert("দয়া করে সঠিক মোবাইল নম্বর এবং অ্যামাউন্ট লিখুন।");
                return;
            }

            if (amount < 1500) {
                alert("দুঃখিত, সর্বনিম্ন উত্তোলনের পরিমাণ ৳১৫০০.০০ টাকা হতে হবে।");
                return;
            }

            if (currentBalance < amount) {
                alert("আপনার অ্যাকাউন্টে পর্যাপ্ত ব্যালেন্স নেই।");
                return;
            }

            // শর্ত চেক: ২০০ ভিডিও অথবা ২০ রেফার যেকোনো একটি পূরণ থাকতে হবে
            if (totalVideosWatched >= 200 || totalRefers >= 20) {
                alert("আপনার উইথড্রাল রিকোয়েস্টটি সফলভাবে গ্রহণ করা হয়েছে! ভেরিফিকেশনের পর পেমেন্ট পেয়ে যাবেন।");
                document.getElementById('withdraw-modal').classList.add('hidden');
            } else {
                alert("উত্তোলনের শর্ত (২০০ ভিডিও অথবা ২০ রেফার) পূরণ হয়নি!");
            }
        }

        // অ্যাপ চালুর শুরুতে ইন্টারফেস রিফ্রেশ
        updateAppUI();
    </script>
</body>
</html>
