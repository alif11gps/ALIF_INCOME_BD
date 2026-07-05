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
            background-color: #0f172a;
            user-select: none;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="flex justify-center items-center min-h-screen">

    <!-- App Container -->
    <div class="w-full max-w-md h-[92vh] bg-slate-900 text-slate-100 rounded-[32px] shadow-2xl border border-slate-800 flex flex-col overflow-hidden relative">
        
        <!-- ================= APP HEADER ================= -->
        <header class="bg-slate-900/80 backdrop-blur-md border-b border-slate-800/60 px-5 py-4 flex items-center justify-between shrink-0 sticky top-0 z-50">
            <div class="flex items-center gap-2">
                <span class="text-lg font-bold bg-gradient-to-r from-cyan-400 to-blue-500 bg-clip-text text-transparent tracking-wide">ALIF_INCOME_BD 💼</span>
                <span class="bg-emerald-500/20 text-emerald-400 text-[10px] px-1.5 py-0.5 rounded-full font-bold border border-emerald-500/30">✓ Verified</span>
            </div>
            <div class="flex items-center gap-3">
                <button class="text-slate-400 hover:text-slate-200 relative p-1 rounded-lg bg-slate-800/50">
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path></svg>
                </button>
            </div>
        </header>

        <!-- ================= MAIN SCROLLABLE CONTENT ================= -->
        <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 pb-28 space-y-4">
            
            <!-- --- TAB 1: HOME --- -->
            <section id="home" class="tab-content active space-y-4">
                <!-- User Profile Card -->
                <div class="flex items-center gap-3 bg-slate-800/40 border border-slate-800 p-3 rounded-2xl">
                    <div class="w-11 h-11 rounded-xl bg-gradient-to-tr from-blue-600 to-cyan-500 flex items-center justify-center text-white font-bold shadow-lg shadow-blue-500/20">
                        AL
                    </div>
                    <div>
                        <h3 class="font-bold text-slate-200 text-sm flex items-center gap-1">ALIF_INCOME_BD <span class="text-cyan-400 text-xs">✓</span></h3>
                        <p class="text-[11px] text-slate-500 font-mono">ID: 8847291</p>
                    </div>
                </div>

                <!-- Total Balance Card (Modern Curved Shape) -->
                <div class="bg-gradient-to-br from-slate-800 via-indigo-950 to-slate-900 border border-indigo-500/20 rounded-3xl p-6 text-white shadow-xl relative overflow-hidden">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-indigo-500/10 rounded-full blur-2xl"></div>
                    <p class="text-xs font-medium text-indigo-300 tracking-wider uppercase opacity-90">মোট ব্যালেন্স</p>
                    <div class="flex items-baseline gap-1 mt-2">
                        <span class="text-3xl font-bold text-indigo-400">৳</span>
                        <h1 id="user-balance" class="text-4xl font-black tracking-tight bg-gradient-to-r from-white to-slate-300 bg-clip-text text-transparent">0.00</h1>
                    </div>
                </div>

                <!-- Ticker Animation -->
                <div class="bg-amber-500/10 border border-amber-500/20 rounded-xl py-2 px-3 flex items-center gap-2 text-xs text-amber-400 font-medium">
                    <span>📢</span>
                    <marquee scrollamount="4">ALIF_INCOME_BD-এ স্বাগতম! • ভিডিও দেখে ইনকাম করুন প্রতি ভিডিও ১০ টাকা! • প্রতিদিন ২০টি কাজ!</marquee>
                </div>

                <!-- Dashboard Stats Grid -->
                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-slate-800/40 p-4 rounded-2xl border border-slate-800/80 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-blue-400 font-semibold text-xs">
                            ⚡ <span>আজকের টাস্ক</span>
                        </div>
                        <span id="stat-tasks" class="text-2xl font-bold text-slate-200 mt-2 font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/40 p-4 rounded-2xl border border-slate-800/80 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-purple-400 font-semibold text-xs">
                            👥 <span>মোট রেফার</span>
                        </div>
                        <span id="stat-refers" class="text-2xl font-bold text-slate-200 mt-2 font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/40 p-4 rounded-2xl border border-slate-800/80 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-cyan-400 font-semibold text-xs">
                            📹 <span>বিজ্ঞাপন দেখা</span>
                        </div>
                        <span id="stat-total-ads" class="text-2xl font-bold text-slate-200 mt-2 font-mono">0</span>
                    </div>
                    <div class="bg-slate-800/40 p-4 rounded-2xl border border-slate-800/80 flex flex-col justify-between">
                        <div class="flex items-center gap-2 text-emerald-400 font-semibold text-xs">
                            💰 <span>বোনাস ব্যালেন্স</span>
                        </div>
                        <span class="text-2xl font-bold text-slate-200 mt-2 font-mono">৳0.00</span>
                    </div>
                </div>
            </section>

            <!-- --- TAB 2: TASKS --- -->
            <section id="tasks" class="tab-content space-y-4">
                <div class="bg-slate-800/40 border border-slate-800 p-5 rounded-2xl text-center space-y-4">
                    <h2 class="text-base font-bold text-slate-200">বিজ্ঞাপন দেখে আয়</h2>
                    <p class="text-xs text-slate-400">প্রতি বিজ্ঞাপন সম্পূর্ণ দেখলে পাবেন ৳১০.০০ নিশ্চিত রিওয়ার্ড।</p>
                    
                    <div class="inline-block bg-indigo-500/10 text-indigo-400 font-bold px-4 py-1.5 rounded-xl text-xs border border-indigo-500/20">
                        💵 রিওয়ার্ড: ৳১০.০০ টাকা
                    </div>
                    
                    <div class="space-y-1.5 pt-2">
                        <div class="flex justify-between text-xs text-slate-400 px-1">
                            <span>আজকের টাস্ক লিমিট</span>
                            <span id="task-count-txt" class="font-bold text-indigo-400 font-mono">0 / 20</span>
                        </div>
                        <div class="w-full bg-slate-800 h-2.5 rounded-full overflow-hidden p-[2px]">
                            <div id="task-progress" class="bg-gradient-to-r from-blue-500 to-indigo-600 h-full w-0 rounded-full transition-all duration-300"></div>
                        </div>
                    </div>

                    <button onclick="watchVideoTask()" class="w-full bg-gradient-to-r from-red-500 to-rose-600 hover:from-red-600 hover:to-rose-700 text-white font-bold py-3 rounded-xl text-xs tracking-wide transition-all shadow-lg shadow-red-950/20">
                        বিজ্ঞাপন দেখুন
                    </button>
                </div>
            </section>

            <!-- --- TAB 3: REFER --- -->
            <section id="refer" class="tab-content space-y-4">
                <div class="bg-gradient-to-b from-slate-800 to-slate-900 border border-slate-800 text-white p-5 rounded-2xl space-y-4">
                    <div class="flex items-center gap-2">
                        🎁 <h2 class="text-base font-bold text-slate-200">বন্ধুদের আমন্ত্রণ জানান</h2>
                    </div>
                    <p class="text-xs text-slate-400 leading-relaxed">আপনার ইউনিক রেফারেল লিংকটি আপনার বন্ধুদের সাথে শেয়ার করুন। নতুন অ্যাকাউন্ট খুললেই পেয়ে যান আকর্ষনীয় বোনাস।</p>
                    
                    <div class="bg-cyan-500/10 border border-cyan-500/20 text-xs py-2.5 px-3 rounded-xl text-center text-cyan-400 font-bold">
                        😊 প্রতি রেফারে ৳৫০.০০ TAKA বোনাস
                    </div>

                    <div class="bg-slate-950 p-3 rounded-xl flex items-center justify-between border border-slate-800">
                        <input type="text" id="ref-link" readonly value="https://t.me/ALIF_INCOME_BDBot?start=userALIF" class="bg-transparent text-xs text-slate-400 outline-none flex-1 truncate font-mono">
                    </div>

                    <div class="grid grid-cols-2 gap-3 pt-2">
                        <button onclick="copyLink()" class="bg-slate-800 hover:bg-slate-700 text-slate-200 border border-slate-700 font-bold text-xs py-2.5 rounded-xl transition-all">📋 লিংক কপি করুন</button>
                        <button onclick="simulateReferral()" class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold text-xs py-2.5 rounded-xl transition-all">➕ ডেমো রেফার</button>
                    </div>
                </div>
            </section>

            <!-- --- TAB 4: WALLET --- -->
            <section id="withdraw" class="tab-content space-y-4">
                <div class="bg-slate-800/40 border border-slate-800/80 p-4 rounded-2xl space-y-3">
                    <div class="bg-blue-500/10 border border-blue-500/20 p-3 rounded-xl space-y-2 text-xs">
                        <h4 class="font-bold text-blue-400 flex items-center gap-1">⚠️ উত্তোলনের নিয়মাবলী</h4>
                        <ul class="space-y-1 text-slate-400 font-medium">
                            <li class="flex justify-between">• অন্তত ১০০টি বিজ্ঞাপন দেখা আবশ্যক: <span id="cond-ads" class="text-emerald-400 font-bold font-mono">0 / 100</span></li>
                            <li class="flex justify-between">• অথবা সফল ৪টি রেফার করা আবশ্যক: <span id="cond-refers" class="text-purple-400 font-bold font-mono">0 / 4</span></li>
                        </ul>
                    </div>

                    <!-- Input Fields -->
                    <div class="space-y-3 text-xs">
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">পেমেন্ট মেথড</label>
                            <select id="method" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-3 py-2.5 text-slate-200 outline-none focus:border-indigo-500 transition-all">
                                <option value="বিকাশ">বিকাশ</option>
                                <option value="নগদ">নগদ</option>
                            </select>
                        </div>
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">পার্সোনাল ওয়ালেট নম্বর</label>
                            <input type="text" id="account" placeholder="বিকাশ/নগদ নম্বর দিন" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-3 py-2.5 text-slate-200 outline-none focus:border-indigo-500 transition-all">
                        </div>
                        <div>
                            <label class="text-slate-400 font-bold block mb-1">উত্তোলনের পরিমাণ (৳)</label>
                            <input type="number" id="amount" placeholder="সর্বনিম্ন ৳১৩০০" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-3 py-2.5 text-slate-200 outline-none focus:border-indigo-500 transition-all font-mono">
                        </div>
                    </div>

                    <button onclick="handleWithdraw()" class="w-full bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-bold py-3 rounded-xl text-xs tracking-wider uppercase transition-all shadow-lg">
                        উত্তোলন সাবমিট করুন
                    </button>
                </div>
            </section>

            <!-- --- TAB 5: SUPPORT --- -->
            <section id="support" class="tab-content space-y-4">
                <div class="bg-slate-800/40 border border-slate-800 p-6 rounded-2xl text-center space-y-4">
                    <h2 class="text-base font-bold text-slate-200">হেল্প এবং সাপোর্ট সেন্টার</h2>
                    
                    <div class="bg-gradient-to-br from-slate-800 to-slate-950 border border-slate-800 rounded-2xl p-6 text-white max-w-sm mx-auto space-y-4 flex flex-col items-center">
                        <div class="w-12 h-12 bg-indigo-500/10 border border-indigo-500/20 text-indigo-400 rounded-full flex items-center justify-center">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12.003 21.112c-.114 0-.228-.02-.338-.061-4.08-1.493-7.665-4.48-10.37-8.63A11.758 11.758 0 0 1 0 5.602c0-.36.21-.69.54-.84a24.223 24.223 0 0 1 10.96-2.61c.17 0 .33.04.47.11l.03.01c.21.1.37.28.44.51.52 1.63 1.57 3.01 2.99 3.91 1.41.9 3.1 1.25 4.77.99a1.002 1.002 0 0 1 .94.57c2.31 4.75.98 10.42-3.1 12.35l-.01.01c-.13.06-.27.09-.43.09h-.03z"/></svg>
                        </div>
                        <div>
                            <h3 class="font-bold text-sm text-slate-200">অফিসিয়াল টেলিগ্রাম সাপোর্ট</h3>
                            <p class="text-xs text-slate-400 mt-1">যেকোনো সমস্যা ২৪ ঘণ্টার মধ্যে সমাধান করতে সরাসরি মেসেজ দিন</p>
                        </div>
                        <a href="https://t.me/Suupport7" target="_blank" class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold text-xs px-6 py-2.5 rounded-xl transition-all">
                            @Suupport7
                        </a>
                    </div>
                </div>
            </section>

        </main>

        <!-- ================= NAVIGATION BOTTOM BAR ================= -->
        <nav class="absolute bottom-0 left-0 right-0 bg-slate-900/90 backdrop-blur-md border-t border-slate-800/80 px-2 py-2 flex justify-around items-center z-50 shadow-xl">
            <button onclick="switchTab('home')" class="nav-btn text-cyan-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="home">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
                <span class="text-[10px] font-medium">হোম</span>
            </button>
            <button onclick="switchTab('tasks')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="tasks">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
                <span class="text-[10px] font-medium">টাস্ক</span>
            </button>
            <button onclick="switchTab('support')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="support">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.36 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                <span class="text-[10px] font-medium">সাপোর্ট</span>
            </button>
            <button onclick="switchTab('refer')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="refer">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                <span class="text-[10px] font-medium">রেফার</span>
            </button>
            <button onclick="switchTab('withdraw')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="withdraw">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"></path></svg>
                <span class="text-[10px] font-medium">ওয়ালেট</span>
            </button>
        </nav>
    </div>

    <!-- ================= BACKEND JS LOGIC ================= -->
    <script>
        let balance = 0.00; // আপনার রিকোয়েস্ট অনুযায়ী জিরো সেট করা হয়েছে
        let todayTasks = 0;
        let totalRefers = 0;
        let totalAdsWatched = 0;
        const maxDailyTasks = 20; // ২০ টি প্রতিদিনের ভিডিও লিমিট

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
            document.getElementById('stat-tasks').innerText = todayTasks;
            document.getElementById('stat-refers').innerText = totalRefers;
            document.getElementById('stat-total-ads').innerText = totalAdsWatched;
            document.getElementById('cond-ads').innerText = `${totalAdsWatched} / 100`;
            document.getElementById('cond-refers').innerText = `${totalRefers} / 4`;
            document.getElementById('task-count-txt').innerText = `${todayTasks} / ${maxDailyTasks}`;
        }

        function watchVideoTask() {
            if(todayTasks >= maxDailyTasks) {
                alert("আজকের সর্বোচ্চ ভিডিও লিমিট (২০/২০) শেষ হয়েছে!");
                return;
            }
            alert("বিজ্ঞাপন লোড হচ্ছে... ৫ সেকেন্ড অপেক্ষা করুন।");
            setTimeout(() => {
                balance += 10.00; // প্রতি ভিডিওতে ১০ টাকা
                todayTasks++;
                totalAdsWatched++;
                document.getElementById('task-progress').style.width = `${(todayTasks / maxDailyTasks) * 100}%`;
                updateUI();
                alert("সফলভাবে বিজ্ঞাপন দেখা সম্পন্ন হয়েছে! আপনার অ্যাকাউন্টে ৳১০ যোগ করা হয়েছে।");
            }, 1500);
        }

        function simulateReferral() {
            balance += 50.00; // প্রতি সফল রেফারে ৫০ টাকা বোনাস
            totalRefers++;
            updateUI();
            alert("সফল রেফারেল যুক্ত হয়েছে! বোনাস ৳৫০.০০ ব্যালেন্সে যোগ করা হলো।");
        }

        function copyLink() {
            const input = document.getElementById('ref-link');
            input.select();
            document.execCommand('copy');
            alert("ALIF_INCOME_BD রেফারেল লি
