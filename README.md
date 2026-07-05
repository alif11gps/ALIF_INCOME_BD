<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ALIF_INCOME_BD - Premium Earning Platform</title> 
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;800&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
        /* সাইট লক এবং নড়াচড়া বন্ধ করার মেইন ট্রিকস */
        html, body {
            overflow-x: hidden !important;
            position: fixed;
            width: 100%;
            height: 100%;
            background-color: #030712;
            color: #f3f4f6;
            font-family: 'Plus Jakarta Sans', sans-serif;
            -webkit-tap-highlight-color: transparent;
        }
        
        .heading-font {
            font-family: 'Space Grotesk', sans-serif;
        }
        
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        
        /* প্রিমিয়াম ডিজিটাল গ্লাস কার্ড */
        .premium-card {
            background: linear-gradient(135deg, rgba(17, 24, 39, 0.8) 0%, rgba(31, 41, 55, 0.6) 100%);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            box-shadow: 0 15px 30px -10px rgba(0,0,0,0.6);
        }

        /* ডিজিটাল গ্লোয়িং লোগো */
        .digital-logo {
            text-shadow: 0 0 10px rgba(34, 211, 238, 0.6), 0 0 20px rgba(168, 85, 247, 0.4);
        }
        
        /* স্প্ল্যাশ স্ক্রিন অ্যানিমেশন */
        @keyframes fadeOut {
            to { opacity: 0; visibility: hidden; }
        }
        .splash-active {
            animation: fadeOut 0.5s ease-in-out forwards;
            animation-delay: 2s;
        }
    </style>
</head>
<body class="flex flex-col items-center justify-start">

<!-- ================= স্প্ল্যাশ স্ক্রিন লোগো ================= -->
<div id="splash-screen" class="fixed inset-0 w-full h-full bg-[#030712] z-[100] flex flex-col items-center justify-center p-6 splash-active">
    <div class="relative flex flex-col items-center space-y-6">
        <div class="w-24 h-24 relative flex items-center justify-center rounded-3xl bg-gradient-to-tr from-cyan-500 via-indigo-500 to-fuchsia-500 shadow-2xl shadow-indigo-500/30">
            <div class="absolute inset-[3px] bg-[#030712] rounded-[21px] flex items-center justify-center">
                <span class="text-3xl font-black heading-font bg-gradient-to-r from-cyan-400 to-fuchsia-400 bg-clip-text text-transparent digital-logo">A_B</span>
            </div>
        </div>
        <div class="text-center">
            <h1 class="text-3xl font-black tracking-widest heading-font bg-gradient-to-r from-white via-slate-200 to-slate-400 bg-clip-text text-transparent digital-logo">ALIF_INCOME_BD</h1>
            <p class="text-xs text-indigo-400/80 tracking-[0.2em] uppercase mt-2 font-semibold">Next-Gen Earning Hub</p>
        </div>
    </div>
</div>

