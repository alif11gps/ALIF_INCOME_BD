<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ALIF_INCOME_BD - Premium Earning Hub</title> 
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* Strict screen lock mechanics to prevent any movement/shaking */
        html, body {
            overflow: hidden !important;
            position: fixed;
            width: 100%;
            height: 100%;
            background-color: #020617;
            color: #f8fafc;
            font-family: 'Rajdhani', sans-serif;
            -webkit-tap-highlight-color: transparent;
            touch-action: none;
        }
        
        .cyber-font {
            font-family: 'Orbitron', sans-serif;
        }
        
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        
        /* Ultra-Premium Cyberpunk Glassmorphism */
        .cyber-card {
            background: linear-gradient(135deg, rgba(15, 23, 42, 0.85) 0%, rgba(30, 41, 59, 0.7) 100%);
            backdrop-filter: blur(25px);
            border: 1px solid rgba(6 182 212 / 0.15);
            box-shadow: 0 0 25px rgba(0, 0, 0, 0.7), inset 0 1px 1px rgba(255,255,255,0.05);
        }

        .cyber-neon-glow {
            text-shadow: 0 0 8px rgba(6, 182, 212, 0.7), 0 0 20px rgba(236, 72, 153, 0.5);
        }
        
        /* Splash Screen Animation */
        @keyframes customFade {
            to { opacity: 0; visibility: hidden; }
        }
        .splash-fade {
            animation: customFade 0.6s cubic-bezier(0.4, 0, 0.2, 1) forwards;
            animation-delay: 2.2s;
        }
    </style>
</head>
<body class="flex flex-col items-center justify-center">

<!-- ================= PREMIUM CYBER SPLASH SCREEN ================= -->
<div id="splash-screen" class="fixed inset-0 w-full h-full bg-[#020617] z-[100] flex flex-col items-center justify-center p-6 splash-fade">
    <div class="relative flex flex-col items-center space-y-6">
        <div class="w-28 h-28 relative flex items-center justify-center rounded-2xl bg-gradient-to-br from-cyan-500 via-purple-500 to-pink-500 shadow-[0_0_40px_rgba(6,182,212,0.3)] animate-pulse">
            <div class="absolute inset-[3px] bg-[#020617] rounded-[13px] flex items-center justify-center">
                <span class="text-4xl font-black cyber-font bg-gradient-to-r from-cyan-400 to-pink-500 bg-clip-text text-transparent cyber-neon-glow">A_B</span>
            </div>
        </div>
        <div class="text-center">
            <h1 class="text-3xl font-black tracking-widest cyber-font bg-gradient-to-r from-white via-cyan-200 to-slate-400 bg-clip-text text-transparent cyber-neon-glow">ALIF_INCOME_BD</h1>
            <p class="text-xs text-cyan-400/80 tracking-[0.25em] uppercase mt-2 font-bold">NEXT-GEN QUANTUM NODES</p>
        </div>
    </div>
</div>

