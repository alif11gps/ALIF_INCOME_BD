<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ALIF_INCOME_BD - Premium Green Matrix</title> 
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* Strict screen lock mechanics to prevent any movement/shaking */
        html, body {
            overflow: hidden !important;
            position: fixed;
            width: 100%;
            height: 100%;
            background-color: #020a05;
            color: #f0fdf4;
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
        
        /* Premium Cyber Emerald Glassmorphism */
        .cyber-card {
            background: linear-gradient(135deg, rgba(2, 20, 10, 0.9) 0%, rgba(4, 30, 15, 0.75) 100%);
            backdrop-filter: blur(25px);
            border: 1px solid rgba(34, 197, 94, 0.2);
            box-shadow: 0 0 30px rgba(0, 0, 0, 0.8), inset 0 1px 1px rgba(255,255,255,0.03);
        }

        .cyber-neon-glow {
            text-shadow: 0 0 10px rgba(34, 197, 94, 0.8), 0 0 25px rgba(16, 185, 129, 0.5);
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

<!-- ================= PREMIUM EMERALD SPLASH SCREEN ================= -->
<div id="splash-screen" class="fixed inset-0 w-full h-full bg-[#020a05] z-[100] flex flex-col items-center justify-center p-6 splash-fade">
    <div class="relative flex flex-col items-center space-y-6">
        <div class="w-28 h-28 relative flex items-center justify-center rounded-2xl bg-gradient-to-br from-green-500 via-emerald-600 to-teal-500 shadow-[0_0_40px_rgba(34,197,94,0.3)] animate-pulse">
            <div class="absolute inset-[3px] bg-[#020a05] rounded-[13px] flex items-center justify-center">
                <span class="text-4xl font-black cyber-font bg-gradient-to-r from-green-400 to-emerald-300 bg-clip-text text-transparent cyber-neon-glow">A_B</span>
            </div>
        </div>
        <div class="text-center">
            <h1 class="text-3xl font-black tracking-widest cyber-font bg-gradient-to-r from-white via-green-200 to-emerald-400 bg-clip-text text-transparent cyber-neon-glow">ALIF_INCOME_BD</h1>
            <p class="text-xs text-green-400/80 tracking-[0.25em] uppercase mt-2 font-bold">GREEN QUANTUM NODES</p>
        </div>
    </div>
</div>

<!-- ================= MAIN APP CONSTRAINED WRAPPER ================= -->
<div class="w-full max-w-md h-full flex flex-col bg-[#020a05] relative overflow-hidden border-x border-green-950/40 shadow-[0_0_50px_rgba(0,0,0,0.9)]">
    
    <!-- ================= APP HEADER ================= -->
    <header class="w-full bg-[#020a05]/95 backdrop-blur-2xl border-b border-green-950/60 px-5 py-4 flex justify-between items-center z-40 shrink-0">
        <div class="flex items-center gap-2">
            <span class="text-xl font-black cyber-font tracking-wide bg-gradient-to-r from-green-400 via-emerald-400 to-teal-300 bg-clip-text text-transparent cyber-neon-glow">ALIF_INCOME_BD</span>
            <span class="flex h-2 w-2 relative">
                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-green-400 opacity-75"></span>
                <span class="relative inline-flex rounded-full h-2 w-2 bg-green-500"></span>
            </span>
        </div>
        <button onclick="switchTab('support')" class="p-2.5 rounded-xl bg-emerald-950/40 border border-green-900/60 text-green-400 hover:text-green-300 transition-all shadow-inner">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
        </button>
    </header>

    <!-- ================= SCROLLABLE SECTION ================= -->
    <main class="flex-1 overflow-y-auto no-scrollbar p-5 pb-32 space-y-5">
        
        <!-- --- TAB: CORE HOME --- -->
        <section id="home" class="tab-content active space-y-5">
            <!-- User Profile Matrix Card -->
            <div class="flex items-center justify-between cyber-card p-4 rounded-xl">
                <div class="flex items-center gap-3.5">
                    <div class="w-11 h-11 rounded-xl bg-gradient-to-br from-green-500 to-emerald-700 flex items-center justify-center font-black text-white text-base shadow-[0_0_15px_rgba(34,197,94,0.3)]">MD</div>
                    <div>
                        <h3 class="font-bold text-green-100 text-sm tracking-wide flex items-center gap-1.5 cyber-font">MD Alife <span class="text-green-400 text-xs">⚡</span></h3>
                        <p class="text-[10px] text-green-500 font-semibold tracking-widest uppercase mt-0.5">Premium Terminal Node</p>
                    </div>
                </div>
                <span class="px-2.5 py-1 rounded-md bg-green-500/10 text-green-400 text-[9px] font-bold border border-green-500/30 uppercase tracking-widest">Verified</span>
            </div>

            <!-- Main Wallet Display -->
            <div class="relative overflow-hidden rounded-2xl cyber-card p-6 border-l-4 border-l-green-500">
                <p class="text-[10px] text-green-400 font-bold tracking-widest uppercase opacity-70 cyber-font">Available Green Vault Asset</p>
                <div class="flex items-baseline gap-1.5 mt-2">
                    <span class="text-xl font-bold text-green-400 cyber-font">৳</span>
                    <h1 id="user-balance" class="text-4xl font-black tracking-tight text-white cyber-font">0.00</h1>
                </div>
                <div class="grid grid-cols-2 gap-4 mt-6 pt-4 border-t border-green-950/80 text-[11px] text-green-400/80 font-medium tracking-wide">
                    <div>
                        <span class="text-green-600 uppercase tracking-wider text-[9px] font-bold block">Daily Stream Limit</span>
                        <span class="text-slate-200">20 Premium Videos</span>
                    </div>
                    <div class="text-right">
                        <span class="text-green-600 uppercase tracking-wider text-[9px] font-bold block">Minimum Withdrawal</span>
                        <span class="text-green-400 font-bold cyber-font">৳1500 BDT</span>
                    </div>
                </div>
            </div>

            <!-- Live Broadcast Ticker -->
            <div class="cyber-card border-green-500/10 text-green-400 text-xs py-2.5 px-4 rounded-xl flex items-center gap-3">
                <span class="w-1.5 h-1.5 rounded-full bg-green-500 animate-ping shrink-0"></span>
                <marquee class="font-semibold uppercase tracking-wider text-green-300" scrollamount="4">User Alif*** just extracted ৳1,550 via bKash! • Fulfill 150 total video views and 20 network node invites to unlock instantaneous vault cashouts!</marquee>
            </div>

            <!-- Stats Arrays -->
            <div class="grid grid-cols-2 gap-4">
                <div class="cyber-card p-4 rounded-xl flex flex-col justify-between h-24">
                    <span class="text-green-400 font-bold text-[10px] tracking-widest uppercase cyber-font">Today's Pool</span>
                    <div class="mt-1">
                        <span id="stat-tasks" class="text-2xl font-black text-white cyber-font">0</span>
                        <span class="text-xs text-green-600 font-medium"> / 20</span>
                    </div>
                </div>
                <div class="cyber-card p-4 rounded-xl flex flex-col justify-between h-24">
                    <span class="text-emerald-400 font-bold text-[10px] tracking-widest uppercase cyber-font">Network Refers</span>
                    <div class="mt-1">
                        <span id="stat-refers" class="text-2xl font-black text-white cyber-font">0</span>
                        <span class="text-xs text-green-600 font-medium"> / 20</span>
                    </div>
                </div>
            </div>

            <!-- ================= REAL-TIME INCOME LEDGER ================= -->
            <div class="cyber-card p-5 rounded-2xl space-y-3">
                <h3 class="text-xs font-bold text-green-300 uppercase tracking-widest cyber-font flex items-center gap-2">
                    <span class="text-green-400">■</span> Real-Time Income Ledger
                </h3>
                <div id="income-history-list" class="space-y-2 max-h-40 overflow-y-auto pr-1 text-xs font-medium tracking-wide">
                    <p id="no-task-msg" class="text-green-700/60 text-center py-4 italic">No transactions mapped onto current ledger cluster.</p>
                </div>
            </div>
        </section>

        <!-- --- TAB: TRANSMISSION CHANNELS (TASKS) --- -->
        <section id="tasks" class="tab-content space-y-4">
            <div class="cyber-card p-6 rounded-2xl text-center relative overflow-hidden">
                <h2 class="text-lg font-bold text-white cyber-font tracking-wide">Matrix Stream Terminal</h2>
                <p class="text-xs text-green-400/70 mt-1.5 tracking-wide">Deconstruct promotional streaming packets to extract asset allocation metrics.</p>
                <div class="my-5 inline-flex bg-green-500/5 text-green-400 font-bold px-4 py-2 rounded-lg text-xs border border-green-500/20 tracking-widest uppercase cyber-font">
                    Yield: ৳10.00 BDT / Video
                </div>
                <div class="w-full bg-green-950/40 h-1.5 rounded-full overflow-hidden mb-6 border border-green-900/30">
                    <div id="task-progress" class="bg-gradient-to-r from-green-400 to-emerald-500 h-full w-0 transition-all duration-300 shadow-[0_0_10px_rgba(34,197,94,0.5)]"></div>
                </div>
                <button onclick="watchAdVideo()" class="w-full bg-gradient-to-r from-green-500 to-emerald-600 hover:from-green-600 hover:to-emerald-700 text-white font-bold py-3 rounded-xl text-xs tracking-widest uppercase cyber-font shadow-lg transition-all active:scale-[0.98]">
                    Initialize Packet Stream
                </button>
            </div>
        </section>

        <!-- --- TAB: AFFILIATE NETWORK (REFER) --- -->
        <section id="refer" class="tab-content space-y-4">
            <div class="cyber-card p-6 rounded-2xl space-y-4">
                <h2 class="text-base font-bold text-white cyber-font tracking-wide">Affiliate Network Expansion</h2>
                <div class="bg-green-500/5 text-green-400 text-xs font-bold py-3 px-4 rounded-xl border border-green-500/20 tracking-wider flex justify-between">
                    <span>PAYLOAD REWARD:</span>
                    <span class="cyber-font">৳50.00 BDT / Node</span>
                </div>
                <div class="relative bg-emerald-950/20 p-3 rounded-xl border border-green-950 flex items-center justify-between">
                    <input type="text" id="ref-link" readonly value="https://t.me/AlifIncomeBdBot?start=user77" class="bg-transparent text-xs text-green-400 outline-none flex-1 truncate font-mono tracking-tight select-all">
                    <button onclick="copyRefLink()" class="ml-2 px-4 py-1.5 bg-green-600 hover:bg-green-700 text-white font-bold text-xs rounded-lg transition-all active:scale-90 cyber-font uppercase">Copy</button>
                </div>
                <button onclick="simulateFakeRefer()" class="w-full bg-gradient-to-r from-emerald-600 to-teal-600 text-white font-bold text-xs py-3.5 rounded-xl uppercase tracking-widest cyber-font shadow-md transition-all active:scale-[0.98]">
                    Simulate Referral Node (+৳50)
                </button>
            </div>
        </section>

        <!-- --- TAB: ASSET EXTRACTION (WITHDRAW) --- -->
        <section id="withdraw" class="tab-content space-y-4">
            <div class="cyber-card p-5 rounded-2xl space-y-4">
                <div class="bg-green-500/5 border border-green-500/20 p-4 rounded-xl text-xs space-y-2">
                    <h4 class="font-bold text-green-400 uppercase tracking-widest cyber-font text-[10px]">⚠️ Escrow Gateway Verification</h4>
                    <p class="text-green-500/70 leading-relaxed font-semibold">To clear verification locks, your terminal must fulfill both milestones:</p>
                    <div class="text-green-300 font-bold space-y-1.5 pt-1">
                        <div class="flex justify-between items-center bg-emerald-950/20 p-2 rounded border border-green-950/40"><span>• Watch 150 Core Videos</span> <span id="cond-ads" class="text-green-400 cyber-font">0 / 150</span></div>
                        <div class="flex justify-between items-center bg-emerald-950/20 p-2 rounded border border-green-950/40"><span>• Onboard 20 Referral Entities</span> <span id="cond-refers" class="text-green-400 cyber-font">0 / 20</span></div>
                    </div>
                </div>

                <div class="space-y-3.5 text-xs">
                    <div>
                        <label class="text-green-400 font-bold uppercase tracking-wider block mb-1">Disbursement Channel</label>
                        <select id="withdraw-method" class="w-full bg-emerald-950/40 border border-green-950 rounded-xl px-4 py-3 text-green-200 font-bold outline-none focus:border-green-500 transition-all">
                            <option value="bKash">bKash (বিকাশ)</option>
                            <option value="Nagad">Nagad (নগদ)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-green-400 font-bold uppercase tracking-wider block mb-1">Secure Wallet Coordinates</label>
                        <input type="text" id="withdraw-account" placeholder="Enter mobile wallet number" class="w-full bg-emerald-950/40 border border-green-950 rounded-xl px-4 py-3 text-green-300 outline-none focus:border-green-500 transition-all font-mono">
                    </div>
                    <div>
                        <label class="text-green-400 font-bold uppercase tracking-wider block mb-1">Extraction Amount (৳)</label>
                        <input type="number" id="withdraw-amount" placeholder="Minimum ৳1500 BDT" class="w-full bg-emerald-950/40 border border-green-950 rounded-xl px-4 py-3 text-green-300 outline-none focus:border-green-500 transition-all font-mono">
                    </div>
                </div>

                <button onclick="processWithdrawalRequest()" class="w-full bg-gradient-to-r from-green-500 via-emerald-500 to-teal-500 text-white font-bold text-xs py-3.5 rounded-xl uppercase tracking-widest cyber-font shadow-lg shadow-green-950/50">
                    Transmit Extraction Ledger
                </button>
            </div>

            <!-- ================= ASSET EXTRACTION RECORD HISTORY ================= -->
            <div class="cyber-card p-5 rounded-2xl space-y-3">
                <h3 class="text-xs font-bold text-green-300 uppercase tracking-widest cyber-font flex items-center gap-2">
                    <span class="text-green-400">■</span> Asset Extraction Archives
                </h3>
                <div id="withdraw-history-list" class="space-y-2 max-h-40 overflow-y-auto pr-1 text-xs font-medium tracking-wide">
                    <p id="no-withdraw-msg" class="text-green-700/60 text-center py-4 italic">No extractions logged into historical database.</p>
                </div>
            </div>
        </section>

        <!-- --- TAB: CUSTOMER SERVICE (SUPPORT) --- -->
        <section id="support" class="tab-content space-y-4">
            <div class="cyber-card p-6 rounded-2xl text-center space-y-5">
                <div>
                    <h2 class="text-lg font-bold text-white cyber-font tracking-wide">Quantum Support Core</h2>
                    <p class="text-xs text-green-400/70 mt-2 leading-relaxed max-w-xs mx-auto">Encountering structural system anomalies? Connect directly with our network executive.</p>
                </div>
                
                <div class="bg-emerald-950/30 border border-green-950 rounded-xl p-5 max-w-xs mx-auto space-y-4 flex flex-col items-center">
                    <div class="w-12 h-12 bg-gradient-to-tr from-green-500/10 to-emerald-500/10 rounded-xl flex items-center justify-center border border-green-500/20">
                        <svg class="w-6 h-6 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>
                    </div>
                    <div class="text-center">
                        <h3 class="font-bold text-sm text-slate-200 tracking-wide cyber-font">Sadia Aktar</h3>
                        <p class="text-[10px] text-green-400 font-bold uppercase tracking-widest mt-0.5">Official Customer Support</p>
                    </div>
                    <a href="https://www.facebook.com/" target="_blank" class="w-full bg-green-600 hover:bg-green-700 text-white text-xs font-bold py-2.5 rounded-lg transition-all text-center block tracking-widest uppercase cyber-font shadow-md">
                        Connect via Facebook Profile
                    </a>
                </div>
            </div>
        </section>

    </main>

    <!-- ================= RIGID IMMOBILE BOTTOM NAV BAR ================= -->
    <nav class="absolute bottom-0 left-0 right-0 bg-[#020a05]/95 backdrop-blur-2xl border-t border-green-950/80 px-2 py-3 flex justify-around items-center z-40 rounded-t-2xl shadow-[0_-5px_20px_rgba(0,0,0,0.8)]">
        <button onclick="switchTab('home')" class="nav-btn text-green-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="home">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[9px] font-bold tracking-widest uppercase cyber-font">Core</span>
        </button>
        <button onclick="switchTab('tasks')" class="nav-btn text-green-800 flex flex-col items-center gap-1 w-14 transition-all" data-tab="tasks">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px] font-bold tracking-widest uppercase cyber-font">Stream</span>
        </button>
        <button onclick="switchTab('refer')" class="nav-btn text-green-800 flex flex-col items-center gap-1 w-14 transition-all" data-tab="refer">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
            <span class="text-[9px] font-bold tracking-widest uppercase cyber-font">Nodes</span>
        </button>
        <button onclick="switchTab('withdraw')" class="nav-btn text-green-800 flex flex-col items-center gap-1 w-14 transition-all" data-tab="withdraw">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 9V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2m2 4h10a2 2 0 002-2v-6a2 2 0 00-2-2H9a2 2 0 00-2 2v6a2 2 0 002 2zm7-5a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
            <span class="text-[9px] font-bold tracking-widest uppercase cyber-font">Vault</span>
        </button>
    </nav>
</div>

<!-- ================= SYSTEM ENGINE AND CORE STATES ================= -->
<script>
    let balance = 0.00;
    let todayTasks = 0;
    let totalRefers = 0;
    let totalStreamed = 0;

    function switchTab(tabId) {
        document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
        document.getElementById(tabId).classList.add('active');
        
        document.querySelectorAll('.nav-btn').forEach(btn => {
            btn.classList.replace('text-green-400', 'text-green-800');
        });
        const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
        if(activeBtn) activeBtn.classList.replace('text-green-800', 'text-green-400');
    }

    function updateDOM() {
        document.getElementById('user-balance').innerText = balance.toFixed(2);
        document.getElementById('stat-tasks').innerText = todayTasks;
        document.getElementById('stat-refers').innerText = totalRefers;
        
        document.getElementById('cond-ads').innerText = `${totalStreamed} / 150`;
        document.getElementById('cond-refers').innerText = `${totalRefers} / 20`;
    }

    function addIncomeHistory(text, type) {
        const historyList = document.getElementById('income-history-list');
        const noMsg = document.getElementById('no-task-msg');
        if(noMsg) noMsg.remove();

        const color = type === 'video' ? 'text-green-400' : 'text-emerald-400';
        const allocationAmount = type === 'video' ? '+৳10.00' : '+৳50.00';
        const item = document.createElement('div');
        item.className = "flex justify-between items-center bg-slate-950/60 p-2.5 rounded-xl border border-green-950/40";
        item.innerHTML = `
            <span class="text-slate-300 uppercase text-[11px] tracking-wide">${text}</span>
            <span class="${color} font-bold cyber-font">${allocationAmount}</span>
        `;
        historyList.prepend(item);
    }

    function watchAdVideo() {
        if(todayTasks >= 20) {
            alert("Daily packet stream limit (20/20) achieved for today!");
            return;
        }
        alert("Buffering promotional sequence matrix... Please hold 5 seconds.");
        
        setTimeout(() => {
            balance += 10.00;
            todayTasks++;
            totalStreamed++;
            
            document.getElementById('task-progress').style.width = `${(todayTasks/20)*100}%`;
            updateDOM();
            addIncomeHistory(`STREAM PACKET #${todayTasks} COMPLETED`, 'video');
            alert("Success: ৳10.00 BDT processed and added to balance.");
        }, 1000);
    }

    function simulateFakeRefer() {
        balance += 50.00;
        totalRefers++;
        updateDOM();
        addIncomeHistory(`NODE REFERRAL LINK MERGED`, 'refer');
        alert("Referral entity added successfully! +৳50.00 BDT allocated.");
    }

    function copyRefLink() {
        const input = document.getElementById('ref-link');
        input.select();
        document.execCommand('copy');
        alert("Your custom network expander link successfully synchronized onto clipboard!");
    }

    function processWithdrawalRequest() {
        const method = document.getElementById('withdraw-method').value;
        const account = document.getElementById('withdraw-account').value;
        const amount = parseFloat(document.getElementById('withdraw-amount').value);

        if(!account || isNaN(amount)) {
            alert("Error: Incomplete coordinates! Verify target network addresses.");
            return;
        }
        if(amount < 1500) {
            alert("Denied: Minimum cashout barrier is ৳1500 BDT.");
            return;
        }
        if(balance < amount) {
            alert("Error: Insufficient capital matrix within current terminal.");
            return;
        }

        // Hard lock check logic for withdrawal execution
        if(totalStreamed < 150 || totalRefers < 20) {
            alert("Gateway Locked: You must complete exactly 150 core video views AND 20 active network refers to bypass withdrawal escrow clearance.");
            return;
        }

        balance -= amount;
        updateDOM();

        // Insertion into withdrawal log history
        const withdrawList = document.getElementById('withdraw-history-list');
        const noWithMsg = document.getElementById('no-withdraw-msg');
        if(noWithMsg) noWithMsg.remove();

        const item = document.createElement('div');
        item.className = "bg-slate-950/60 p-3 rounded-xl border border-green-950/40 flex justify-between items-center shadow-inner";
        item.innerHTML = `
            <div>
                <p class="text-slate-200 font-bold cyber-font text-xs">${method} (${account})</p>
                <p class="text-[10px] text-amber-400 font-bold tracking-widest uppercase mt-0.5">⏳ PENDING CORE AUDIT</p>
            </div>
            <span class="text-red-400 font-bold cyber-font text-xs">-৳${amount.toFixed(2)}</span>
        `;
        withdrawList.prepend(item);

        alert("Disbursement packet routed. Verification cluster processing pipeline active.");
    }
</script>

</body>
</html>