<!-- ================= মেইন কন্টেইনার (মোবাইলে ফুল স্ক্রিন ও স্ট্রং থাকবে) ================= -->
<div class="w-full max-w-md h-full flex flex-col bg-[#030712] relative overflow-hidden shadow-2xl border-x border-slate-900">
    
    <!-- ================= অ্যাপ হেডার ================= -->
    <header class="w-full bg-[#030712]/90 backdrop-blur-xl border-b border-slate-800/60 px-5 py-4 flex justify-between items-center z-40 shrink-0">
        <div class="flex items-center gap-2.5">
            <!-- ডিজিটাল স্টাইলে ভাসমান লোগো নাম -->
            <span class="text-2xl font-black heading-font tracking-wider bg-gradient-to-r from-cyan-400 via-indigo-400 to-fuchsia-400 bg-clip-text text-transparent digital-logo">ALIF_INCOME_BD</span>
            <span class="flex h-2.5 w-2.5 relative">
                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-emerald-500"></span>
            </span>
        </div>
        <button onclick="switchTab('support')" class="p-2 rounded-xl bg-slate-900 border border-slate-800 text-slate-400 hover:text-cyan-400 transition-all">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
        </button>
    </header>

    <!-- ================= স্ক্রোলযোগ্য কন্টেন্ট এরিয়া ================= -->
    <main class="flex-1 overflow-y-auto no-scrollbar p-5 pb-32 space-y-5">
        
        <!-- --- ট্যাব: হোম --- -->
        <section id="home" class="tab-content active space-y-5">
            <!-- ইউজার প্রোফাইল কার্ড -->
            <div class="flex items-center justify-between premium-card p-4 rounded-2xl">
                <div class="flex items-center gap-3.5">
                    <div class="w-12 h-12 rounded-2xl bg-gradient-to-tr from-cyan-500 to-indigo-500 flex items-center justify-center font-black text-white text-lg shadow-lg">MD</div>
                    <div>
                        <h3 class="font-bold text-slate-200 text-sm flex items-center gap-1.5">MD Alife <span class="text-cyan-400 text-xs">⚡</span></h3>
                        <p class="text-[10px] text-slate-400 font-medium tracking-wider uppercase mt-0.5">Premium Earning Node</p>
                    </div>
                </div>
                <span class="px-3 py-1 rounded-xl bg-cyan-500/10 text-cyan-400 text-[10px] font-bold border border-cyan-500/20 uppercase tracking-wider">Verified</span>
            </div>

            <!-- ব্যালেন্স বোর্ড -->
            <div class="relative overflow-hidden rounded-3xl premium-card p-6 border border-indigo-500/10">
                <p class="text-[11px] text-slate-400 font-semibold tracking-widest uppercase opacity-80">Available Liquidity</p>
                <div class="flex items-baseline gap-2 mt-2">
                    <span class="text-2xl font-bold text-cyan-400 heading-font">৳</span>
                    <h1 id="user-balance" class="text-4xl font-black tracking-tight text-white heading-font">0.00</h1>
                </div>
                <div class="grid grid-cols-2 gap-4 mt-6 pt-5 border-t border-slate-800/80 text-[11px] text-slate-400 font-medium">
                    <div>
                        <span class="text-slate-500 uppercase tracking-wider text-[9px] block">Daily Limit</span>
                        <span class="text-slate-200">20 Stream Videos</span>
                    </div>
                    <div class="text-right">
                        <span class="text-slate-500 uppercase tracking-wider text-[9px] block">Threshold Payout</span>
                        <span class="text-cyan-400 font-bold">৳1500 BDT</span>
                    </div>
                </div>
            </div>

            <!-- লাইভ নোটিফিকেশন ফীড -->
            <div class="premium-card border-amber-500/10 text-amber-300 text-xs py-3 px-4 rounded-2xl flex items-center gap-3">
                <span class="w-2 h-2 rounded-full bg-amber-500 animate-pulse shrink-0"></span>
                <marquee class="font-medium" scrollamount="4">User Shaki*** just cashed out ৳1,620 via bKash! • Fulfill 150 Videos or 20 Refers to completely unlock instant gateways!</marquee>
            </div>

            <!-- ম্যাট্রিক্স গ্রিড স্ট্যাটস -->
            <div class="grid grid-cols-2 gap-4">
                <div class="premium-card p-4 rounded-2xl flex flex-col justify-between h-24">
                    <span class="text-cyan-400 font-semibold text-xs tracking-wider uppercase">Today's Pool</span>
                    <div class="mt-1">
                        <span id="stat-tasks" class="text-2xl font-bold text-white heading-font">0</span>
                        <span class="text-xs text-slate-500 font-medium"> / 20</span>
                    </div>
                </div>
                <div class="premium-card p-4 rounded-2xl flex flex-col justify-between h-24">
                    <span class="text-fuchsia-400 font-semibold text-xs tracking-wider uppercase">Network Refer</span>
                    <div class="mt-1">
                        <span id="stat-refers" class="text-2xl font-bold text-white heading-font">0</span>
                        <span class="text-xs text-slate-500 font-medium"> / 20</span>
                    </div>
                </div>
            </div>

            <!-- ================= নতুন সংযোজন: লাইভ ইনকাম ও কাজের ইতিহাস ================= -->
            <div class="premium-card p-5 rounded-3xl space-y-3">
                <h3 class="text-xs font-bold text-slate-300 uppercase tracking-wider flex items-center gap-2">
                    📋 কাজের ও আয়ের ইতিহাস (Task History)
                </h3>
                <div id="income-history-list" class="space-y-2 max-h-48 overflow-y-auto pr-1 text-xs">
                    <p id="no-task-msg" class="text-slate-500 text-center py-4">এখনো কোনো কাজ করা হয়নি।</p>
                </div>
            </div>
        </section>

        <!-- --- ট্যাব: ভিডিও টাস্ক --- -->
        <section id="tasks" class="tab-content space-y-4">
            <div class="premium-card p-6 rounded-3xl text-center relative overflow-hidden">
                <h2 class="text-xl font-bold text-white heading-font">Advanced Video Matrix</h2>
                <p class="text-xs text-slate-400 mt-2">Stream premium promotional content pipelines.</p>
                <div class="my-5 inline-flex bg-cyan-500/5 text-cyan-400 font-bold px-4 py-2 rounded-xl text-xs border border-cyan-500/10">
                    Reward: ৳10.00 BDT / Video
                </div>
                <div class="w-full bg-slate-900 h-2 rounded-full overflow-hidden mb-6">
                    <div id="task-progress" class="bg-gradient-to-r from-cyan-500 to-indigo-500 h-full w-0 transition-all duration-300"></div>
                </div>
                <button onclick="watchAdVideo()" class="w-full bg-gradient-to-r from-cyan-500 to-indigo-600 text-white font-bold py-3.5 rounded-2xl text-xs tracking-widest uppercase heading-font active:scale-95 transition-all">
                    Initialize Stream Node
                </button>
            </div>
        </section>

        <!-- --- ট্যাব: রেফারেল --- -->
        <section id="refer" class="tab-content space-y-4">
            <div class="premium-card p-6 rounded-3xl space-y-4">
                <h2 class="text-base font-bold text-white heading-font">Affiliate Network Expansion</h2>
                <div class="bg-emerald-500/5 text-emerald-400 text-[11px] font-semibold py-3 px-4 rounded-xl border border-emerald-500/10">
                    Affiliate Payload: ৳50.00 BDT / Referral
                </div>
                <div class="relative bg-slate-950 p-3.5 rounded-xl border border-slate-900 flex items-center justify-between">
                    <input type="text" id="ref-link" readonly value="https://t.me/AlifIncomeBdBot?start=user77" class="bg-transparent text-xs text-slate-400 outline-none flex-1 truncate font-mono">
                    <button onclick="copyRefLink()" class="p-2 bg-indigo-600 text-white rounded-lg active:scale-90 transition-all">Copy</button>
                </div>
                <button onclick="simulateFakeRefer()" class="w-full bg-gradient-to-r from-fuchsia-600 to-indigo-600 text-white font-bold text-xs py-3.5 rounded-xl uppercase heading-font">
                    Simulate Referral Influx (+৳50)
                </button>
            </div>
        </section>

        <!-- --- ট্যাব: উইথড্র বা ওয়ালেট গেইট --- -->
        <section id="withdraw" class="tab-content space-y-4">
            <div class="premium-card p-5 rounded-3xl space-y-4">
                <div class="bg-indigo-500/5 border border-indigo-500/10 p-4 rounded-2xl text-xs space-y-2">
                    <h4 class="font-bold text-indigo-400 uppercase tracking-wider">⚠️ Smart Escrow Gate Requirements</h4>
                    <p class="text-slate-400">উত্তোলনের জন্য নিচের যেকোনো ১টি শর্ত পূরণ করতে হবে:</p>
                    <div class="text-slate-300 font-medium space-y-1">
                        <div class="flex justify-between"><span>• 150 ভিডিও দেখা</span> <span id="cond-ads" class="text-fuchsia-400">0 / 150</span></div>
                        <div class="flex justify-between"><span>• অথবা 20 রেফার করা</span> <span id="cond-refers" class="text-cyan-400">0 / 20</span></div>
                    </div>
                </div>

                <div class="space-y-3 text-xs">
                    <div>
                        <label class="text-slate-400 block mb-1">Disbursement Channel</label>
                        <select id="withdraw-method" class="w-full bg-slate-950 border border-slate-900 rounded-xl px-4 py-3 text-slate-300 outline-none">
                            <option value="bKash">bKash (বিকাশ)</option>
                            <option value="Nagad">Nagad (নগদ)</option>
                            <option value="Rocket">Rocket (রকেট)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-slate-400 block mb-1">Account Number</label>
                        <input type="text" id="withdraw-account" placeholder="Enter mobile wallet address" class="w-full bg-slate-950 border border-slate-900 rounded-xl px-4 py-3 text-slate-300 outline-none">
                    </div>
                    <div>
                        <label class="text-slate-400 block mb-1">Amount (৳)</label>
                        <input type="number" id="withdraw-amount" placeholder="Minimum threshold ৳1500 BDT" class="w-full bg-slate-950 border border-slate-900 rounded-xl px-4 py-3 text-slate-300 outline-none">
                    </div>
                </div>

                <button onclick="processWithdrawalRequest()" class="w-full bg-gradient-to-r from-cyan-500 via-indigo-500 to-fuchsia-500 text-white font-bold text-xs py-4 rounded-xl uppercase tracking-widest heading-font">
                    Transmit Withdrawal Ledger
                </button>
            </div>

            <!-- ================= নতুন সংযোজন: উত্তোলনের লাইভ ইতিহাস ================= -->
            <div class="premium-card p-5 rounded-3xl space-y-3">
                <h3 class="text-xs font-bold text-slate-300 uppercase tracking-wider flex items-center gap-2">
                    ⏳ উত্তোলনের ইতিহাস (Withdrawal History)
                </h3>
                <div id="withdraw-history-list" class="space-y-2 max-h-48 overflow-y-auto pr-1 text-xs">
                    <p id="no-withdraw-msg" class="text-slate-500 text-center py-4">এখনো কোনো উত্তোলন রিকোয়েস্ট দেওয়া হয়নি।</p>
                </div>
            </div>
        </section>

        <!-- --- ট্যাব: সাপোর্ট --- -->
        <section id="support" class="tab-content space-y-4">
            <div class="premium-card p-6 rounded-3xl text-center space-y-4">
                <h2 class="text-xl font-bold text-white heading-font">Global Support Core</h2>
                <p class="text-xs text-slate-400">যেকোনো সমস্যা সমাধানের জন্য সরাসরি অফিশিয়াল টেলিগ্রাম অপারেটরের সাথে যোগাযোগ করুন।</p>
                <a href="https://t.me/Suupport7" target="_blank" class="w-full bg-gradient-to-r from-indigo-600 to-purple-600 text-white text-xs font-bold py-3 rounded-xl block tracking-widest text-center uppercase heading-font">
                    Establish Connection (@Suupport7)
                </a>
            </div>
        </section>

    </main>

    <!-- ================= বটম নেভিগেশন বার (ফিক্সড ও নড়াচড়াহীন) ================= -->
    <nav class="absolute bottom-0 left-0 right-0 bg-[#030712]/95 backdrop-blur-xl border-t border-slate-900 px-2 py-3 flex justify-around items-center z-40 rounded-t-[24px]">
        <button onclick="switchTab('home')" class="nav-btn text-cyan-400 flex flex-col items-center gap-1 w-14 transition-all" data-tab="home">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[9px] font-bold uppercase">Core</span>
        </button>
        <button onclick="switchTab('tasks')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="tasks">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px] font-bold uppercase">Stream</span>
        </button>
        <button onclick="switchTab('refer')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="refer">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
            <span class="text-[9px] font-bold uppercase">Nodes</span>
        </button>
        <button onclick="switchTab('withdraw')" class="nav-btn text-slate-500 flex flex-col items-center gap-1 w-14 transition-all" data-tab="withdraw">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 9V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2m2 4h10a2 2 0 002-2v-6a2 2 0 00-2-2H9a2 2 0 00-2 2v6a2 2 0 002 2zm7-5a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
            <span class="text-[9px] font-bold uppercase">Vault</span>
        </button>
    </nav>