<!-- ================= MAIN APP CONSTRAINED WRAPPER ================= -->
<div class="w-full max-w-md h-full flex flex-col bg-[#020617] relative overflow-hidden border-x border-cyan-950/40 shadow-[0_0_50px_rgba(0,0,0,0.8)]">
    
    <!-- ================= APP HEADER ================= -->
    <header class="w-full bg-[#020617]/90 backdrop-blur-2xl border-b border-cyan-950/60 px-5 py-4 flex justify-between items-center z-40 shrink-0">
        <div class="flex items-center gap-2">
            <span class="text-xl font-black cyber-font tracking-wide bg-gradient-to-r from-cyan-400 via-indigo-400 to-pink-500 bg-clip-text text-transparent cyber-neon-glow">ALIF_INCOME_BD</span>
            <span class="flex h-2 w-2 relative">
                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-cyan-400 opacity-75"></span>
                <span class="relative inline-flex rounded-full h-2 w-2 bg-cyan-500"></span>
            </span>
        </div>
        <button onclick="switchTab('support')" class="p-2.5 rounded-xl bg-slate-900/80 border border-cyan-950 text-slate-400 hover:text-cyan-400 transition-all shadow-inner">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
        </button>
    </header>

    <!-- ================= SCROLLABLE SECTION (LOCKED WITHIN MAIN) ================= -->
    <main class="flex-1 overflow-y-auto no-scrollbar p-5 pb-32 space-y-5">
        
        <!-- --- TAB: CORE CORE --- -->
        <section id="home" class="tab-content active space-y-5">
            <!-- User Cluster Profile Card -->
            <div class="flex items-center justify-between cyber-card p-4 rounded-xl">
                <div class="flex items-center gap-3.5">
                    <div class="w-11 h-11 rounded-xl bg-gradient-to-br from-cyan-500 to-blue-600 flex items-center justify-center font-black text-white text-base shadow-[0_0_15px_rgba(6,182,212,0.3)]">MD</div>
                    <div>
                        <h3 class="font-bold text-slate-200 text-sm tracking-wide flex items-center gap-1.5 cyber-font">MD Alife <span class="text-cyan-400 text-xs">⚡</span></h3>
                        <p class="text-[10px] text-slate-400 font-semibold tracking-widest uppercase mt-0.5">Premium Terminal Node</p>
                    </div>
                </div>
                <span class="px-2.5 py-1 rounded-md bg-cyan-500/10 text-cyan-400 text-[9px] font-bold border border-cyan-500/30 uppercase tracking-widest">Verified</span>
            </div>

            <!-- Ultimate Liquidity Core Board -->
            <div class="relative overflow-hidden rounded-2xl cyber-card p-6 border-l-4 border-l-cyan-500">
                <p class="text-[10px] text-slate-400 font-bold tracking-widest uppercase opacity-70 cyber-font">Available Vault Asset</p>
                <div class="flex items-baseline gap-1.5 mt-2">
                    <span class="text-xl font-bold text-cyan-400 cyber-font">৳</span>
                    <h1 id="user-balance" class="text-4xl font-black tracking-tight text-white cyber-font">0.00</h1>
                </div>
                <div class="grid grid-cols-2 gap-4 mt-6 pt-4 border-t border-cyan-950/80 text-[11px] text-slate-400 font-medium tracking-wide">
                    <div>
                        <span class="text-slate-500 uppercase tracking-wider text-[9px] font-bold block">Daily Stream Limit</span>
                        <span class="text-slate-200">20 Premium Videos</span>
                    </div>
                    <div class="text-right">
                        <span class="text-slate-500 uppercase tracking-wider text-[9px] font-bold block">Minimum Milestone</span>
                        <span class="text-cyan-400 font-bold cyber-font">৳1500 BDT</span>
                    </div>
                </div>
            </div>

            <!-- Live Broadcast Feed Ticker -->
            <div class="cyber-card border-pink-500/10 text-pink-400 text-xs py-2.5 px-4 rounded-xl flex items-center gap-3">
                <span class="w-1.5 h-1.5 rounded-full bg-pink-500 animate-ping shrink-0"></span>
                <marquee class="font-semibold uppercase tracking-wider" scrollamount="4">User Miraz*** just extracted ৳1,750 via bKash! • Watch 150 Videos or complete 20 Network Invites to trigger instant execution gateways!</marquee>
            </div>

            <!-- Metric Grid Arrays -->
            <div class="grid grid-cols-2 gap-4">
                <div class="cyber-card p-4 rounded-xl flex flex-col justify-between h-24">
                    <span class="text-cyan-400 font-bold text-[10px] tracking-widest uppercase cyber-font">Today's Pool</span>
                    <div class="mt-1">
                        <span id="stat-tasks" class="text-2xl font-black text-white cyber-font">0</span>
                        <span class="text-xs text-slate-500 font-medium"> / 20</span>
                    </div>
                </div>
                <div class="cyber-card p-4 rounded-xl flex flex-col justify-between h-24">
                    <span class="text-pink-400 font-bold text-[10px] tracking-widest uppercase cyber-font">Network Refers</span>
                    <div class="mt-1">
                        <span id="stat-refers" class="text-2xl font-black text-white cyber-font">0</span>
                        <span class="text-xs text-slate-500 font-medium"> / 20</span>
                    </div>
                </div>
            </div>

            <!-- ================= WORK & INCOME HISTORY ARRAYS ================= -->
            <div class="cyber-card p-5 rounded-2xl space-y-3">
                <h3 class="text-xs font-bold text-slate-300 uppercase tracking-widest cyber-font flex items-center gap-2">
                    <span class="text-cyan-400">■</span> Real-Time Income Ledger
                </h3>
                <div id="income-history-list" class="space-y-2 max-h-40 overflow-y-auto pr-1 text-xs font-medium tracking-wide">
                    <p id="no-task-msg" class="text-slate-500 text-center py-4 italic">No transactions mapped onto current ledger cluster.</p>
                </div>
            </div>
        </section>

        <!-- --- TAB: TRANSMISSION CHANNELS (TASKS) --- -->
        <section id="tasks" class="tab-content space-y-4">
            <div class="cyber-card p-6 rounded-2xl text-center relative overflow-hidden">
                <h2 class="text-lg font-bold text-white cyber-font tracking-wide">Quantum Stream Terminal</h2>
                <p class="text-xs text-slate-400 mt-1.5 tracking-wide">Deconstruct promotional streaming packets to extract asset allocation metrics.</p>
                <div class="my-5 inline-flex bg-cyan-500/5 text-cyan-400 font-bold px-4 py-2 rounded-lg text-xs border border-cyan-500/20 tracking-widest uppercase cyber-font">
                    Yield: ৳10.00 BDT / Packet
                </div>
                <div class="w-full bg-slate-950 h-1.5 rounded-full overflow-hidden mb-6 border border-cyan-950">
                    <div id="task-progress" class="bg-gradient-to-r from-cyan-400 to-blue-500 h-full w-0 transition-all duration-300 shadow-[0_0_10px_rgba(6,182,212,0.5)]"></div>
                </div>
                <button onclick="watchAdVideo()" class="w-full bg-gradient-to-r from-cyan-500 to-blue-600 hover:from-cyan-600 hover:to-blue-700 text-white font-bold py-3 rounded-xl text-xs tracking-widest uppercase cyber-font shadow-lg transition-all active:scale-[0.98]">
                    Initialize Packet Stream
                </button>
            </div>
        </section>

        <!-- --- TAB: AFFILIATE NETWORK (REFER) --- -->
        <section id="refer" class="tab-content space-y-4">
            <div class="cyber-card p-6 rounded-2xl space-y-4">
                <h2 class="text-base font-bold text-white cyber-font tracking-wide">Affiliate Network Expansion</h2>
                <div class="bg-emerald-500/5 text-emerald-400 text-xs font-bold py-3 px-4 rounded-xl border border-emerald-500/20 tracking-wider flex justify-between">
                    <span>PAYLOAD REWARD:</span>
                    <span class="cyber-font">৳50.00 BDT / Node</span>
                </div>
                <div class="relative bg-slate-950 p-3 rounded-xl border border-cyan-950 flex items-center justify-between">
                    <input type="text" id="ref-link" readonly value="https://t.me/AlifIncomeBdBot?start=user77" class="bg-transparent text-xs text-cyan-400 outline-none flex-1 truncate font-mono tracking-tight select-all">
                    <button onclick="copyRefLink()" class="ml-2 px-4 py-1.5 bg-cyan-600 hover:bg-cyan-700 text-white font-bold text-xs rounded-lg transition-all active:scale-90 cyber-font uppercase">Copy</button>
                </div>
                <button onclick="simulateFakeRefer()" class="w-full bg-gradient-to-r from-pink-600 to-purple-600 text-white font-bold text-xs py-3.5 rounded-xl uppercase tracking-widest cyber-font shadow-md transition-all active:scale-[0.98]">
                    Simulate Referral Node (+৳50)
                </button>
            </div>
        </section>

        <!-- --- TAB: ESCROW EXTRACATION (WITHDRAW) --- -->
        <section id="withdraw" class="tab-content space-y-4">
            <div class="cyber-card p-5 rounded-2xl space-y-4">
                <div class="bg-cyan-500/5 border border-cyan-500/20 p-4 rounded-xl text-xs space-y-2">
                    <h4 class="font-bold text-cyan-400 uppercase tracking-widest cyber-font text-[10px]">⚠️ Escrow Gateway Verification</h4>
                    <p class="text-slate-400 leading-relaxed font-semibold">To clear verification, your node must unlock at least ONE parameter:</p>
                    <div class="text-slate-300 font-bold space-y-1.5 pt-1">
                        <div class="flex justify-between items-center bg-slate-950/40 p-2 rounded border border-cyan-950/40"><span>• Stream 150 Core Packets</span> <span id="cond-ads" class="text-pink-400 cyber-font">0 / 150</span></div>
                        <div class="flex justify-between items-center bg-slate-950/40 p-2 rounded border border-cyan-950/40"><span>• Onboard 20 Referral Entities</span> <span id="cond-refers" class="text-cyan-400 cyber-font">0 / 20</span></div>
                    </div>
                </div>

                <div class="space-y-3.5 text-xs">
                    <div>
                        <label class="text-slate-400 font-bold uppercase tracking-wider block mb-1">Disbursement Channel</label>
                        <select id="withdraw-method" class="w-full bg-slate-950 border border-cyan-950 rounded-xl px-4 py-3 text-slate-200 font-bold outline-none focus:border-cyan-500 transition-all">
                            <option value="bKash">bKash (বিকাশ)</option>
                            <option value="Nagad">Nagad (নগদ)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-slate-400 font-bold uppercase tracking-wider block mb-1">Recipient Account Coordinates</label>
                        <input type="text" id="withdraw-account" placeholder="Enter mobile secure wallet address" class="w-full bg-slate-950 border border-cyan-950 rounded-xl px-4 py-3 text-slate-300 outline-none focus:border-cyan-500 transition-all font-mono">
                    </div>
                    <div>
                        <label class="text-slate-400 font-bold uppercase tracking-wider block mb-1">Extraction Amount (৳)</label>
                        <input type="number" id="withdraw-amount" placeholder="Minimum threshold ৳1500 BDT" class="w-full bg-slate-950 border border-cyan-950 rounded-xl px-4 py-3 text-slate-300 outline-none focus:border-cyan-500 transition-all font-mono">
                    </div>
                </div>

                <button onclick="processWithdrawalRequest()" class="w-full bg-gradient-to-r from-cyan-500 via-indigo-500 to-pink-500 text-white font-bold text-xs py-3.5 rounded-xl uppercase tracking-widest cyber-font shadow-lg shadow-cyan-950/50">
                    Transmit Extraction Ledger
                </button>
            </div>

            <!-- ================= ASSET EXTRACTION RECORD HISTORY ================= -->
            <div class="cyber-card p-5 rounded-2xl space-y-3">
                <h3 class="text-xs font-bold text-slate-300 uppercase tracking-widest cyber-font flex items-center gap-2">
                    <span class="text-pink-400">■</span> Asset Extraction Archives
                </h3>
                <div id="withdraw-history-list" class="space-y-2 max-h-40 overflow-y-auto pr-1 text-xs font-medium tracking-wide">
                    <p id="no-withdraw-msg" class="text-slate-500 text-center py-4 italic">No extractions logged into historical ledger database.</p>
                </div>
            </div>
        </section>

        <!-- --- TAB: QUANTUM OVERWATCH (SUPPORT) --- -->
        <section id="support" class="tab-content space-y-4">
            <div class="cyber-card p-6 rounded-2xl text-center space-y-5">
                <div>
                    <h2 class="text-lg font-bold text-white cyber-font tracking-wide">Quantum Overwatch Support</h2>
                    <p class="text-xs text-slate-400 mt-2 leading-relaxed max-w-xs mx-auto">Encountering structural operational grid anomalies? Connect directly with Human Support Supervisor.</p>
                </div>
                
                <!-- Updated Support Node pointing directly to Sadia Aktar's Facebook Core -->
                <div class="bg-slate-950/60 border border-cyan-950 rounded-xl p-5 max-w-xs mx-auto space-y-4 flex flex-col items-center">
                    <div class="w-12 h-12 bg-gradient-to-tr from-cyan-500/10 to-pink-500/10 rounded-xl flex items-center justify-center border border-cyan-500/20">
                        <svg class="w-6 h-6 text-cyan-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>
                    </div>
                    <div class="text-center">
                        <h3 class="font-bold text-sm text-slate-200 tracking-wide cyber-font">Sadia Aktar</h3>
                        <p class="text-[10px] text-cyan-400/80 font-bold uppercase tracking-widest mt-0.5">Official Network Executive</p>
                    </div>
                    <a href="https://www.facebook.com/" target="_blank" class="w-full bg-blue-600 hover:bg-blue-700 text-white text-xs font-bold py-2.5 rounded-lg transition-all text-center block tracking-widest uppercase cyber-font shadow-md">
                        Connect via Facebook Profile
                    </a>
                </div>
            </div>
        </section>

    </main>

    <!-- ================= RIGID IMMOBILE BOTTOM NAV BAR ================= -->
    <nav class="absolute bottom-0 left-0 right-0 bg-[#020617]/95 backdrop-blur-2xl border-t border-cyan-950/80 px-2 py-3 flex justify-around items-center z-40 rounded-t-2xl shadow-[0_-5px_20px_rgba(0,0,0,0.6)]">
        <button onclick="switchTab('home')" class="nav-btn text-cyan-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="home">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[9px] font-bold tracking-widest uppercase cyber-font">Core</span>
        </button>
        <button onclick="switchTab('tasks')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="tasks">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px] font-bold tracking-widest uppercase cyber-font">Stream</span>
        </button>
        <button onclick="switchTab('refer')" clas
