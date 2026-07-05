<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ALIF_INCOME_BD</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #0b0f19;
            user-select: none;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="flex justify-center items-center min-h-screen p-2">

    <!-- App Container (Premium Edge Design) -->
    <div class="w-full max-w-md h-[95vh] bg-[#111625] text-slate-100 rounded-[36px] shadow-2xl border border-slate-800 flex flex-col overflow-hidden relative">
        
        <!-- ================= APP HEADER ================= -->
        <header class="bg-[#111625]/90 backdrop-blur-md border-b border-slate-800/80 px-6 py-4 flex items-center justify-between shrink-0 sticky top-0 z-50">
            <div class="flex items-center gap-2">
                <span class="text-xl font-black bg-gradient-to-r from-orange-400 via-amber-400 to-yellow-500 bg-clip-text text-transparent tracking-wide">ALIF_INCOME_BD</span>
                <span class="bg-emerald-500/20 text-emerald-400 text-[10px] px-2 py-0.5 rounded-full font-bold border border-emerald-500/30">✓ OFFICIAL</span>
            </div>
            <div class="w-2.5 h-2.5 bg-emerald-500 rounded-full animate-pulse"></div>
        </header>

        <!-- ================= MAIN CONTENT SCROLLABLE ================= -->
        <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 pb-28 space-y-5">
            
            <!-- --- TAB 1: HOME --- -->
            <section id="home" class="tab-content active space-y-4">
                <!-- User Profile & Status -->
                <div class="flex items-center justify-between bg-slate-800/30 border border-slate-800/80 p-4 rounded-2xl">
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-2xl bg-gradient-to-tr from-amber-500 to-orange-600 flex items-center justify-center text-white font-bold text-lg shadow-lg">
                            A
                        </div>
                        <div>
                            <h3 class="font-bold text-slate-200 text-sm flex items-center gap-1">ALIF_INCOME_BD <span class="text-amber-400 text-xs">✓</span></h3>
                            <p class="text-[11px] text-slate-500 font-mono">ID: 9948271</p>
                        </div>
                    </div>
                    <span class="bg-orange-500/10 text-orange-400 border border-orange-500/20 text-xs px-2.5 py-1 rounded-xl font-bold">VIP 0</span>
                </div>

                <!-- Total Balance Card (Glossy Orange Curve Style) -->
                <div class="bg-gradient-to-br from-orange-500 via-amber-600 to-yellow-600 rounded-3xl p-6 text-white shadow-xl relative overflow-hidden">
                    <div class="absolute -right-8 -top-8 w-32 h-32 bg-white/10 rounded-full blur-2xl"></div>
                    <p class="text-xs font-semibold text-orange-100 tracking-wider uppercase opacity-90">বর্তমান ব্যালেন্স</p>
                    <div class="flex items-baseline gap-1 mt-2">
                        <span class="text-3xl font-bold text-orange-200">৳</span>
                        <h1 id="user-balance" class="text-5xl font-black tracking-tight font-mono">0.00</h1>
                    </div>
                </div>

                <!-- Live Ticker Info -->
                <div class="bg-slate-800/50 border border-slate-700/50 rounded-xl py-2.5 px-3 flex items-center gap-2 text-xs text-slate-300 font-medium">
                    <span class="animate-bounce">💸</span>
                    <marquee scrollamount="4">ALIF_INCOME_BD-এ প্রতিদিন ২০টি কাজ করুন! প্রতি ভিডিও ৳১০! ১৫০টি ভিডিও অথবা ২০টি রেফারে উত্তোলন!</marquee>
                </div>

                <!-- Modern Dashboard Grid Layout -->
                <div class="grid grid-cols-2 gap-3.5">
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-orange-400 font-semibold text-xs">
                            ⚡ <span>আজকের কাজ</span>
                        </div>
                        <span id="stat-tasks" class="text-2xl font-black text-slate-200 mt-2 font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-amber-400 font-semibold text-xs">
                            👥 <span>মোট রেফার</span>
                        </div>
                        <span id="stat-refers" class="text-2xl font-black text-slate-200 mt-2 font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-yellow-400 font-semibold text-xs">
                            📹 <span>বিজ্ঞাপন দেখা</span>
                        </div>
                        <span id="stat-total-ads" class="text-2xl font-black text-slate-200 mt-2 font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-emerald-400 font-semibold text-xs">
                            💰 <span>বোনাস ব্যালেন্স</span>
                        </div>
                        <span class="text-2xl font-black text-slate-200 mt-2 font-mono">৳0.00</span>
                    </div>
                </div>
            </section>

            <!-- --- TAB 2: TASKS --- -->
            <section id="tasks" class="tab-content space-y-4">
                <div class="bg-slate-800/20 border border-slate-800 p-6 rounded-3xl text-center space-y-5">
                    <div>
                        <h2 class="text-lg font-bold text-slate-200">ভিডিও ওয়াচ সেন্টার</h2>
                        <p class="text-xs text-slate-400 mt-1">সঠিকভাবে সম্পূর্ণ ভিডিওটি দেখলে ব্যালেন্স যোগ হবে।</p>
                    </div>
                    
                    <div class="inline-block bg-orange-500/10 text-orange-400 font-bold px-4 py-1.5 rounded-xl text-xs border border-orange-500/20">
                        💰 রিওয়ার্ড: ৳১০.০০ টাকা
                    </div>
                    
                    <div class="space-y-2 pt-2 text-left">
                        <div class="flex justify-between text-xs text-slate-400 px-1">
                            <span>আজকের ভিডিও লিমিট</span>
                            <span id="task-count-txt" class="font-bold text-orange-400 font-mono">0 / 20</span>
                        </div>
                        <div class="w-full bg-slate-950 h-3 rounded-full overflow-hidden p-[2px] border border-slate-800">
                            <div id="task-progress" class="bg-gradient-to-r from-orange-500 to-yellow-500 h-full w-0 rounded-full transition-all duration-300"></div>
                        </div>
                    </div>

                    <button onclick="watchVideoTask()" class="w-full bg-gradient-to-r from-red-500 to-orange-600 hover:from-red-600 hover:to-orange-700 text-white font-bold py-3.5 rounded-2xl text-xs tracking-wide transition-all shadow-lg shadow-red-950/40">
                        ভিডিও বিজ্ঞাপন দেখুন
                    </button>
                </div>
            </section>

            <!-- --- TAB 3: REFER --- -->
            <section id="refer" class="tab-content space-y-4">
                <div class="bg-gradient-to-b from-slate-800/40 to-slate-900/40 border border-slate-800 p-5 rounded-3xl space-y-4">
                    <div class="flex items-center gap-2 text-amber-400">
                        🎁 <h2 class="text-base font-bold text-slate-200">রেফারেল ইনকাম প্রোগ্রাম</h2>
                    </div>
                    <p class="text-xs text-slate-400 leading-relaxed">নিচের লিংকটি শেয়ার করে বন্ধুদের আমন্ত্রণ জানান। আপনার লিংকে নতুন কেউ সাইন-আপ করলে সাথে সাথে বোনাস পাবেন।</p>
                    
                    <div class="bg-amber-500/10 border border-amber-500/20 text-xs py-2.5 px-3 rounded-xl text-center text-amber-400 font-bold">
                        😊 প্রতি সফল রেফারে পাবেন ৳৫০.০০ TAKA বোনাস
                    </div>

                    <div class="bg-slate-950 p-3 rounded-xl flex items-center justify-between border border-slate-800">
                        <input type="text" id="ref-link" readonly value="https://t.me/ALIF_INCOME_BDBot?start=userALIF" class="bg-transparent text-xs text-slate-400 outline-none flex-1 truncate font-mono">
                    </div>

                    <div class="grid grid-cols-2 gap-3 pt-2">
                        <button onclick="copyLink()" class="bg-slate-800 hover:bg-slate-700 text-slate-200 border border-slate-700 font-bold text-xs py-2.5 rounded-xl transition-all">📋 লিংক কপি</button>
                        <button onclick="simulateReferral()" class="bg-amber-600 hover:bg-amber-700 text-white font-bold text-xs py-2.5 rounded-xl transition-all">➕ ডেমো রেফার যোগ</button>
                    </div>
                </div>
            </section>

            <!-- --- TAB 4: WALLET --- -->
            <section id="withdraw" class="tab-content space-y-4">
                <div class="bg-slate-800/20 border border-slate-800 p-4 rounded-3xl space-y-4">
                    
                    <!-- New Withdrawal Rule Header -->
                    <div class="bg-amber-500/10 border border-amber-500/20 p-3.5 rounded-2xl space-y-2 text-xs">
                        <h4 class="font-bold text-amber-400 flex items-center gap-1">⚠️ উইথড্র লক খোলার শর্তাবলী</h4>
                        <p class="text-[11px] text-slate-400">উত্তোলনের জন্য নিচের যেকোনো ১টি শর্ত অবশ্যই পূরণ হতে হবে:</p>
                        <ul class="space-y-1.5 text-slate-300 font-medium pt-1">
                            <li class="flex justify-between items-center bg-slate-900/50 p-2 rounded-lg">
                                <span>• ন্যূনতম ১৫০টি ভিডিও দেখা:</span> 
                                <span id="cond-ads" class="text-orange-400 font-bold font-mono">0 / 150</span>
                            </li>
                            <li class="flex justify-between items-center bg-slate-900/50 p-2 rounded-lg">
                                <span>• অথবা ন্যূনতম ২০টি রেফার করা:</span> 
                                <span id="cond-refers" class="text-yellow-400 font-bold font-mono">0 / 20</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Input Fields -->
                    <div class="space-y-3.5 text-xs">
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">পেমেন্ট গেটওয়ে</label>
                            <select id="method" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-3 py-3 text-slate-200 outline-none focus:border-amber-500 transition-all">
                                <option value="বিকাশ">বিকাশ (Personal)</option>
                                <option value="নগদ">নগদ (Personal)</option>
                            </select>
                        </div>
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">আপনার অ্যাকাউন্ট নম্বর</label>
                            <input type="text" id="account" placeholder="017XXXXXXXX" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-3 py-3 text-slate-200 outline-none focus:border-amber-500 transition-all">
                        </div>
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">টাকার পরিমাণ (৳)</label>
                            <input type="number" id="amount" value="1500" readonly class="w-full bg-slate-900 border border-slate-800 rounded-xl px-3 py-3 text-slate-400 outline-none font-mono font-bold cursor-not-allowed">
                            <span class="text-[10px] text-slate-500 block mt-1">* উত্তোলনের পরিমাণ নির্দিষ্টভাবে ৳১৫০০ টাকা হতে হবে।</span>
                        </div>
                    </div>

                    <button onclick="handleWithdraw()" class="w-full bg-gradient-to-r from-amber-500 to-orange-600 hover:from-amber-600 hover:to-orange-700 text-white font-bold py-3.5 rounded-2xl text-xs tracking-wider uppercase transition-all shadow-lg">
                        উত্তোলন রিকোয়েস্ট সাবমিট
                    </button>
                </div>
            </section>

            <!-- --- TAB 5: SUPPORT --- -->
            <section id="support" class="tab-content space-y-4">
                <div class="bg-slate-800/20 border border-slate-800 p-6 rounded-3xl text-center space-y-4">
                    <h2 class="text-base font-bold text-slate-200">হেল্পলাইন ও কাস্টমার কেয়ার</h2>
                    
                    <div class="bg-gradient-to-br from-slate-900 to-slate-950 border border-slate-800 rounded-2xl p-6 text-white max-w-sm mx-auto space-y-4 flex flex-col items-center">
                        <div class="w-12 h-12 bg-amber-500/10 border border-amber-500/20 text-amber-400 rounded-full flex items-center justify-center">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12.003 21.112c-.114 0-.228-.02-.338-.061-4.08-1.493-7.665-4.48-10.37-8.63A11.758 11.758 0 0 1 0 5.602c0-.36.21-.69.54-.84a24.223 24.223 0 0 1 10.96-2.61c.17 0 .33.04.47.11l.03.01c.21.1.37.28.44.51.52 1.63 1.57 3.01 2.99 3.91 1.41.9 3.1 1.25 4.77.99a1.002 1.002 0 0 1 .94.57c2.31 4.75.98 10.42-3.1 12.35l-.01.01c-.13.06-.27.09-.43.09h-.03z"/></svg>
                        </div>
                        <div>
                            <h3 class="font-bold text-sm text-slate-200">২৪/৭ অনলাইন সাপোর্ট</h3>
                            <p class="text-xs text-slate-400 mt-1">পেমেন্ট বা যেকোনো কাজের সমস্যার জন্য নিচে বাটনে ক্লিক করে যোগাযোগ করুন।</p>
                        </div>
                        <a href="https://t.me/Suupport7" target="_blank" class="bg-amber-600 hover:bg-amber-700 text-white font-bold text-xs px-6 py-2.5 rounded-xl transition-all">
                            টেলিগ্রাম সাপোর্ট (@Suupport7)
                        </a>
                    </div>
                </div>
            </section>

        </main>

        <!-- ================= MODERN BOTTOM BAR NAVIGATION ================= -->
        <nav class="absolute bottom-0 left-0 right-0 bg-[#111625]/95 backdrop-blur-md border-t border-slate-800 px-2 py-2.5 flex justify-around items-center z-50 shadow-xl">
            <button onclick="switchTab('home')" class="nav-btn text-amber-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="home">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
                <span class="text-[10px] font-bold">হোম</span>
            </button>
            <button onclick="switchTab('tasks')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="tasks">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
                <span class="text-[10px] font-bold">কাজ</span>
            </button>
            <button onclick="switchTab('support')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="support">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.36 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                <span class="text-[10px] font-bold">সাপোর্ট</span>
            </button>
            <button onclick="switchTab('refer')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="refer">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                <span class="text-[10px] font-bold">রেফার</span>
            </button>
            <button onclick="switchTab('withdraw')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="withdraw">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"></path></svg>
                <span class="text-[10px] font-bold">ওয়ালেট</span>
            </button>
        </nav>
    </div>

    <!-- ================= JAVASCRIPT SYSTEM LOGIC ================= -->
    <script>
        let balance = 0.00; 
        let todayTasks = 0;
        let totalRefers = 0;
        let totalAdsWatched = 0;
        const maxDailyTasks = 20; // প্রতিদিন ২০টি ভিডিও লিমিট

        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.replace('text-amber-400', 'text-slate-500');
            });
            const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
            if(activeBtn) activeBtn.classList.replace('text-slate-500', 'text-amber-400');
        }

        function updateUI() {
            document.getElementById('user-balance').innerText = balance.toFixed(2);
            document.getElementById('stat-tasks').innerText = todayTasks;
            document.getElementById('stat-refers').innerText = totalRefers;
            document.getElementById('stat-total-ads').innerText = totalAdsWatched;
            document.getElementById('cond-ads').innerText = `${totalAdsWatched} / 150`; // ১৫০ টি বিজ্ঞপ্তির শর্ত
            document.getElementById('cond-refers').innerText = `${totalRefers} / 20`;   // ২০ টি রেফারের শর্ত
            document.getElementById('task-count-txt').innerText = `${todayTasks} / ${maxDailyTasks}`;
        }

        function watchVideoTask() {
            if(todayTasks >= maxDailyTasks) {
                alert("আজকের সর্বোচ্চ ভিডিও লিমিট (২০/২০) শেষ হয়েছে! আগামীকাল আবার চেষ্টা করুন।");
                return;
            }
            alert("ভিডিও বিজ্ঞাপন লোড হচ্ছে... ৫ সেকেন্ড অপেক্ষা করুন।");
            setTimeout(() => {
                balance += 10.00; // প্রতি ভিডিওতে ১০ টাকা ইনকাম
                todayTasks++;
                totalAdsWatched++;
                document.getElementById('task-progress').style.width = `${(todayTasks / maxDailyTasks) * 100}%`;
     