</div>

<!-- ================= জাভাস্ক্রিপ্ট লজিক ও ডায়নামিক হিস্ট্রি ট্র্যাকিং ================= -->
<script>
    let balance = 0.00;
    let todayTasks = 0;
    let totalRefers = 0;
    let totalStreamed = 0;

    function switchTab(tabId) {
        document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
        document.getElementById(tabId).classList.add('active');
        
        document.querySelectorAll('.nav-btn').forEach(btn => {
            btn.classList.replace('text-cyan-400', 'text-slate-500');
        });
        const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
        if(activeBtn) activeBtn.classList.replace('text-slate-500', 'text-cyan-400');
    }

    function updateDOM() {
        document.getElementById('user-balance').innerText = balance.toFixed(2);
        document.getElementById('stat-tasks').innerText = todayTasks;
        document.getElementById('stat-refers').innerText = totalRefers;
        
        // লক কন্ডিশন আপডেট
        document.getElementById('cond-ads').innerText = `${totalStreamed} / 150`;
        document.getElementById('cond-refers').innerText = `${totalRefers} / 20`;
    }

    // ইনকাম বা কাজের ইতিহাস যোগ করার ফাংশন
    function addIncomeHistory(text, type) {
        const historyList = document.getElementById('income-history-list');
        const noMsg = document.getElementById('no-task-msg');
        if(noMsg) noMsg.remove();

        const color = type === 'video' ? 'text-cyan-400' : 'text-fuchsia-400';
        const item = document.createElement('div');
        item classList = "flex justify-between items-center bg-slate-900/60 p-2.5 rounded-xl border border-slate-800";
        item.innerHTML = `
            <span class="text-slate-300">${text}</span>
            <span class="${color} font-bold">${type === 'video' ? '+৳10.00' : '+৳50.00'}</span>
        `;
        historyList.prepend(item);
    }

    function watchAdVideo() {
        if(todayTasks >= 20) {
            alert("আপনার আজকের ভিডিও লিমিট (২০টি) শেষ!");
            return;
        }
        alert("ভিডিও স্ট্রিম হচ্ছে... অনুগ্রহ করে ৫ সেকেন্ড অপেক্ষা করুন।");
        
        setTimeout(() => {
            balance += 10.00;
            todayTasks++;
            totalStreamed++;
            
            document.getElementById('task-progress').style.width = `${(todayTasks/20)*100}%`;
            updateDOM();
            addIncomeHistory(`ভিডিও টাস্ক #${todayTasks} সম্পন্ন`, 'video');
            alert("৳১০.০০ সফলভাবে যোগ করা হয়েছে!");
        }, 1000);
    }

    function simulateFakeRefer() {
        balance += 50.00;
        totalRefers++;
        updateDOM();
        addIncomeHistory(`রেফারেল সফল (Node Expansion)`, 'refer');
        alert("সফল রেফারেল! ৳৫০.০০ ব্যালেন্সে যুক্ত হয়েছে।");
    }

    function copyRefLink() {
        const input = document.getElementById('ref-link');
        input.select();
        document.execCommand('copy');
        alert("রেফারেল লিংক কপি হয়েছে!");
    }

    // উইথড্র বা উত্তোলনের ইতিহাস প্রোসেস
    function processWithdrawalRequest() {
        const method = document.getElementById('withdraw-method').value;
        const account = document.getElementById('withdraw-account').value;
        const amount = parseFloat(document.getElementById('withdraw-amount').value);

        if(!account || isNaN(amount)) {
            alert("অনুগ্রহ করে সঠিক নম্বর এবং অ্যামাউন্ট দিন।");
            return;
        }
        if(amount < 1500) {
            alert("সর্বনিম্ন উত্তোলন সীমা ১৫০০ টাকা!");
            return;
        }
        if(balance < amount) {
            alert("আপনার অ্যাকাউন্টে পর্যাপ্ত ব্যালেন্স নেই।");
            return;
        }

        // শর্ত পরীক্ষা
        if(totalStreamed < 150 && totalRefers < 20) {
            alert("দুঃখিত! উইথড্র গেইট লক। আপনাকে অন্তত ১৫০টি ভিডিও দেখতে হবে অথবা ২০টি রেফার করতে হবে।");
            return;
        }

        balance -= amount;
        updateDOM();

        // উইথড্র ইতিহাস স্ক্রিনে অ্যাড করা
        const withdrawList = document.getElementById('withdraw-history-list');
        const noWithMsg = document.getElementById('no-withdraw-msg');
        if(noWithMsg) noWithMsg.remove();

        const item = document.createElement('div');
        item classList = "bg-slate-900/60 p-3 rounded-xl border border-slate-800 flex justify-between items-center";
        item.innerHTML = `
            <div>
                <p class="text-slate-200 font-bold">${method} (${account})</p>
                <p class="text-[10px] text-amber-400">⏳ Pending Audit</p>
            </div>
            <span class="text-rose-400 font-bold">-৳${amount.toFixed(2)}</span>
        `;
        withdrawList.prepend(item);

        alert("আপনার উইথড্রাল রিকোয়েস্ট সফলভাবে জমা হয়েছে এবং অডিটের জন্য পাঠানো হয়েছে।");
    }
</script>

</body>
</html>
