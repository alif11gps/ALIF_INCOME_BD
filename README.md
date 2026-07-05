<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ADDS JOB CITY</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #f3f4f6;
            user-select: none;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="flex justify-center items-center min-h-screen bg-slate-100 p-2">

    <!-- App Container -->
    <div class="w-full max-w-md h-[92vh] bg-[#f8fafc] text-slate-800 rounded-3xl shadow-xl flex flex-col overflow-hidden relative border border-slate-200">
        
        <!-- ================= APP HEADER ================= -->
        <header class="bg-white border-b border-slate-100 px-4 py-3 flex items-center justify-between shrink-0 sticky top-0 z-50">
            <div class="flex items-center gap-2">
                <span class="text-xl font-bold text-slate-800 tracking-wide">ADDS JOB CITY 💼</span>
                <span class="text-blue-600 text-sm">✓</span>
            </div>
            <button class="text-slate-400 hover:text-slate-600">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path></svg>
            </button>
        </header>

        <!-- ================= MAIN CONTENT SCROLLABLE ================= -->
        <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 pb-24 space-y-4">
            
            <!-- --- TAB 1: হোম --- -->
            <section id="home" class="tab-content active space-y-4">
                <div class="flex items-center gap-3 bg-white p-3 rounded-2xl border border-slate-100">
                    <div class="w-12 h-12 rounded-full border-2 border-purple-500 overflow-hidden flex items-center justify-center bg-purple-100 text-purple-600 font-bold">
                        MD
                    </div>
                    <div>
                        <h3 class="font-bold text-slate-800 flex items-center gap-1">MD <span class="text-purple-600 text-xs">✓</span></h3>
                        <p class="text-[11px] text-slate-400">মেম্বার আইডি: #00000</p>
                    </div>
                </div>

                <!-- Main Balance Card -->
                <div class="bg-gradient-to-br from-indigo-500 to-purple-600 rounded-3xl p-6 text-white shadow-md relative overflow-hidden">
                    <p class="text-xs font-medium text-indigo-100 tracking-wider">মোট ব্যালেন্স</p>
                    <h1 class="text-4xl font-bold mt-2 flex items-baseline gap-1">
                        <span class="text-2xl font-medium">৳</span>
                        <span id="user-balance">0.00</span>
                    </h1>
                </div>

                <!-- Info Notice Slider Ticker -->
                <div class="bg-white border border-slate-100 p-3 rounded-xl text-xs text-slate-600 flex items-center gap-2 overflow-hidden">
                    <span class="shrink-0">🎉</span>
                    <marquee class="font-medium" scrollamount="4">Alif*** সবেমাত্র ৳১৫০০ উত্তোলন করেছেন! নতুন কাজের আপডেট পেতে আমাদের সাথে থাকুন।</marquee>
                </div>

                <!-- Dashboard Statistics Grid Layout -->
                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm relative">
                        <div class="text-purple-500 mb-2">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                        </div>
                        <div class="text-slate-400 font-medium text-xs">মোট টাস্ক</div>
                        <span id="stat-tasks" class="text-xl font-bold text-slate-800 mt-1 block">0</span>
                    </div>
                    
                    <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm">
                        <div class="text-blue-500 mb-2">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                        </div>
                        <div class="text-slate-400 font-medium text-xs">মোট রেফার</div>
                        <span id="stat-refers" class="text-xl font-bold text-slate-800 mt-1 block">0</span>
                    </div>

                    <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm">
                        <div class="text-indigo-500 mb-2">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 10l4.553-2.276A1 1 0 0121 8.618v6.764a1 1 0 01-1.447.894L15 14M5 18h8a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v8a2 2 0 002 2z"></path></svg>
                        </div>
                        <div class="text-slate-400 font-medium text-xs">বিজ্ঞাপন দেখা</div>
                        <span id="stat-total-ads" class="text-xl font-bold text-slate-800 mt-1 block">0</span>
                    </div>

                    <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm">
                        <div class="text-emerald-500 mb-2">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                        </div>
                        <div class="text-slate-400 font-medium text-xs">বোনাস ব্যালেন্স</div>
                        <span id="stat-refer-bonus" class="text-xl font-bold text-slate-800 mt-1 block">৳0.00</span>
                    </div>
                </div>
            </section>

            <!-- --- TAB 2: কাজ --- -->
            <section id="tasks" class="tab-content space-y-4">
                <div class="bg-white border border-slate-100 p-5 rounded-3xl text-center shadow-sm space-y-4">
                    <div>
                        <h2 class="text-base font-bold text-slate-800">বিজ্ঞাপন দেখুন</h2>
                        <p class="text-xs text-slate-400 mt-1">প্রতি বিজ্ঞাপন দেখে ৳১০.০০ ইনকাম করুন</p>
                    </div>
                    
                    <div class="inline-flex bg-blue-50 text-blue-600 font-bold px-4 py-1.5 rounded-full text-xs border border-blue-100 items-center gap-1">
                        💵 রিওয়ার্ড: ৳১০.০০টাকা
                    </div>
                    
                    <div class="space-y-1 pt-1 text-left">
                        <div class="flex justify-between text-xs text-slate-500 px-1">
                            <span>আজকের সম্পন্ন</span>
                            <span id="task-count-txt" class="font-bold text-slate-700">0 / 20</span>
                        </div>
                        <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden">
                            <div id="task-progress" class="bg-red-500 h-full w-0 rounded-full transition-all duration-300"></div>
                        </div>
                    </div>

                    <button onclick="watchVideoTask()" class="w-full bg-red-500 hover:bg-red-600 text-white font-bold py-3 rounded-xl text-sm shadow-md transition-all">
                        বিজ্ঞাপন দেখুন
                    </button>
                </div>
            </section>

            <!-- --- TAB 3: সাপোর্ট --- -->
            <section id="support" class="tab-content space-y-4">
                <div class="bg-white border border-slate-100 p-5 rounded-3xl text-center shadow-sm space-y-4">
                    <h2 class="text-base font-bold text-slate-800 text-left">সাহায্য প্রয়োজন?</h2>
                    
                    <div class="bg-red-500 text-white p-6 rounded-2xl space-y-3">
                        <div class="w-12 h-12 bg-white/20 rounded-full flex items-center justify-center mx-auto text-xl">✈️</div>
                        <h3 class="font-bold text-base">কাস্টমার সাপোর্ট</h3>
                        <p class="text-xs text-red-100">যেকোনো সমস্যা সমাধানের জন্য আমাদের সাথে যোগাযোগ করুন</p>
                        
                        <a href="https://t.me/Suupport7" target="_blank" class="inline-block bg-white/20 hover:bg-white/30 text-white font-medium text-xs px-6 py-2.5 rounded-full transition-all">
                            @Suupport7
                        </a>
                    </div>
                </div>
            </section>

            <!-- --- TAB 4: রেফার --- -->
            <section id="refer" class="tab-content space-y-4">
                <div class="bg-[#1e2538] text-slate-100 p-5 rounded-3xl space-y-4 shadow-sm">
                    <h2 class="text-base font-bold flex items-center gap-2">🎁 বন্ধুকে রেফার করুন এবং আয় করুন</h2>
                    <p class="text-xs text-slate-400 leading-relaxed">আপনার রেফার লিংকটি শেয়ার করুন এবং আপনার বন্ধুদের আমন্ত্রণ করুন। আপনার বন্ধু সাইন আপ করলে আপনি ৳৫০.০০ বোনাস পাবেন।</p>
                    
                    <div class="bg-slate-800/60 text-xs py-2 px-3 rounded-xl text-slate-300 font-medium inline-block">
                        😊 প্রতি রেফারে ৳৫০.০০ টাকা বোনাস
                    </div>

                    <div class="bg-slate-900 p-3 rounded-xl flex items-center justify-between border border-slate-800">
                        <input type="text" id="ref-link" readonly value="https://t.me/AddsJobCityBot?start=user" class="bg-transparent text-xs text-slate-400 outline-none flex-1 truncate">
                        <button onclick="copyLink()" class="p-1.5 bg-gradient-to-r from-pink-500 to-purple-500 rounded-lg text-white text-xs">📋</button>
                    </div>

                    <div class="grid grid-cols-2 gap-3 pt-2">
                        <button onclick="copyLink()" class="bg-gradient-to-r from-pink-500 to-purple-500 font-bold text-xs py-2.5 rounded-xl transition-all">লিংক কপি করুন</button>
                        <button onclick="simulateReferral()" class="bg-indigo-600 hover:bg-indigo-700 font-bold text-xs py-2.5 rounded-xl transition-all">➕ ডেমো রেফার</button>
                    </div>
                </div>
            </section>

            <!-- --- TAB 5: ওয়ালেট --- -->
            <section id="withdraw" class="tab-content space-y-4">
                <div class="bg-white border border-slate-200 p-5 rounded-3xl space-y-4 shadow-sm">
                    
                    <!-- Withdrawal Conditions Box -->
                    <div class="bg-blue-50 border border-blue-100 p-4 rounded-xl space-y-2 text-xs">
                        <h4 class="font-bold text-blue-700 flex items-center gap-1">⚠️ উত্তোলনের শর্তাবলী</h4>
                        <p class="text-slate-600">উত্তোলনের জন্য নিচের শর্তটি পূরণ করতে হবে:</p>
                        <ul class="space-y-1 text-slate-600 font-medium">
                            <li>• অন্তত <span class="text-blue-700 font-bold">১৫০টি</span> বিজ্ঞাপন দেখতে হবে।</li>
                            <li class="bg-white/60 p-1.5 rounded mt-1 flex justify-between">
                                <span>আপনার বর্তমান সম্পন্ন:</span>
                                <span id="cond-ads" class="text-emerald-600 font-bold">0 / 150</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Withdrawal Fields -->
                    <div class="space-y-3 text-xs">
                        <div>
                            <label class="text-slate-500 font-bold block mb-1">পেমেন্ট মেথড</label>
                            <select id="method" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-2.5 text-slate-700 outline-none focus:border-blue-500">
                                <option value="বিকার">বিকাশ</option>
                                <option value="নগদ">নগদ</option>
                            </select>
                        </div>
                        <div>
                            <label class="text-slate-500 font-bold block mb-1">উত্তোলন নাম্বার/Binance ID</label>
                            <input type="text" id="account" placeholder="আপনার ফোন নম্বর বা অ্যাড্রেস লিখুন" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-2.5 text-slate-700 outline-none focus:border-blue-500">
                        </div>
                        <div>
                            <label class="text-slate-500 font-bold block mb-1">পরিমাণ (৳)</label>
                            <input type="number" id="amount" value="1500" readonly class="w-full bg-slate-100 border border-slate-200 rounded-xl px-3 py-2.5 text-slate-400 outline-none cursor-not-allowed font-bold">
                        </div>
                    </div>

                    <button onclick="handleWithdraw()" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 rounded-xl text-sm transition-all shadow-md">
                        উত্তোলন করুন
                    </button>
                </div>
            </section>

        </main>

        <!-- ================= BOTTOM NAVIGATION BAR ================= -->
        <nav class="absolute bottom-0 left-0 right-0 bg-white border-t border-slate-100 py-2 flex justify-around items-center z-50">
            <!-- হোম -->
            <button onclick="switchTab('home')" class="nav-btn text-purple-600 flex flex-col items-center gap-0.5 w-14" data-tab="home">
                <span class="text-lg">🏠</span>
                <span class="text-[10px] font-bold">হোম</span>
            </button>
            <!-- কাজ -->
            <button onclick="switchTab('tasks')" class="nav-btn text-slate-400 flex flex-col items-center gap-0.5 w-14" data-tab="tasks">
                <span class="text-lg">📋</span>
                <span class="text-[10px] font-bold">কাজ</span>
            </button>
            <!-- সাপোর্ট -->
            <button onclick="switchTab('support')" class="nav-btn text-slate-400 flex flex-col items-center gap-0.5 w-14" data-tab="support">
                <span class="text-lg">🎧</span>
                <span class="text-[10px] font-bold">সাপোর্ট</span>
            </button>
            <!-- রেফার -->
            <button onclick="switchTab('refer')" class="nav-btn text-slate-400 flex flex-col items-center gap-0.5 w-14" data-tab="refer">
                <span class="text-lg">👥</span>
                <span class="text-[10px] font-bold">রেফার</span>
            </button>
            <!-- ওয়ালেট -->
            <button onclick="switchTab('withdraw')" class="nav-btn text-slate-400 flex flex-col items-center gap-0.5 w-14" data-tab="withdraw">
                <span class="text-lg">💳</span>
                <span class="text-[10px] font-bold">ওয়ালেট</span>
            </button>
        </nav>
    </div>

    <!-- ================= SYSTEM LOGIC SCRIPTS ================= -->
    <script>
        let balance = 0.00; 
        let todayTasks = 0;
        let totalRefers = 0;
        let totalAdsWatched = 0;
        let referBonus = 0.00;
        const maxDailyTasks = 20;

        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.replace('text-purple-600', 'text-slate-400');
            });
            const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
            if(activeBtn) activeBtn.classList.replace('text-slate-400', 'text-purple-600');
        }

        function updateUI() {
            document.getElementById('user-balance').innerText = balance.toFixed(2);
            document.getElementById('stat-tasks').innerText = todayTasks;
            document.getElementById('stat-refers').innerText = totalRefers;
            document.getElementById('stat-total-ads').innerText = totalAdsWatched;
            document.getElementById('stat-refer-bonus').innerText = `৳${referBonus.toFixed(2)}`;
            
            document.getElementById('cond-ads').innerText = `${totalAdsWatched} / 150`; 
            document.getElementById('task-count-txt').innerText = `${todayTasks} / ${maxDailyTasks}`;
        }

        function watchVideoTask() {
            if(todayTasks >= maxDailyTasks) {
                alert("আজকের লিমিট (২০/২০) শেষ হয়েছে!");
                return;
            }
            alert("বিজ্ঞাপন লোড হচ্ছে... ৫ সেকেন্ড অপেক্ষা করুন।");
            setTimeout(() => {
                balance += 10.00; 
                todayTasks++;
                totalAdsWatched++;
                document.getElementById('task-progress').style.width = `${(todayTasks / maxDailyTasks) * 100}%`;
                updateUI();
                alert("সফলভাবে ভিডিও দেখা সম্পন্ন! ওয়ালেটে ৳১০ যোগ হয়েছে।");
            }, 1000);
        }

        function simulateReferral() {
            balance += 50.00; 
            referBonus += 50.00;
            totalRefers++;
            updateUI();
            alert("১টি রেফার সফল হয়েছে! ৳৫০ বোনাস দেওয়া হয়েছে।");
        }

        function copyLink() {
            const input = document.getElementById('ref-link');
            input.select();
            document.execCommand('copy');
            alert("রেফারেল লিংক কপি হয়েছে!");
        }

        function handleWithdraw() {
            const account = document.getElementById('account').value;
            const amount = 1500; 
            
            if(!account) {
                alert("আপনার অ্যাকাউন্ট নম্বরটি লিখুন!");
                return;
            }
            if(balance < amount) {
                alert("উত্তোলনের জন্য আপনার একাউন্টে ন্যূনতম ৳১৫০০ টাকা থাকতে হবে।");
                return;
            }
            if(totalAdsWatched < 150) {
                alert(`শর্ত অপূর্ণ! উত্তোলন করার আগে আপনাকে কমপক্ষে ১৫০টি বিজ্ঞাপন দেখতে হবে। (আপনার বর্তমান দেখা: ${totalAdsWatched}টি)`);
                return;
            }
            
            balance -= amount;
            updateUI();
            alert(`আপনার ৳${amount} টাকা উত্তোলনের রিকোয়েস্টটি সফল হয়েছে।`);
        }
    </script>
</body>
</html>
