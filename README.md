<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ADDS JOB CITY</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #f4f6fa;
            user-select: none;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .app-container {
            max-width: 450px;
            width: 100%;
            height: 100vh;
            background-color: #fcfdfe;
        }
    </style>
</head>
<body class="flex justify-center items-center min-h-screen">

<div class="app-container flex flex-col relative shadow-xl overflow-hidden border-x border-gray-100">
    
    <!-- ================= APP HEADER ================= -->
    <header class="bg-white border-b border-gray-100 px-4 py-3 flex items-center justify-between shrink-0">
        <div class="flex items-center gap-2">
            <span class="text-xl font-bold text-gray-800 tracking-wide">ADDS JOB CITY 💼</span>
            <span class="text-emerald-500 font-bold text-sm">✓</span>
        </div>
        <div class="flex items-center gap-3">
            <button class="text-gray-400 relative">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path></svg>
            </button>
        </div>
    </header>

    <!-- ================= MAIN SCROLLABLE WRAPPER ================= -->
    <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 pb-24 space-y-4">
        
        <!-- --- TAB 1: HOME --- -->
        <section id="home" class="tab-content active space-y-4">
            <!-- User Profile Structure -->
            <div class="flex items-center gap-3 bg-white p-2 rounded-xl">
                <div class="w-12 h-12 rounded-full bg-indigo-600 flex items-center justify-center text-white font-bold border-2 border-indigo-200">
                    MD
                </div>
                <div>
                    <h3 class="font-bold text-gray-800 text-base flex items-center gap-1">MD <span class="text-blue-500 text-xs">✓</span></h3>
                    <p class="text-xs text-gray-400">ID: 8847291</p>
                </div>
            </div>

            <!-- Total Balance Card -->
            <div class="bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 rounded-2xl p-6 text-white shadow-md relative overflow-hidden">
                <p class="text-sm font-medium opacity-90">মোট ব্যালেন্স</p>
                <div class="flex items-baseline gap-1 mt-2">
                    <span class="text-4xl font-extrabold tracking-tight">৳</span>
                    <h1 id="user-balance" class="text-5xl font-black tracking-tight">1477.00</h1>
                </div>
                <div class="absolute -right-6 -bottom-6 w-24 h-24 bg-white/10 rounded-full blur-xl"></div>
            </div>

            <!-- Live Text Ticker Animation -->
            <div class="bg-amber-50 border border-amber-100 rounded-xl py-2 px-3 flex items-center gap-2 text-xs text-amber-700 font-medium">
                🎉 <marquee scrollamount="4">Aka*** সবেমাত্র ৳৯৬৭০ উত্তোলন করেছেন! • ভিডিও দেখে ইনকাম করুন প্রতি ভিডিও ১০ টাকা!</marquee>
            </div>

            <!-- Grid Data Arrays -->
            <div class="grid grid-cols-2 gap-3">
                <div class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm flex flex-col justify-between">
                    <div class="flex items-center gap-2 text-indigo-500 font-semibold text-sm">
                        ⚡ <span>মোট টাস্ক</span>
                    </div>
                    <span id="stat-tasks" class="text-2xl font-bold text-gray-800 mt-2">3</span>
                </div>
                <div class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm flex flex-col justify-between">
                    <div class="flex items-center gap-2 text-purple-500 font-semibold text-sm">
                        👥 <span>মোট রেফার</span>
                    </div>
                    <span id="stat-refers" class="text-2xl font-bold text-gray-800 mt-2">3</span>
                </div>
                <div class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm flex flex-col justify-between">
                    <div class="flex items-center gap-2 text-pink-500 font-semibold text-sm">
                        📹 <span>বিজ্ঞাপন দেখা</span>
                    </div>
                    <span id="stat-total-ads" class="text-2xl font-bold text-gray-800 mt-2">105</span>
                </div>
                <div class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm flex flex-col justify-between">
                    <div class="flex items-center gap-2 text-emerald-500 font-semibold text-sm">
                        💰 <span>ননাস ব্যালেন্স</span>
                    </div>
                    <span class="text-2xl font-bold text-gray-800 mt-2">৳0.00</span>
                </div>
            </div>
        </section>

        <!-- --- TAB 2: TASKS --- -->
        <section id="tasks" class="tab-content space-y-4">
            <div class="bg-indigo-50/60 border border-indigo-100/80 p-5 rounded-2xl text-center space-y-4">
                <h2 class="text-lg font-bold text-indigo-900">বিজ্ঞাপন দেখুন</h2>
                <p class="text-xs text-gray-500">প্রতি বিজ্ঞাপন দেখে ৳১০.০০ ইনকাম করুন</p>
                
                <div class="inline-block bg-white text-indigo-600 font-bold px-4 py-1.5 rounded-full text-xs shadow-sm border border-indigo-100">
                    💵 রিওয়ার্ড: ৳১০.০০ টাকা
                </div>
                
                <div class="space-y-1 pt-2">
                    <div class="flex justify-between text-xs text-gray-500 px-1">
                        <span>আজকের সম্পন্ন</span>
                        <span id="task-count-txt" class="font-bold">0 / 15</span>
                    </div>
                    <div class="w-full bg-gray-200 h-2 rounded-full overflow-hidden">
                        <div id="task-progress" class="bg-indigo-600 h-full w-0 transition-all duration-300"></div>
                    </div>
                </div>

                <button onclick="watchVideoTask()" class="w-full bg-red-500 hover:bg-red-600 text-white font-bold py-3 rounded-xl text-sm transition-all shadow-md shadow-red-100">
                    বিজ্ঞাপন দেখুন
                </button>
            </div>
        </section>

        <!-- --- TAB 3: REFER --- -->
        <section id="refer" class="tab-content space-y-4">
            <div class="bg-slate-900 text-white p-5 rounded-2xl space-y-4 relative overflow-hidden">
                <div class="flex items-center gap-2">
                    🎁 <h2 class="text-base font-bold">বন্ধুকে রেফার করুন এবং আয় করুন</h2>
                </div>
                <p class="text-xs text-slate-300 leading-relaxed">আপনার রেফার লিংকটি শেয়ার করুন এবং আপনার বন্ধুদের আমন্ত্রণ করুন। আপনার বন্ধু সাইন আপ করলে আপনি <span class="text-yellow-400 font-bold">৳৯৯.০০ TAKA</span> বোনাস পাবেন।</p>
                
                <div class="bg-white/5 border border-white/10 text-xs py-2 px-3 rounded-lg text-center text-indigo-300 font-semibold">
                    😊 প্রতি রেফারে ৳৯৯.০০ TAKA বোনাস
                </div>

                <div class="bg-black/20 p-2.5 rounded-xl flex items-center justify-between border border-white/5">
                    <input type="text" id="ref-link" readonly value="https://t.me/AddsJobCityBot?start=userMD" class="bg-transparent text-xs text-slate-300 outline-none flex-1 truncate font-mono select-all">
                </div>

                <div class="grid grid-cols-2 gap-3 pt-2">
                    <button onclick="copyLink()" class="bg-pink-600 hover:bg-pink-700 text-white font-bold text-xs py-2.5 rounded-xl transition-all flex items-center justify-center gap-1">📋 লিংক কপি করুন</button>
                    <button onclick="simulateReferral()" class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold text-xs py-2.5 rounded-xl transition-all">➕ ডেমো রেফার যোগ</button>
                </div>
            </div>
        </section>

        <!-- --- TAB 4: WALLET --- -->
        <section id="withdraw" class="tab-content space-y-4">
            <div class="bg-white border border-gray-100 p-4 rounded-xl space-y-3 shadow-sm">
                <div class="bg-blue-50 border border-blue-100 p-3 rounded-xl space-y-2 text-xs">
                    <h4 class="font-bold text-blue-800 flex items-center gap-1">⚠️ উত্তোলনের শর্তাবলী</h4>
                    <p class="text-blue-700">উত্তোলনের জন্য নিচের যেকোনো একটি শর্ত পূরণ করতে হবে:</p>
                    <ul class="space-y-1 text-slate-600 font-medium">
                        <li class="flex justify-between">• অন্তত ১০০টি বিজ্ঞাপন দেখতে হবে। <span id="cond-ads" class="text-emerald-600 font-bold">105 / 100</span></li>
                        <li class="flex justify-between">• অথবা অন্তত ৪টি সফল রেফার করতে হবে। <span id="cond-refers" class="text-purple-600 font-bold">3 / 4</span></li>
                    </ul>
                </div>

                <!-- Withdrawal Form Fields -->
                <div class="space-y-3 text-xs">
                    <div>
                        <label class="text-gray-600 font-bold block mb-1">পেমেন্ট মেথড</label>
                        <select id="method" class="w-full bg-gray-50 border border-gray-200 rounded-xl px-3 py-2.5 font-medium text-gray-800 outline-none focus:border-indigo-500 transition-all">
                            <option value="বিকাশ">বিকাশ</option>
                            <option value="নগদ">নগদ</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-gray-600 font-bold block mb-1">উত্তোলন নাম্বার/Binance ID</label>
                        <input type="text" id="account" placeholder="আপনার ফোন নম্বর বা অ্যাড্রেস লিখুন" class="w-full bg-gray-50 border border-gray-200 rounded-xl px-3 py-2.5 outline-none focus:border-indigo-500 transition-all">
                    </div>
                    <div>
                        <label class="text-gray-600 font-bold block mb-1">পরিমাণ (৳)</label>
                        <input type="number" id="amount" placeholder="ন্যূনতম ৳১৩০০" class="w-full bg-gray-50 border border-gray-200 rounded-xl px-3 py-2.5 outline-none focus:border-indigo-500 transition-all font-mono">
                    </div>
                </div>

                <button onclick="handleWithdraw()" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 rounded-xl text-xs tracking-wider uppercase transition-all shadow-md">
                    উত্তোলন করুন
                </button>
            </div>
        </section>

        <!-- --- TAB 5: SUPPORT --- -->
        <section id="support" class="tab-content space-y-4">
            <div class="bg-white border border-gray-100 p-6 rounded-2xl text-center space-y-4 shadow-sm">
                <h2 class="text-base font-bold text-gray-800">সাহায্য প্রয়োজন?</h2>
                
                <div class="bg-gradient-to-br from-red-500 to-red-600 rounded-2xl p-6 text-white max-w-sm mx-auto space-y-4 flex flex-col items-center shadow-lg shadow-red-100">
                    <div class="w-12 h-12 bg-white/20 rounded-full flex items-center justify-center">
                        <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24"><path d="M12.003 21.112c-.114 0-.228-.02-.338-.061-4.08-1.493-7.665-4.48-10.37-8.63A11.758 11.758 0 0 1 0 5.602c0-.36.21-.69.54-.84a24.223 24.223 0 0 1 10.96-2.61c.17 0 .33.04.47.11l.03.01c.21.1.37.28.44.51.52 1.63 1.57 3.01 2.99 3.91 1.41.9 3.1 1.25 4.77.99a1.002 1.002 0 0 1 .94.57c2.31 4.75.98 10.42-3.1 12.35l-.01.01c-.13.06-.27.09-.43.09h-.03z"/></svg>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">কাস্টমার সাপোর্ট</h3>
                        <p class="text-xs text-red-100 mt-1">যেকোনো সমস্যা সমাধানের জন্য আমাদের সাথে যোগাযোগ করুন</p>
                    </div>
                    <a href="https://t.me/Suupport7" target="_blank" class="bg-white/20 hover:bg-white/30 text-white font-bold text-sm px-6 py-2 rounded-xl transition-all tracking-wide">
                        @Suupport7
                    </a>
                </div>
            </div>
        </section>

    </main>

    <!-- ================= PREMIUM STRUCTURAL NAVIGATION BOTTOM BAR ================= -->
    <nav class="absolute bottom-0 left-0 right-0 bg-white border-t border-gray-100 px-2 py-2 flex justify-around items-center z-50 shadow-lg">
        <button onclick="switchTab('home')" class="nav-btn text-indigo-600 flex flex-col items-center gap-1 w-14 transition-all" data-tab="home">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[11px] font-medium">হোম</span>
        </button>
        <button onclick="switchTab('tasks')" class="nav-btn text-gray-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="tasks">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
            <span class="text-[11px] font-medium">কাজ</span>
        </button>
        <button onclick="switchTab('support')" class="nav-btn text-gray-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="support">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
            <span class="text-[11px] font-medium">সাপোর্ট</span>
        </button>
        <button onclick="switchTab('refer')" class="nav-btn text-gray-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="refer">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
            <span class="text-[11px] font-medium">রেফার</span>
        </button>
        <button onclick="switchTab('withdraw')" class="nav-btn text-gray-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="withdraw">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"></path></svg>
            <span class="text-[11px] font-medium">ওয়ালেট</span>
        </button>
    </nav>
