<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ALIF_INCOME_BD</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f1f5f9;
            color: #1e293b;
            -webkit-tap-highlight-color: transparent;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="max-w-md mx-auto min-h-screen bg-slate-50 flex flex-col relative overflow-x-hidden select-none">

    <!-- Top App Bar (Fixed) -->
    <header class="sticky top-0 z-50 bg-white border-b border-slate-200 px-4 py-3 flex justify-between items-center shadow-sm">
        <div class="flex items-center gap-2">
            <span class="text-xl font-bold text-slate-800 tracking-wide">ALIF_INCOME_BD</span>
            <span class="text-emerald-500 text-xs">✓</span>
        </div>
        <div class="flex items-center gap-2 text-slate-600">
            <svg class="w-5 h-5 animate-pulse text-amber-500" fill="currentColor" viewBox="0 0 20 20"><path d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6zM10 18a3 3 0 01-3-3h6a3 3 0 01-3 3z"></path></svg>
        </div>
    </header>

    <!-- Main Dynamic Container -->
    <main class="flex-1 p-4 pb-24 overflow-y-auto no-scrollbar">
        
        <!-- Tab: HOME -->
        <section id="home" class="tab-content active space-y-4">
            <!-- User Profile Section -->
            <div class="flex items-center justify-between bg-white p-3 rounded-2xl shadow-sm border border-slate-100">
                <div class="flex items-center gap-3">
                    <div class="w-12 h-12 bg-gradient-to-tr from-purple-500 to-indigo-600 rounded-full border-2 border-white shadow flex items-center justify-center text-white font-bold text-lg">MD</div>
                    <div>
                        <h3 class="font-bold text-slate-800 flex items-center gap-1">MD <span class="text-blue-500 text-xs">✓</span></h3>
                        <p class="text-[11px] text-slate-400 font-medium">Premium Member</p>
                    </div>
                </div>
                <button class="p-2 text-slate-400 hover:text-slate-600"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path></svg></button>
            </div>

            <!-- Balance Card -->
            <div class="bg-gradient-to-r from-purple-500 to-indigo-500 rounded-3xl p-6 text-white shadow-md relative overflow-hidden">
                <p class="text-xs text-purple-100 font-medium tracking-wide">মোট ব্যালেন্স</p>
                <h1 class="text-4xl font-black mt-1 tracking-tight">৳ <span id="user-balance">0.00</span></h1>
                <div class="w-24 h-24 bg-white/10 rounded-full absolute -right-6 -bottom-6 blur-xl"></div>
            </div>

            <!-- Live Withdrawal Ticker / Notice -->
            <div class="bg-amber-50 border border-amber-200 text-amber-800 text-xs py-2 px-3 rounded-xl flex items-center gap-2 shadow-sm">
                <span>🎉</span>
                <marquee class="font-medium" scrollamount="4">Aka*** সবেমাত্র ৳৯৬৭০ উত্তোলন করেছেন! • MD Alife*** সবেমাত্র ২০ জন রেফার সম্পন্ন করেছেন!</marquee>
            </div>

            <!-- Statistics Grid -->
            <div class="grid grid-cols-2 gap-3">
                <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-100 flex flex-col gap-1">
                    <span class="text-purple-500"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg></span>
                    <span class="text-xs text-slate-400 font-medium mt-1">মোট টাস্ক</span>
                    <span class="text-lg font-bold text-slate-800" id="stat-tasks">0</span>
                </div>
                <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-100 flex flex-col gap-1">
                    <span class="text-indigo-500"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg></span>
                    <span class="text-xs text-slate-400 font-medium mt-1">মোট রেফার</span>
                    <span class="text-lg font-bold text-slate-800" id="stat-refers">0 <span class="text-xs text-slate-400 font-normal">/20</span></span>
                </div>
                <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-100 flex flex-col gap-1">
                    <span class="text-rose-500"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 10l4.553-2.276A1 1 0 0121 8.618v6.764a1 1 0 01-1.447.894L15 14M5 18h8a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v8a2 2 0 002 2z"></path></svg></span>
                    <span class="text-xs text-slate-400 font-medium mt-1">বিজ্ঞাপন দেখা</span>
                    <span class="text-lg font-bold text-slate-800" id="stat-ads">0</span>
                </div>
                <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-100 flex flex-col gap-1">
                    <span class="text-emerald-500"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg></span>
                    <span class="text-xs text-slate-400 font-medium mt-1">বোনাস ব্যালেন্স</span>
                    <span class="text-lg font-bold text-slate-800">৳0.00</span>
                </div>
            </div>
        </section>

        <!-- Tab: TASKS (কাজ) -->
        <section id="tasks" class="tab-content space-y-4">
            <div class="bg-indigo-50 border border-indigo-100 p-5 rounded-3xl text-center shadow-sm">
                <h2 class="text-lg font-bold text-slate-800">বিজ্ঞাপন দেখুন</h2>
                <p class="text-xs text-slate-500 mt-1">প্রতি বিজ্ঞাপন দেখে ৳১০.০০ ইনকাম করুন</p>
                
                <div class="my-5 inline-block bg-indigo-100 text-indigo-700 font-bold px-4 py-2 rounded-xl text-sm shadow-sm border border-indigo-200">
                    💵 রিওয়ার্ড: ৳১০.০০ টাকা
                </div>

                <div class="space-y-1 mb-4 max-w-xs mx-auto">
                    <div class="flex justify-between text-[11px] text-slate-500 font-bold">
                        <span>আজকের সম্পন্ন</span>
                        <span id="task-count-text">0 / 15</span>
                    </div>
                    <div class="w-full bg-slate-200 h-2 rounded-full overflow-hidden">
                        <div id="task-progress" class="bg-indigo-600 h-full w-0 transition-all duration-300"></div>
                    </div>
                </div>

                <button onclick="watchAdVideo()" class="w-full max-w-xs bg-rose-500 hover:bg-rose-600 text-white font-bold py-3.5 rounded-2xl shadow-md transition-all active:scale-95 tracking-wide text-sm">
                    বিজ্ঞাপন দেখুন
                </button>
            </div>
        </section>

        <!-- Tab: SUPPORT (সাপোর্ট) -->
        <section id="support" class="tab-content space-y-4">
            <div class="bg-white p-6 rounded-3xl shadow-sm border border-slate-100 text-center space-y-4">
                <h2 class="text-xl font-bold text-slate-800">সাহায্য প্রয়োজন?</h2>
                <p class="text-xs text-slate-500 leading-relaxed">যেকোনো সমস্যা সমাধানের জন্য আমাদের কাস্টমার সাপোর্টের সাথে যোগাযোগ করুন।</p>
                
                <div class="bg-gradient-to-b from-rose-500 to-rose-600 rounded-2xl p-6 text-white max-w-xs mx-auto shadow-md space-y-3 flex flex-col items-center">
                    <div class="w-12 h-12 bg-white/20 rounded-full flex items-center justify-center shadow-inner">
                        <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24"><path d="M12.003 21c-5.523 0-10-4.477-10-10s4.477-10 10-10 10 4.477 10 10-4.477 10-10 10zm-1.897-7.984l.257 2.762c.033.354.331.622.687.622h1.91c.356 0 .654-.268.687-.622l.257-2.762a.753.753 0 00-.749-.823h-2.299a.753.753 0 00-.751.823zm.459-5.918c-.024.463.155.914.494 1.232.338.317.798.494 1.268.484.469-.01 1.104-.197 1.428-.525.323-.328.488-.785.452-1.248-.073-.925-.85-1.641-1.782-1.625-.933.016-1.787.757-1.86 1.682z"/></svg>
                    </div>
                    <h3 class="font-bold text-lg tracking-wide">কাস্টমার সাপোর্ট</h3>
                    <a href="https://t.me/Suupport7" target="_blank" class="bg-white/20 hover:bg-white/30 backdrop-blur text-white text-xs font-bold px-5 py-2 rounded-xl transition-all shadow border border-white/10">
                        @Suupport7
                    </a>
                </div>
            </div>
        </section>

        <!-- Tab: REFER (রেফার) -->
        <section id="refer" class="tab-content space-y-4">
            <div class="bg-slate-900 text-white p-6 rounded-3xl shadow-lg border border-slate-800 space-y-4 relative overflow-hidden">
                <div class="flex items-center gap-3">
                    <span class="text-pink-400 text-xl">🎁</span>
                    <h2 class="text-base font-bold">বন্ধুকে রেফার করুন এবং আয় করুন</h2>
                </div>
                <p class="text-xs text-slate-300 leading-relaxed">আপনার রেফার লিংকটি শেয়ার করুন এবং আপনার বন্ধুদের আমন্ত্রণ করুন। আপনার বন্ধু সাইন আপ করলে আপনি <span class="text-amber-400 font-bold">৳৫০.০০ টাকা</span> বোনাস পাবেন।</p>
                
                <button class="bg-blue-600/20 text-blue-400 text-xs font-bold py-2 px-4 rounded-xl border border-blue-500/30 w-full text-left flex justify-between items-center">
                    <span>প্রতি রেফারে ৳৫০.০০ টাকা বোনাস</span>
                    <span>✓</span>
                </button>

                <div class="relative bg-slate-950 p-3.5 rounded-xl border border-slate-800 flex items-center justify-between gap-2">
                    <input type="text" id="ref-link" readonly value="https://t.me/AlifIncomeBdBot?start=user77" class="bg-transparent text-xs text-slate-400 outline-none flex-1 truncate select-all">
                    <button onclick="copyRefLink()" class="p-2 bg-pink-600 hover:bg-pink-700 text-white rounded-lg shadow transition-all active:scale-95">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7v8a2 2 0 002 2h6a2 2 0 002-2V7a2 2 0 00-2-2h-6a2 2 0 00-2 2zM8 7H6a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2v-2"></path></svg>
                    </button>
                </div>

                <div class="flex gap-2 pt-2">
                    <button onclick="simulateFakeRefer()" class="flex-1 bg-gradient-to-r from-purple-600 to-indigo-600 text-white font-bold text-xs py-3 rounded-xl shadow active:scale-95 transition-all">
                        সিমুলেট রেফার (+১)
                    </button>
                </div>
            </div>
        </section>

        <!-- Tab: WALLET (ওয়ালেট) -->
        <section id="withdraw" class="tab-content space-y-4">
            <div class="bg-white p-5 rounded-3xl shadow-sm border border-slate-100 space-y-4">
                
                <!-- Terms / Condition Box -->
                <div class="bg-blue-50 border border-blue-200 p-4 rounded-2xl text-xs space-y-2">
                    <h4 class="font-bold text-blue-900 flex items-center gap-1.5">
                        ⚠️ উত্তোলনের শর্তাবলী
                    </h4>
                    <p class="text-blue-800 leading-relaxed">উত্তোলনের জন্য নিচের যেকোনো একটি শর্ত পূরণ করতে হবে:</p>
                    <ul class="space-y-1 text-blue-700 font-medium list-disc pl-4">
                        <li>অন্তত ১০০টি বিজ্ঞাপন দেখতে হবে।</li>
                        <li>অথবা অন্তত <span class="text-blue-900 font-bold">২০টি</span> সফল রেফার করতে হবে। (আপনার বর্তমান: <span id="current-refers-status" class="font-bold text-rose-600">0/20</span>)</li>
                    </ul>
                </div>

                <!-- Form Fields -->
                <div class="space-y-3">
                    <div>
                        <label class="text-[11px] font-bold text-slate-400 uppercase tracking-wider block mb-1">পেমেন্ট মেথড</label>
                        <select id="withdraw-method" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-3 text-xs text-slate-700 font-semibold outline-none focus:border-indigo-500">
                            <option value="bKash">বিকাশ</option>
                            <option value="Nagad">নগদ</option>
                            <option value="Rocket">রকেট</option>
                        </select>
                    </div>

                    <div>
                        <label class="text-[11px] font-bold text-slate-400 uppercase tracking-wider block mb-1">উত্তোলন নাম্বার/Binance ID</label>
                        <input type="number" id="withdraw-account" placeholder="আপনার ফোন নম্বর বা অ্যাড্রেস লিখুন" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-3 text-xs text-slate-700 outline-none focus:border-indigo-500">
                    </div>

                    <div>
                        <label class="text-[11px] font-bold text-slate-400 uppercase tracking-wider block mb-1">পরিমাণ (৳)</label>
                        <input type="number" id="withdraw-amount" placeholder="ন্যূনতম ৳১৩০০" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-3 text-xs text-slate-700 outline-none focus:border-indigo-500">
                    </div>
                </div>

                <button onclick="processWithdrawalRequest()" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold text-xs py-3.5 rounded-xl shadow-md transition-all active:scale-95 uppercase tracking-wider">
                    উত্তোলন করুন
                </button>
            </div>
        </section>

    </main>

    <!-- Bottom Navigation Bar (Fixed & Locked) -->
    <nav class="fixed bottom-0 left-0 right-0 max-w-md mx-auto bg-white/95 backdrop-blur border-t border-slate-200/80 px-2 py-2 flex justify-around items-center z-50 rounded-t-3xl shadow-[0_-4px_20px_rgba(0,0,0,0.04)]">
        <button onclick="switchTab('home')" class="nav-btn text-indigo-600 flex flex-col items-center gap-1 py-1 w-14" data-tab="home">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[10px] font-bold">হোম</span>
        </button>
        <button onclick="switchTab('tasks')" class="nav-btn text-slate-400 flex flex-col items-center gap-1 py-1 w-14" data-tab="tasks">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
            <span class="text-[10px] font-bold">কাজ</span>
        </button>
        <button onclick="switchTab('support')" class="nav-btn text-slate-400 flex flex-col items-center gap-1 py-1 w-14" data-tab="support">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
            <span class="text-[10px] font-bold">সাপোর্ট</span>
        </button>
        <button onclick="switchTab('refer')" class="nav-btn text-slate-400 flex flex-col items-center gap-1 py-1 w-14" data-tab="refer">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
            <span class="text-[10px] font-bold">রেফার</span>
        </button>
        <button onclick="switchTab('withdraw')" class="nav-btn text-slate-400 flex flex-col items-center gap-1 py-1 w-14" data-tab="withdraw">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"></path></svg>
            <span class="text-[10px] font-bold">ওয়ালেট</span>
        </button>
    </nav>

    <script>
        let currentBalance = 0;
        let totalRefers = 0;
        let totalTasks = 0;
        let totalAdsWatched = 0;
        const requiredRefers = 20;

        // --- Tab Management ---
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('text-indigo-600');
                btn.classList.add('text-slate-400');
            });
            
            document.getElementById(tabId).classList.add('active');
            const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
            if(activeBtn) {
                activeBtn.classList.remove('text-slate-400');
                activeBtn.classList.add('text-indigo-600');
            }
        }

        // --- Copy Link Mechanism ---
        function copyRefLink() {
            const linkInput = document.getElementById("ref-link");
            linkInput.select();
            linkInput.setSelectionRange(0, 99999);
            navigator.clipboard.writeText(linkInput.value);
            alert("রেফার লিংক কপি হয়েছে!");
        }

        // --- Task Simulation ---
        function watchAdVideo() {
            if(totalTasks >= 15) {
                alert("আজকের সর্বোচ্চ ১৫টি বিজ্ঞাপনের সীমা পূর্ণ হয়েছে!");
                return;
            }
            alert("বিজ্ঞাপন লোড হচ্ছে... অনুগ্রহ করে ৫ সেকেন্ড অপেক্ষা করুন।");
            setTimeout(() => {
                totalTasks += 1;
                totalAdsWatched += 1;
                currentBalance += 10.00; // ৳10 per ad watch
                
                // Update UI
                document.getElementById('user-balance').innerText = currentBalance.toFixed(2);
                document.getElementById('stat-tasks').innerText = totalTasks;
                document.getElementById('stat-ads').innerText = totalAdsWatched;
                document.getElementById('task-count-text').innerText = `${totalTasks} / 15`;
                
                let percent = (totalTasks / 15) * 100;
                document.getElementById('task-progress').style.width = `${percent}%`;
                
                alert("বিজ্ঞাপন দেখা সফল হয়েছে! আপনার ব্যালেন্সে ৳১০.০০ যোগ করা হয়েছে।");
            }, 2000);
        }

        // --- Fake Refer Simulation ---
        function simulateFakeRefer() {
            if (totalRefers < requiredRefers) {
                totalRefers += 1;
                currentBalance += 50.00; // ৳50 per refer as requested
                
                // Sync UI
                document.getElementById('user-balance').innerText = currentBalance.toFixed(2);
                document.getElementById('stat-refers').innerHTML = `${totalRefers} <span class="text-xs text-slate-400 font-normal">/20</span>`;
                document.getElementById('current-refers-status').innerText = `${totalRefers}/20`;
                
                if(totalRefers >= requiredRefers) {
                    document.getElementById('current-refers-status').className = "font-bold text-emerald-600";
                }
                alert(`সফল রেফার! প্রতি রেফারে ৳৫০ বোনাস যুক্ত হয়েছে।`);
            } else {
                alert("আপনি ইতিমধ্যে ২০টি সফল রেফারের টার্গেট পূর্ণ করেছেন!");
            }
        }

        // --- Withdrawal System Logic ---
        function processWithdrawalRequest() {
            const account = document.getElementById('withdraw-account').value;
            const amount = parseFloat(document.getElementById('withdraw-amount').value);
            const method = document.getElementById('withdraw-method').value;

            // Check refer milestone
            if(totalRefers < requiredRefers) {
                alert(`উত্তোলন ব্যর্থ! টাকা তুলতে হলে আপনাকে অবশ্যই অন্তত ২০ জনকে সফল রেফার করতে হবে। (বর্তমান রেফার: ${totalRefers}টি)`);
                return;
            }

            if(!account || account.trim() === "") {
                alert("অনুগ্রহ করে আপনার অ্যাকাউন্ট নম্বর প্রদান করুন।");
                return;
            }

            if(isNaN(amount) || amount < 1300) {
                alert("উত্তোলন ব্যর্থ! সর্বনিম্ন ডাউনলিংক বা উত্তোলনের পরিমাণ ৳১৩০০ টাকা হতে হবে।");
                return;
            }

            if(amount > currentBalance) {
                alert("আপনার অ্যাকাউন্টে পর্যাপ্ত ব্যালেন্স নেই!");
                return;
            }

            // Success Execution
            alert(`আপনার ৳${amount} টাকা ${method}-এ উত্তোলনের অনুরোধটি সফলভাবে গ্রহণ করা হয়েছে। ২৪ ঘণ্টার মধ্যে পেমেন্ট সম্পন্ন করা হবে।`);
            currentBalance -= amount;
            document.getElementById('user-balance').innerText = currentBalance.toFixed(2);
            document.getElementById('withdraw-account').value = "";
            document.getElementById('withdraw-amount').value = "";
        }
    </script>
</body>
</html>
