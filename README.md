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

    <!-- App Container -->
    <div class="w-full max-w-md h-[95vh] bg-[#0c1220] text-slate-100 rounded-[36px] shadow-2xl border border-slate-800 flex flex-col overflow-hidden relative">
        
        <!-- ================= APP HEADER ================= -->
        <header class="bg-[#0c1220]/90 backdrop-blur-md border-b border-slate-800/60 px-6 py-4 flex items-center justify-between shrink-0 sticky top-0 z-50">
            <div class="flex items-center gap-2">
                <span class="text-xl font-black bg-gradient-to-r from-cyan-400 to-blue-500 bg-clip-text text-transparent tracking-wide">ALIF_INCOME_BD</span>
                <span class="bg-cyan-500/20 text-cyan-400 text-[10px] px-2 py-0.5 rounded-full font-bold border border-cyan-500/30">✓ OFFICIAL</span>
            </div>
            <div class="w-2.5 h-2.5 bg-cyan-500 rounded-full animate-pulse"></div>
        </header>

        <!-- ================= MAIN CONTENT SCROLLABLE ================= -->
        <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 pb-28 space-y-4">
            
            <!-- --- TAB 1: হোম --- -->
            <section id="home" class="tab-content active space-y-4">
                <div class="flex items-center justify-between bg-slate-800/30 border border-slate-800/80 p-4 rounded-2xl">
                    <div class="flex items-center gap-3">
                        <div class="w-11 h-11 rounded-xl bg-gradient-to-tr from-cyan-500 to-blue-600 flex items-center justify-center text-white font-bold text-lg shadow-lg">
                            A
                        </div>
                        <div>
                            <h3 class="font-bold text-slate-200 text-sm flex items-center gap-1">ALIF_INCOME_BD <span class="text-cyan-400 text-xs">✓</span></h3>
                            <p class="text-[11px] text-slate-500 font-mono">ID: 9948271</p>
                        </div>
                    </div>
                    <span class="bg-cyan-500/10 text-cyan-400 border border-cyan-500/20 text-xs px-2.5 py-1 rounded-xl font-bold">VIP 0</span>
                </div>

                <!-- Current Balance Card -->
                <div class="bg-gradient-to-br from-slate-800 via-slate-900 to-slate-950 border border-slate-800 rounded-3xl p-6 text-white shadow-xl relative overflow-hidden">
                    <p class="text-xs font-semibold text-cyan-400 tracking-wider uppercase">💰 বর্তমান ব্যালেন্স</p>
                    <div class="flex items-baseline gap-1 mt-2">
                        <span class="text-3xl font-bold text-slate-400">৳</span>
                        <h1 id="user-balance" class="text-5xl font-black tracking-tight font-mono text-slate-100">0.00</h1>
                    </div>
                </div>

                <!-- Total Withdrawn Card -->
                <div class="bg-gradient-to-br from-emerald-950/40 to-slate-900/60 border border-emerald-900/40 rounded-2xl p-4 flex justify-between items-center">
                    <div>
                        <p class="text-xs text-slate-400 font-medium">💸 মোট উত্তোলন করেছেন</p>
                        <div class="flex items-baseline gap-0.5 mt-1">
                            <span class="text-sm font-bold text-emerald-400">৳</span>
                            <span id="total-withdrawn" class="text-xl font-black text-emerald-400 font-mono">0.00</span>
                        </div>
                    </div>
                    <div class="p-3 bg-emerald-500/10 rounded-xl border border-emerald-500/20 text-emerald-400 text-xl">
                        📥
                    </div>
                </div>

                <!-- Modern Dashboard Grid Layout -->
                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800/60">
                        <div class="text-slate-400 font-semibold text-xs">⚡ আজকের কাজ</div>
                        <span id="stat-tasks" class="text-xl font-black text-slate-200 mt-2 block font-mono">0 / 20</span>
                    </div>
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800/60">
                        <div class="text-slate-400 font-semibold text-xs">👥 মোট রেফার</div>
                        <span id="stat-refers" class="text-xl font-black text-slate-200 mt-2 block font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800/60">
                        <div class="text-slate-400 font-semibold text-xs">📹 মোট ভিডিও দেখা</div>
                        <span id="stat-total-ads" class="text-xl font-black text-slate-200 mt-2 block font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/20 p-4 rounded-2xl border border-slate-800/60">
                        <div class="text-slate-400 font-semibold text-xs">🎁 রেফারেল বোনাস</div>
                        <span id="stat-refer-bonus" class="text-xl font-black text-slate-200 mt-2 block font-mono">৳0.00</span>
                    </div>
                </div>
            </section>

            <!-- --- TAB 2: টাস্ক --- -->
            <section id="tasks" class="tab-content space-y-4">
                <div class="bg-slate-800/20 border border-slate-800/60 p-6 rounded-3xl text-center space-y-5">
                    <div>
                        <h2 class="text-lg font-bold text-slate-200">ভিডিও ওয়াচ সেন্টার</h2>
                        <p class="text-xs text-slate-400 mt-1">সম্পূর্ণ ভিডিওটি শেষ পর্যন্ত দেখলে ব্যালেন্স যোগ হবে।</p>
                    </div>
                    
                    <div class="inline-block bg-cyan-500/10 text-cyan-400 font-bold px-4 py-1.5 rounded-xl text-xs border border-cyan-500/20">
                        💰 রিওয়ার্ড: ৳১০.০০ টাকা
                    </div>
                    
                    <div class="space-y-2 pt-2 text-left">
                        <div class="flex justify-between text-xs text-slate-400 px-1">
                            <span>আজকের ভিডিও লিমিট</span>
                            <span id="task-count-txt" class="font-bold text-cyan-400 font-mono">0 / 20</span>
                        </div>
                        <div class="w-full bg-slate-950 h-2.5 rounded-full overflow-hidden p-[1px] border border-slate-800">
                            <div id="task-progress" class="bg-gradient-to-r from-cyan-500 to-blue-500 h-full w-0 rounded-full transition-all duration-300"></div>
                        </div>
                    </div>

                    <button onclick="watchVideoTask()" class="w-full bg-gradient-to-r from-cyan-500 to-blue-600 hover:from-cyan-600 hover:to-blue-700 text-white font-bold py-3.5 rounded-2xl text-xs tracking-wide transition-all shadow-lg">
                        ভিডিও বিজ্ঞাপন দেখুন
                    </button>
                </div>
            </section>

            <!-- --- TAB 3: সাপোর্ট --- -->
            <section id="support" class="tab-content space-y-4">
                <div class="bg-slate-800/20 border border-slate-800/60 p-6 rounded-3xl text-center space-y-5">
                    <div class="w-14 h-14 bg-cyan-500/10 border border-cyan-500/20 text-cyan-400 rounded-full flex items-center justify-center mx-auto text-2xl">
                        🛠️
                    </div>
                    <div>
                        <h2 class="text-base font-bold text-slate-200">২৪/৭ কাস্টমার সার্ভিস</h2>
                        <p class="text-xs text-slate-400 mt-1.5 leading-relaxed">পেমেন্ট রিলেটেড অথবা যেকোনো কারিগরি সমস্যার জন্য সরাসরি আমাদের অফিশিয়াল টেলিগ্রাম কাস্টমার কেয়ারে যোগাযোগ করুন।</p>
                    </div>
                    
                    <a href="https://t.me/Suupport7" target="_blank" class="block w-full bg-slate-800 hover:bg-slate-700 text-cyan-400 border border-slate-700 font-bold text-xs py-3.5 rounded-xl transition-all">
                        টেলিগ্রাম সাপোর্ট (@Suupport7)
                    </a>
                </div>
            </section>

            <!-- --- TAB 4: রেফার --- -->
            <section id="refer" class="tab-content space-y-4">
                <div class="bg-slate-800/20 border border-slate-800/60 p-5 rounded-3xl space-y-4">
                    <h2 class="text-base font-bold text-slate-200 flex items-center gap-2">🔗 বন্ধুদের আমন্ত্রণ জানান</h2>
                    <p class="text-xs text-slate-400 leading-relaxed">আপনার ইনভাইটেশন লিংক ব্যবহার করে নতুন অ্যাকাউন্ট খুললেই পেয়ে যাবেন ইনস্ট্যান্ট বোনাস।</p>
                    
                    <div class="bg-cyan-500/10 border border-cyan-500/20 text-xs py-2.5 px-3 rounded-xl text-center text-cyan-400 font-bold">
                        🎁 প্রতি সফল আমন্ত্রণে বোনাস ৳৫০.০০ টাকা
                    </div>

                    <div class="bg-slate-950 p-3 rounded-xl flex items-center justify-between border border-slate-800">
                        <input type="text" id="ref-link" readonly value="https://t.me/ALIF_INCOME_BDBot?start=userALIF" class="bg-transparent text-xs text-slate-400 outline-none flex-1 truncate font-mono">
                    </div>

                    <div class="grid grid-cols-2 gap-3">
                        <button onclick="copyLink()" class="bg-slate-800 hover:bg-slate-700 text-slate-200 border border-slate-700 font-bold text-xs py-2.5 rounded-xl transition-all">📋 লিংক কপি</button>
                        <button onclick="simulateReferral()" class="bg-cyan-600 hover:bg-cyan-700 text-white font-bold text-xs py-2.5 rounded-xl transition-all">➕ ডেমো রেফার</button>
                    </div>
                </div>
            </section>

            <!-- --- TAB 5: ওয়ালেট --- -->
            <section id="withdraw" class="tab-content space-y-4">
                <div class="bg-slate-800/20 border border-slate-800/60 p-4 rounded-3xl space-y-4">
                    
                    <!-- Locked Rules Header -->
                    <div class="bg-amber-500/10 border border-amber-500/20 p-3.5 rounded-2xl space-y-2 text-xs">
                        <h4 class="font-bold text-amber-400 flex items-center gap-1">⚠️ যেকোনো ১টি শর্ত অবশ্যই পূরণ করুন</h4>
                        <ul class="space-y-1.5 text-slate-300 font-medium pt-1">
                            <li class="flex justify-between items-center bg-slate-900/50 p-2 rounded-lg">
                                <span>• ন্যূনতম ১৫০টি ভিডিও দেখা:</span> 
                                <span id="cond-ads" class="text-cyan-400 font-bold font-mono">0 / 150</span>
                            </li>
                            <li class="flex justify-between items-center bg-slate-900/50 p-2 rounded-lg">
                                <span>• অথবা ন্যূনতম ২০টি রেফার করা:</span> 
                                <span id="cond-refers" class="text-cyan-400 font-bold font-mono">0 / 20</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Input Fields -->
                    <div class="space-y-3 text-xs">
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">পেমেন্ট গেটওয়ে</label>
                            <select id="method" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-3 py-3 text-slate-200 outline-none focus:border-cyan-500 transition-all">
                                <option value="বিকাশ">বিকাশ (Personal)</option>
                                <option value="নগদ">নগদ (Personal)</option>
                            </select>
                        </div>
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">আপনার অ্যাকাউন্ট নম্বর</label>
                            <input type="text" id="account" placeholder="01XXXXXXXXX" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-3 py-3 text-slate-200 outline-none focus:border-cyan-500 transition-all">
                        </div>
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">টাকার পরিমাণ (৳)</label>
                            <input type="number" id="amount" value="1500" readonly class="w-full bg-slate-900 border border-slate-800 rounded-xl px-3 py-3 text-slate-400 outline-none font-mono font-bold cursor-not-allowed">
                        </div>
                    </div>

                    <button onclick="handleWithdraw()" class="w-full bg-gradient-to-r from-cyan-500 to-blue-600 hover:from-cyan-600 hover:to-blue-700 text-white font-bold py-3.5 rounded-2xl text-xs tracking-wider transition-all shadow-lg">
                        উত্থাপন রিকোয়েস্ট সাবমিট
                    </button>
                </div>

                <!-- Withdraw History Section -->
                <div class="bg-slate-800/10 border border-slate-800/60 p-4 rounded-3xl space-y-3">
                    <h3 class="text-xs font-bold text-slate-300 uppercase tracking-wider">📋 উত্তোলনের ইতিহাস</h3>
                    <div id="history-container" class="space-y-2 max-h-[160px] overflow-y-auto no-scrollbar">
                        <p id="no-history" class="text-xs text-slate-500 text-center py-4">এখনো কোনো উত্তোলনের রেকর্ড নেই।</p>
                    </div>
                </div>
            </section>

        </main>

        <!-- ================= BOTTOM NAVIGATION BAR (IMG MATCHED) ================= -->
        <nav class="absolute bottom-0 left-0 right-0 bg-[#070b14] border-t border-slate-800/80 px-2 py-3 flex justify-around items-center z-50 shadow-2xl rounded-b-[36px]">
            <!-- হোম -->
            <button onclick="switchTab('home')" class="nav-btn text-cyan-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="home">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
                <span class="text-[11px] font-bold">হোম</span>
            </button>
            <!-- টাস্ক -->
            <button onclick="switchTab('tasks')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="tasks">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
                <span class="text-[11px] font-bold">টাস্ক</span>
            </button>
            <!-- সাপোর্ট -->
            <button onclick="switchTab('support')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="support">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.36 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                <span class="text-[11px] font-bold">সাপোর্ট</span>
            </button>
            <!-- রেফার -->
            <button onclick="switchTab('refer')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="refer">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                <span class="text-[11px] font-bold">রেফার</span>
            </button>
            <!-- ওয়ালেট -->
            <button onclick="switchTab('withdraw')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="withdraw">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"></path></svg>
                <span class="text-[11px] font-bold">ওয়ালেট</span>
            </button>
        </nav>
    </div>

    <!-- ================= SYSTEM SCRIPTS ================= -->
    <script>
        let balance = 0.00; 
        let withdrawnTotal = 0.00;
        let todayTasks = 0;
        let totalRefers = 0;
        let totalAdsWatched = 0;
        let referBonus = 0.00;
        const maxDailyTasks = 20;

        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.replace('text-cyan-400', 'text-slate-500');
            });
            const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
            if(activeBtn) activeBtn.classList.replace('text-slate-500', 'text-cyan-400');
        }

        function updateUI() {
            document.getElementById('user-balance').innerText = balance.toFixed(2);
            document.getElementById('total-withdrawn').innerText = withdrawnTotal.toFixed(2);
            document.getElementById('stat-tasks').innerText = `${todayTasks} / ${maxDailyTasks}`;
            document.getElementById('stat-refers').innerText = totalRefers;
            document.getElementById('stat-total-ads').innerText = totalAdsWatched;
            document.getElementById('stat-refer-bonus').innerText = `৳${referBonus.toFixed(2)}`;
            
            document.getElementById('cond-ads').innerText = `${totalAdsWatched} / 150`; 
            document.getElementById('cond-refers').innerText = `${totalRefers} / 20`;   
            document.getElementById('task-count-txt').innerText = `${todayTasks} / ${maxDailyTasks}`;
        }

        function watchVideoTask() {
            if(todayTasks >= maxDailyTasks) {
                alert("আজকের সর্বোচ্চ ভিডিও লিমিট (২০/২০) শেষ হয়েছে!");
                return;
            }
            alert("ভিডিও প্লে হচ্ছে... ৫ সেকেন্ড অপেক্ষা করুন।");
            setTimeout(() => {
                balance += 10.00; 
                todayTasks++;
                totalAdsWatched++;
                document.getElementById('task-progress').style.width = `${(todayTasks / maxDailyTasks) * 100}%`;
                updateUI();
                alert("সফলভাবে ভিডিও দেখা সম্পন্ন! ওয়ালেটে ৳১০ যোগ হয়েছে।");
            }, 1200);
        }

        function simulateReferral() {
            balance += 50.00; 
            referBonus += 50.00;
            totalRefers++;
            updateUI();
            alert("সফলভাবে ১টি ডেমো রেফার যোগ হয়েছে এবং ৳৫০ বোনাস দেওয়া হয়েছে!");
        }

        function copyLink() {
            const input = document.getElementById('ref-link');
      
