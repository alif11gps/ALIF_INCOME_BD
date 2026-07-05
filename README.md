<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ALIF_INCOME_BD - Premium Earning Platform</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@400;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #030712;
            color: #f3f4f6;
            -webkit-tap-highlight-color: transparent;
        }
        .heading-font {
            font-family: 'Space Grotesk', sans-serif;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        
        /* Futuristic Glassmorphism */
        .premium-card {
            background: linear-gradient(135deg, rgba(17, 24, 39, 0.7) 0%, rgba(31, 41, 55, 0.5) 100%);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.06);
            box-shadow: 0 20px 40px -15px rgba(0,0,0,0.5);
        }
        
        /* Splash Screen Fade Out Animation */
        @keyframes fadeOut {
            to { opacity: 0; visibility: hidden; }
        }
        .splash-active {
            animation: fadeOut 0.6s ease-in-out forwards;
            animation-delay: 2.5s;
        }
    </style>
</head>
<body class="flex flex-col min-h-screen max-w-md mx-auto relative bg-[#030712] shadow-2xl overflow-x-hidden">

    <!-- ================= SPLASH SCREEN LOGO ================= -->
    <div id="splash-screen" class="fixed inset-0 max-w-md mx-auto bg-[#030712] z-[100] flex flex-col items-center justify-center p-6 splash-active">
        <div class="relative flex flex-col items-center space-y-6">
            <!-- Animated Tech Logo Box -->
            <div class="w-24 h-24 relative flex items-center justify-center rounded-3xl bg-gradient-to-tr from-cyan-500 via-indigo-500 to-fuchsia-500 animate-spin-slow shadow-2xl shadow-indigo-500/30">
                <div class="absolute inset-[3px] bg-[#030712] rounded-[21px] flex items-center justify-center">
                    <span class="text-3xl font-black heading-font bg-gradient-to-r from-cyan-400 to-fuchsia-400 bg-clip-text text-transparent">A_B</span>
                </div>
            </div>
            <!-- Brand Text Showcase -->
            <div class="text-center">
                <h1 class="text-2xl font-black tracking-widest heading-font bg-gradient-to-r from-white via-slate-200 to-slate-400 bg-clip-text text-transparent">ALIF_INCOME_BD</h1>
                <p class="text-xs text-indigo-400/80 tracking-[0.2em] uppercase mt-2 font-semibold">Next-Gen Earning Hub</p>
            </div>
            <!-- Progress Loader Bar -->
            <div class="w-32 bg-slate-900 h-1 rounded-full overflow-hidden p-[1px]">
                <div class="bg-gradient-to-r from-cyan-500 to-fuchsia-500 h-full w-full rounded-full origin-left animate-[transform_2.2s_ease-in-out]"></div>
            </div>
        </div>
    </div>


    <!-- ================= MAIN APP HEADER ================= -->
    <header class="sticky top-0 z-50 bg-[#030712]/80 backdrop-blur-xl border-b border-slate-900 px-5 py-4 flex justify-between items-center">
        <div class="flex items-center gap-2.5">
            <span class="text-xl font-black heading-font tracking-wider bg-gradient-to-r from-cyan-400 via-indigo-400 to-fuchsia-400 bg-clip-text text-transparent">ALIF_INCOME_BD</span>
            <span class="flex h-2 w-2 relative">
                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
            </span>
        </div>
        <div class="flex items-center gap-3">
            <button onclick="switchTab('support')" class="relative p-2 rounded-xl bg-slate-900 border border-slate-800 text-slate-400 hover:text-cyan-400 transition-all">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
            </button>
        </div>
    </header>


    <!-- ================= SCROLLABLE CONTENT ================= -->
    <main class="flex-1 p-5 pb-28 overflow-y-auto no-scrollbar space-y-5">
        
        <!-- --- TAB: HOME --- -->
        <section id="home" class="tab-content active space-y-5">
            <!-- Dynamic Greeting Card -->
            <div class="flex items-center justify-between premium-card p-4 rounded-2xl">
                <div class="flex items-center gap-3.5">
                    <div class="w-12 h-12 rounded-2xl bg-gradient-to-tr from-cyan-500 to-indigo-500 flex items-center justify-center font-black text-white text-lg shadow-lg shadow-indigo-500/10">MD</div>
                    <div>
                        <h3 class="font-bold text-slate-200 text-sm flex items-center gap-1.5">MD Alife <span class="text-cyan-400 text-xs">⚡</span></h3>
                        <p class="text-[10px] text-slate-400 font-medium tracking-wider uppercase mt-0.5">Premium Earning Node</p>
                    </div>
                </div>
                <span class="px-3 py-1 rounded-xl bg-cyan-500/10 text-cyan-400 text-[10px] font-bold border border-cyan-500/20 uppercase tracking-wider">Verified</span>
            </div>

            <!-- Ultimate Futuristic Balance Board -->
            <div class="relative overflow-hidden rounded-3xl premium-card p-6 border border-indigo-500/10">
                <div class="absolute -right-10 -top-10 w-40 h-40 bg-indigo-500/10 rounded-full blur-3xl pointer-events-none"></div>
                <div class="absolute -left-10 -bottom-10 w-40 h-40 bg-fuchsia-500/10 rounded-full blur-3xl pointer-events-none"></div>
                
                <p class="text-[11px] text-slate-400 font-semibold tracking-widest uppercase opacity-80">Available Liquidity</p>
                <div class="flex items-baseline gap-2 mt-2">
                    <span class="text-2xl font-bold text-cyan-400 heading-font">৳</span>
                    <h1 id="user-balance" class="text-4xl font-black tracking-tight text-white heading-font">0.00</h1>
                </div>
                
                <div class="grid grid-cols-2 gap-4 mt-6 pt-5 border-t border-slate-800/80 text-[11px] text-slate-400 font-medium">
                    <div class="flex flex-col gap-0.5">
                        <span class="text-slate-500 uppercase tracking-wider text-[9px]">Daily Limit</span>
                        <span class="text-slate-200">20 Stream Videos</span>
                    </div>
                    <div class="flex flex-col gap-0.5 text-right">
                        <span class="text-slate-500 uppercase tracking-wider text-[9px]">Threshold Payout</span>
                        <span class="text-cyan-400 font-bold">৳1500 BDT</span>
                    </div>
                </div>
            </div>

            <!-- Live Payout Feed Ticker -->
            <div class="premium-card border-amber-500/10 text-amber-300 text-xs py-3 px-4 rounded-2xl flex items-center gap-3">
                <span class="w-2 h-2 rounded-full bg-amber-500 animate-pulse shrink-0"></span>
                <marquee class="font-medium" scrollamount="4">User Shaki*** just cashed out ৳1,620 via bKash! • Fulfill 150 Videos or 20 Refers to completely unlock instant gateways!</marquee>
            </div>

            <!-- Precision Metric Matrix Grid -->
            <div class="grid grid-cols-2 gap-4">
                <div class="premium-card p-4 rounded-2xl flex flex-col justify-between h-28">
                    <span class="text-cyan-400 font-semibold text-xs tracking-wider uppercase">Today's Pool</span>
                    <div class="mt-2">
                        <span id="stat-tasks" class="text-2xl font-bold text-white heading-font">0</span>
                        <span class="text-xs text-slate-500 font-medium"> / 20</span>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-1">Daily video cap</p>
                </div>
                <div class="premium-card p-4 rounded-2xl flex flex-col justify-between h-28">
                    <span class="text-fuchsia-400 font-semibold text-xs tracking-wider uppercase">Network Refer</span>
                    <div class="mt-2">
                        <span id="stat-refers" class="text-2xl font-bold text-white heading-font">0</span>
                        <span class="text-xs text-slate-500 font-medium"> / 20</span>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-1">৳50.00 / node</p>
                </div>
                <div class="premium-card p-4 rounded-2xl flex flex-col justify-between h-28">
                    <span class="text-indigo-400 font-semibold text-xs tracking-wider uppercase">Total Streamed</span>
                    <div class="mt-2">
                        <span id="stat-ads" class="text-2xl font-bold text-white heading-font">0</span>
                        <span class="text-xs text-slate-500 font-medium"> / 150</span>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-1">Unlock milestone</p>
                </div>
                <div class="premium-card p-4 rounded-2xl flex flex-col justify-between h-28 bg-gradient-to-br from-slate-900 to-indigo-950/20">
                    <span class="text-emerald-400 font-semibold text-xs tracking-wider uppercase">Total Payouts</span>
                    <div class="mt-2">
                        <span class="text-xl font-bold text-slate-400 heading-font">৳</span>
                        <span class="text-2xl font-bold text-emerald-400 heading-font">0.00</span>
                    </div>
                    <p class="text-[10px] text-emerald-500/60 mt-1">Secure & audited</p>
                </div>
            </div>
        </section>

        <!-- --- TAB: VIDEO TASKS --- -->
        <section id="tasks" class="tab-content space-y-4">
            <div class="premium-card p-6 rounded-3xl text-center relative overflow-hidden">
                <div class="absolute inset-x-0 top-0 h-[2px] bg-gradient-to-r from-transparent via-cyan-500 to-transparent"></div>
                <h2 class="text-xl font-bold text-white heading-font">Advanced Video Matrix</h2>
                <p class="text-xs text-slate-400 mt-2 max-w-xs mx-auto">Stream premium promotional content pipelines. Each transmission yields native assets.</p>
                
                <div class="my-6 inline-flex bg-cyan-500/5 text-cyan-400 font-bold px-4 py-2.5 rounded-xl text-xs border border-cyan-500/10 tracking-wide">
                    Reward Module: ৳10.00 BDT / Video
                </div>

                <div class="space-y-2 mb-6 max-w-xs mx-auto text-left">
                    <div class="flex justify-between text-[11px] text-slate-400 font-bold tracking-wider uppercase">
                        <span>Stream Engine Progress</span>
                        <span id="task-count-text" class="text-cyan-400">0 / 20</span>
                    </div>
                    <div class="w-full bg-slate-900 h-2 rounded-full overflow-hidden p-[1px] border border-slate-800">
                        <div id="task-progress" class="bg-gradient-to-r from-cyan-500 via-indigo-500 to-fuchsia-500 h-full w-0 rounded-full transition-all duration-500 shadow-md"></div>
                    </div>
                </div>

                <button onclick="watchAdVideo()" class="w-full max-w-xs bg-gradient-to-r from-cyan-500 to-indigo-600 hover:from-cyan-600 hover:to-indigo-700 text-white font-bold py-3.5 rounded-2xl shadow-xl shadow-cyan-500/10 transition-all active:scale-[0.98] text-xs tracking-widest uppercase heading-font">
                    Initialize Stream Node
                </button>
            </div>
        </section>

        <!-- --- TAB: INDEPENDENT SUPPORT --- -->
        <section id="support" class="tab-content space-y-4">
            <div class="premium-card p-6 rounded-3xl text-center space-y-5">
                <div>
                    <h2 class="text-xl font-bold text-white heading-font">Global Support Core</h2>
                    <p class="text-xs text-slate-400 mt-2 leading-relaxed max-w-xs mx-auto">Encountering anomalies regarding nodes, streams, or asset extraction? Connect instantly with human operatives.</p>
                </div>
                
                <div class="bg-[#050b18] border border-slate-850 rounded-2xl p-6 max-w-xs mx-auto space-y-5 flex flex-col items-center shadow-inner">
                    <div class="w-14 h-14 bg-gradient-to-tr from-indigo-500/10 to-fuchsia-500/10 rounded-2xl flex items-center justify-center border border-indigo-500/20">
                        <svg class="w-6 h-6 text-indigo-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>
                    </div>
                    <div class="text-center">
                        <h3 class="font-bold text-sm text-slate-200">Official Telegram Operator</h3>
                        <p class="text-[11px] text-slate-500 mt-1">Secure verified support terminal</p>
                    </div>
                    <a href="https://t.me/Suupport7" target="_blank" class="w-full bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white text-xs font-bold py-3 rounded-xl transition-all text-center block tracking-widest uppercase shadow-md heading-font">
                        Establish Connection (@Suupport7)
                    </a>
                </div>
            </div>
        </section>

        <!-- --- TAB: REFER PIPELINE --- -->
        <section id="refer" class="tab-content space-y-4">
            <div class="premium-card p-6 rounded-3xl space-y-4 relative overflow-hidden">
                <div class="flex items-center gap-3">
                    <div class="w-8 h-8 rounded-lg bg-fuchsia-500/10 flex items-center justify-center text-fuchsia-400 text-sm">✦</div>
                    <h2 class="text-base font-bold text-white heading-font">Affiliate Network Expansion</h2>
                </div>
                <p class="text-xs text-slate-400 leading-relaxed">Amplify your node. Every structural entity onboarded via your link directly awards liquid capital to your vault.</p>
                
                <div class="bg-emerald-500/5 text-emerald-400 text-[11px] font-semibold py-3 px-4 rounded-xl border border-emerald-500/10 flex justify-between items-center">
                    <span>Affiliate Payload: ৳50.00 BDT / Referral</span>
                    <span>✨</span>
                </div>

                <!-- Input box -->
                <div class="relative bg-slate-950 p-3.5 rounded-xl border border-slate-900 flex items-center justify-between gap-3">
                    <input type="text" id="ref-link" readonly value="https://t.me/AlifIncomeBdBot?start=user77" class="bg-transparent text-xs text-slate-400 outline-none flex-1 truncate select-all font-mono tracking-tight">
                    <button onclick="copyRefLink()" class="p-2.5 bg-indigo-600 hover:bg-indigo-700 text-white rounded-lg transition-all active:scale-90">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7v8a2 2 0 002 2h6a2 2 0 002-2V7a2 2 0 00-2-2h-6a2 2 0 00-2 2zM8 7H6a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2v-2"></path></svg>
                    </button>
                </div>

                <button onclick="simulateFakeRefer()" class="w-full bg-gradient-to-r from-fuchsia-600 to-indigo-600 text-white font-bold text-xs py-3.5 rounded-xl active:scale-[0.98] transition-all tracking-wider shadow-lg uppercase heading-font">
                    Simulate Referral Influx (+৳50)
                </button>
            </div>
        </section>

        <!-- --- TAB: WALLET GATEWAY --- -->
        <section id="withdraw" class="tab-content space-y-4">
            <div class="premium-card p-5 rounded-3xl space-y-4">
                <!-- Smart Conditional Logic Display -->
                <div class="bg-indigo-500/5 border border-indigo-500/10 p-4 rounded-2xl text-xs space-y-3">
                    <h4 class="font-bold text-indigo-400 flex items-center gap-2 uppercase tracking-wider text-[11px]">
                        ⚠️ Smart Escrow Gate Requirements
                    </h4>
                    <p class="text-slate-400 leading-relaxed">To claim withdrawal requests, you must successfully clear at least **ONE** of the following validation parameters:</p>
                    <ul class="space-y-2 text-slate-300 font-medium pl-1">
                        <li class="flex justify-between items-center bg-slate-900/50 p-2 rounded-lg border border-slate-850">
                            <span>• Complete 150 Video Transmissions</span>
                            <span id="cond-ads" class="text-fuchsia-400 font-bold bg-fuchsia-500/10 px-2 py-0.5 rounded">0 / 150</span>
                        </li>
                        <li class="flex justify-between items-center bg-slate-900/50 p-2 rounded-lg border border-slate-850">
                            <span>• OR Secure 20 Network Referrals</span>
                            <span id="cond-refers" class="text-cyan-400 font-bold bg-cyan-500/10 px-2 py-0.5 rounded">0 / 20</span>
                        </li>
                    </ul>
                </div>

                <!-- Input Processing Fields -->
                <div class="space-y-4 pt-2">
                    <div>
                        <label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest block mb-1.5">Disbursement Channel</label>
                        <select id="withdraw-method" class="w-full bg-slate-950 border border-slate-900 rounded-xl px-4 py-3.5 text-xs text-slate-300 font-semibold outline-none focus:border-cyan-500 transition-all">
                            <option value="bKash">bKash (বিকাশ)</option>
                            <option value="Nagad">Nagad (নগদ)</option>
                            <option value="Rocket">Rocket (রকেট)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest block mb-1.5">Recipient Account Number</label>
                        <input type="text" id="withdraw-account" placeholder="Enter mobile wallet address" class="w-full bg-slate-950 border border-slate-900 rounded-xl px-4 py-3.5 text-xs text-slate-300 outline-none focus:border-cyan-500 transition-all font-mono">
                    </div>
                    <div>
                        <label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest block mb-1.5">Quantum Amount (৳)</label>
                        <input type="number" id="withdraw-amount" placeholder="Minimum threshold ৳1500 BDT" class="w-full bg-slate-950 border border-slate-900 rounded-xl px-4 py-3.5 text-xs text-slate-300 outline-none focus:border-cyan-500 transition-all font-mono">
                    </div>
                </div>

                <button onclick="processWithdrawalRequest()" class="w-full bg-gradient-to-r from-cyan-500 via-indigo-500 to-fuchsia-500 text-white font-bold text-xs py-4 rounded-xl transition-all active:scale-[0.98] uppercase tracking-widest shadow-xl shadow-indigo-500/10 heading-font">
                    Transmit Withdrawal Ledger
                </button>
            </div>
        </section>

    </main>


    <!-- ================= BOTTOM PREMIUM NAV BAR ================= -->
    <nav class="fixed bottom-0 left-0 right-0 max-w-md mx-auto bg-[#030712]/90 backdrop-blur-xl border-t border-slate-900/60 px-3 py-3 flex justify-around items-center z-50 rounded-t-[28px] shadow-2xl">
        <button onclick="switchTab('home')" class="nav-btn text-cyan-400 flex flex-col items-center gap-1.5 py-1 w-14 transition-all" data-tab="home">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[9px] font-bold tracking-wider uppercase">Core</span>
        </button>
        <button onclick="switchTab('tasks')" class="nav-btn text-slate-500 flex flex-col items-center gap-1.5 py-1 w-14 transition-all" data-tab="tasks">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 10l4.553-2.276A1 1 0 0121 8.618v6.764a1 1 0 01-1.447.894L15 14M5 18h8a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v8a2 2 0 002 2z"></path></svg>
            <span class="text-[9px] font-bold tracking-wider uppercase">Streams</span>
        </button>
        <button onclick="switchTab('support')" class="nav-btn text-slate-500 flex flex-col items-center gap-1.5 py-1 w-14 transition-all" data-tab="support">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px] font-bold tracking-wider uppercase">Support</span>
        </button>
        <button onclick="switchTab('refer')" class="nav-btn text-slate-500 flex flex-col items-center gap-1.5 py-1 w-14 transition-all" data-tab="refer">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
            <span class="text-[9px] font-bold tracking-wider uppercase">Nodes</span>
        </button>
        <button onclick="switchTab('withdraw')" class="nav-btn text-slate-500 flex flex-col items-center gap-1.5 py-1 w-14 transition-all" data-tab="withdraw">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px] font-bold tracking-wider uppercase">Vault</span>
        </button>
    </nav>


    <!-- ================= DYNAMIC JAVASCRIPT SYSTEM ================= -->
    <script>
        // Reactive State Storage
        let currentBalance = 0;
        let totalRefers = 0;
        let todayVideosStreamed = 0;
        let totalAdsWatched = 0; 
        
        const maxDailyVideos = 20;
        const rewardPerVideo = 10;
        const rewardPerRefer = 50;
        
        const conditionMinAds = 150;
        const conditionMinRefers = 20;
        const hardMinWithdraw = 1500;

        // UI Initialization & Splash Screen Logic
        window.addEventListener('DOMContentLoaded', () => {
            setTimeout(() => {
                const splash = document.getElementById('splash-screen');
                splash.style.display = 'none';
            }, 3100); // Fades completely out after CSS keyframe finish
            updateDisplayEngine();
        });

        // Modular Tab Swapper Engine
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('text-cyan-400');
                btn.classList.add('text-slate-500');
            });
            
            document.getElementById(tabId).classList.add('active');
            const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
            if (activeBtn) {
                activeBtn.classList.remove('text-slate-500');
                activeBtn.classList.add('text-cyan-400');
            }
        }

        // Live DOM Syncer 
        function updateDisplayEngine() {
            document.getElementById('user-balance').innerText = currentBalance.toFixed(2);
            document.getElementById('stat-tasks').innerText = todayVideosStreamed;
            document.getElementById('stat-refers').innerText = totalRefers;
            document.getElementById('stat-ads').innerText = totalAdsWatched;
            
            // Sync Task Tab Elements
            document.getElementById('task-count-text').innerText = `${todayVideosStreamed} / ${maxDailyVideos}`;
            const percentage = (todayVideosStreamed / maxDailyVideos) * 100;
            document.getElementById('task-progress').style.width = `${percentage}%`;
            
            // Sync Wallet Qualification Data
            document.getElementById('cond-ads').innerText = `${totalAdsWatched} / ${conditionMinAds}`;
            document.getElementById('cond-refers').innerText = `${totalRefers} / ${conditionMinRefers}`;
        }

        // Action Core: Video Streams Simulation
        function watchAdVideo() {
            if (todayVideosStreamed >= maxDailyVideos) {
                alert("❌ Critical: Daily transmission bandwidth allocation reached (Max 20/day)!");
                return;
            }
            
            todayVideosStreamed++;
            totalAdsWatched++; 
            currentBalance += rewardPerVideo;
            
            alert(`✨ Connection Secure: Stream Transmitted successfully!\n💰 Reward Granted: ৳${rewardPerVideo}.00 BDT`);
            updateDisplayEngine();
        }

        // Action Core: Affiliate Simulator Node
        function simulateFakeRefer() {
            totalRefers++;
            currentBalance += rewardPerRefer;
            alert(`🚀 Node Linked: Affiliate structurally bounded!\n💰 Wallet Credited: +৳${rewardPerRefer}.00 BDT`);
            updateDisplayEngine();
        }

        // Clipboard Copy Utility
        function copyRefLink() {
            const copyText = document.getElementById("ref-link");
            copyText.select();
            copyText.setSelectionRange(0, 99999);
            navigator.clipboard.writeText(copyText.value);
            alert("🔗 Link encrypted & copied to operational clipboard!");
        }

        // Smart Withdrawal Validation Matrix
        function processWithdrawalRequest() {
            const targetMethod = document.getElementById('withdraw-method').value;
            const targetAccount = document.getElementById('withdraw-account').value.trim();
            const targetAmount = parseFloat(document.getElementById('withdraw-amount').value);

            if (!targetAccount) {
                alert("❌ Input Error: Recipient account parameter cannot be blank.");
                return;
            }
            if (isNaN(targetAmount) || targetAmount < hardMinWithdraw) {
                alert(`❌ Gate Rejected: Minimum withdrawal amount parameter must be ৳${hardMinWithdraw} BDT or greater.`);
                return;
            }
            if (currentBalance < targetAmount) {
                alert("❌ Financial Error: Insufficient funds in available ledger balance.");
                return;
            }

            // Gatekeeping conditional checks (Must clear at least ONE condition)
            const clearedAds = totalAdsWatched >= conditionMinAds;
            const clearedRefers = totalRefers >= conditionMinRefers;

            if (!clearedAds && !clearedRefers) {
                alert(`🔒 Security Gate Locked:\n\nYou have not satisfied verification protocols. Clear at least ONE threshold to unlock payouts:\n\n1. Watch ${conditionMinAds} Videos total (Current: ${totalAdsWatched})\n2. OR Onboard ${conditionMinRefers} Node Referrals (Current: ${totalRefers})`);
                return;
            }

            // Success Execution Pipeline
            currentBalance -= targetAmount;
            alert(`✅ Transaction Initialized!\n\nChannel: ${targetMethod}\nTarget Account: ${targetAccount}\nQuantum Balance: ৳${targetAmount} BDT\n\nStatus: Processing via Network Nodes. Will credit within short window.`);
            
            document.getElementById('withdraw-account').value = "";
            document.getElementById('withdraw-amount').value = "";
            updateDisplayEngine();
        }
    </script>
</body>
</html>