</div>

<!-- ================= PLATFORM JAVASCRIPT CORE ENGINE ================= -->
<script>
    let balance = 1477.00;
    let todayTasks = 3;
    let totalRefers = 3;
    let totalAdsWatched = 105;

    function switchTab(tabId) {
        document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
        document.getElementById(tabId).classList.add('active');
        
        document.querySelectorAll('.nav-btn').forEach(btn => {
            btn.classList.replace('text-indigo-600', 'text-gray-400');
        });
        const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
        if(activeBtn) activeBtn.classList.replace('text-gray-400', 'text-indigo-600');
    }

    function updateUI() {
        document.getElementById('user-balance').innerText = balance.toFixed(2);
        document.getElementById('stat-tasks').innerText = todayTasks;
        document.getElementById('stat-refers').innerText = totalRefers;
        document.getElementById('stat-total-ads').innerText = totalAdsWatched;
        
        document.getElementById('cond-ads').innerText = `${totalAdsWatched} / 100`;
        document.getElementById('cond-refers').innerText = `${totalRefers} / 4`;
        document.getElementById('task-count-txt').innerText = `${todayTasks} / 15`;
    }

    function watchVideoTask() {
        if(todayTasks >= 15) {
            alert("আজকের সর্বোচ্চ ভিডিও লিমিট (১৫/১৫) শেষ হয়েছে!");
            return;
        }
        
        alert("বিজ্ঞাপন লোড হচ্ছে... ৫ সেকেন্ড অপেক্ষা করুন।");
        
        setTimeout(() => {
            balance += 10.00;
            todayTasks++;
            totalAdsWatched++;
            
            document.getElementById('task-progress').style.width = `${(todayTasks / 15) * 100}%`;
            updateUI();
            alert("সফলভাবে বিজ্ঞাপন দেখা সম্পন্ন হয়েছে! আপনার অ্যাকাউন্টে ৳১০ যোগ করা হয়েছে।");
        }, 1500);
    }

    function simulateReferral() {
        balance += 99.00;
        totalRefers++;
        updateUI();
        alert("সফল রেফারেল নোড যুক্ত হয়েছে! বোনাস ৳৯৯.০০ ব্যালেন্সে যোগ করা হলো।");
    }

    function copyLink() {
        const input = document.getElementById('ref-link');
        input.select();
        document.execCommand('copy');
        alert("রেফারেল লিংক সফলভাবে কপি হয়েছে!");
    }

    function handleWithdraw() {
        const account = document.getElementById('account').value;
        const amount = parseFloat(document.getElementById('amount').value);

        if(!account || isNaN(amount)) {
            alert("দয়া করে সঠিক অ্যাকাউন্ট নাম্বার এবং পরিমাণ লিখুন!");
            return;
        }
        if(amount < 1300) {
            alert("দুঃখিত! সর্বনিম্ন উত্তোলনের পরিমাণ ৳১৩০০ টাকা।");
            return;
        }
        if(balance < amount) {
            alert("আপনার অ্যাকাউন্টে পর্যাপ্ত ব্যালেন্স নেই!");
            return;
        }

        // Hard lock check condition logic validation (Ads >= 100 OR Refers >= 4)
        if(totalAdsWatched < 100 && totalRefers < 4) {
            alert("উত্তোলন লক! আপনাকে অবশ্যই অন্তত ১০০টি ভিডিও দেখতে হবে অথবা ৪টি সফল রেফার সম্পন্ন করতে হবে।");
            return;
        }

        balance -= amount;
        updateUI();
        alert("আপনার উইথড্র রিকোয়েস্টটি সফলভাবে সাবমিট হয়েছে। এডমিন প্যানেল রিভিউ করার পর পেমেন্ট পেয়ে যাবেন।");
    }
</script>

</body>
</html>
