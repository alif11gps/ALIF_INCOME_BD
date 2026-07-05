<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ALIF_INCOME_BD - Watch Videos & Earn Money</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0f172a;
            --accent: #3b82f6;
            --success: #22c55e;
            --amber-500: #f59e0b;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #0f172a;
            color: #ffffff;
            user-select: none;
        }
        .premium-gradient {
            background: linear-gradient(135deg, #1e3a8a 0%, #3b82f6 50%, #1d4ed8 100%);
        }
        .glass {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        ::-webkit-scrollbar { display: none; }
        .tab-content { display: none; }
        .tab-content.active { display: block; animation: fadeIn 0.4s ease-out; }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="max-w-md mx-auto min-h-screen relative shadow-2xl bg-slate-950">

<!-- Loading Screen -->
<div id="loading-screen" class="fixed inset-0 z-[100] bg-slate-900 flex flex-col items-center justify-center">
    <div class="w-16 h-16 border-4 border-slate-800 border-t-blue-500 rounded-full animate-spin"></div>
    <p class="mt-4 font-bold text-blue-400 tracking-wider">ALIF_INCOME_BD Loading...</p>
</div>

<!-- Header -->
<header class="sticky top-0 z-50 bg-slate-900/80 backdrop-blur-md px-6 py-4 flex justify-between items-center border-b border-slate-800">
    <div class="flex items-center gap-3">
        <div class="w-10 h-10 bg-blue-600 rounded-2xl flex items-center justify-center text-white font-black shadow-lg shadow-blue-500/20">A</div>
        <div>
            <h1 class="font-black text-white leading-none tracking-tight">ALIF_INCOME_BD</h1>
            <span class="text-[9px] font-bold text-amber-500 tracking-widest uppercase">Watch & Earn Premium Hub</span>
        </div>
    </div>
    <div class="text-[10px] bg-slate-800 px-3 py-1 rounded-full text-slate-400 font-bold uppercase tracking-wider animate-pulse">● Live Server</div>
</header>

<!-- Main Content Area -->
<main class="p-5 pb-32">
    
    <!-- Tab: Home / Dashboard -->
    <section id="home" class="tab-content active space-y-6">
        <!-- Dashboard Balance Card -->
        <div class="premium-gradient rounded-[2.5rem] p-6 text-white shadow-xl relative overflow-hidden">
            <div class="relative z-10">
                <div class="flex justify-between items-start">
                    <div>
                        <p class="text-blue-200 font-medium text-sm">Welcome Back, User</p>
                        <h2 class="text-3xl font-black mt-1">৳ <span id="main-balance">0.00</span></h2>
                        <p class="text-amber-300 font-bold text-xs mt-1 tracking-wide uppercase">Current Earnings</p>
                    </div>
                    <div class="glass p-2 rounded-2xl text-center min-w-[90px]">
                        <span class="text-[9px] font-black block uppercase tracking-wider text-blue-200">Total Refers</span>
                        <span id="refer-count" class="text-xl font-black leading-none text-amber-400">0</span><span class="text-xs text-slate-300">/20</span>
                    </div>
                </div>
                
                <div class="grid grid-cols-2 gap-4 mt-6">
                    <div class="glass rounded-3xl p-4">
                        <p class="text-[9px] text-blue-200 font-bold uppercase mb-1">Per Refer Bonus</p>
                        <p class="text-lg font-black text-amber-400">৳ 10.00</p>
                    </div>
                    <div class="glass rounded-3xl p-4">
                        <p class="text-[9px] text-blue-200 font-bold uppercase mb-1">Daily Task Profit</p>
                        <p class="text-lg font-black text-emerald-400">৳ 50 - 100</p>
                    </div>
                </div>
            </div>
            <div class="absolute -bottom-10 -left-10 w-40 h-40 bg-white/5 rounded-full blur-3xl"></div>
        </div>

        <!-- Refer Progress Bar -->
        <div class="bg-slate-900 rounded-[2rem] p-5 border border-slate-800">
            <div class="flex justify-between items-center mb-2">
                <h3 class="text-xs font-bold text-slate-400 uppercase tracking-wider">Withdrawal Unlock Progress</h3>
                <span id="progress-percent" class="text-xs font-bold text-blue-400">0%</span>
            </div>
            <div class="h-3 bg-slate-800 rounded-full overflow-hidden">
                <div id="progress-bar" class="h-full bg-gradient-to-r from-blue-600 to-emerald-500 w-0 transition-all duration-500"></div>
            </div>
            <p class="text-[10px] text-slate-500 mt-2 text-center">You need minimum 20 successful refers to unlock withdrawal system.</p>
        </div>

        <!-- Quick Action Buttons -->
        <div class="grid grid-cols-2 gap-4">
            <button onclick="switchTab('tasks')" class="bg-slate-900 p-5 rounded-3xl border border-slate-800 flex flex-col items-center justify-center gap-2 hover:border-blue-500 transition-all group">
                <div class="w-12 h-12 rounded-2xl bg-blue-500/10 flex items-center justify-center text-blue-500 group-hover:scale-110 transition-transform">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                </div>
                <span class="text-xs font-bold tracking-wide">Watch Videos</span>
            </button>
            <button onclick="switchTab('refer')" class="bg-slate-900 p-5 rounded-3xl border border-slate-800 flex flex-col items-center justify-center gap-2 hover:border-blue-500 transition-all group">
                <div class="w-12 h-12 rounded-2xl bg-amber-500/10 flex items-center justify-center text-amber-500 group-hover:scale-110 transition-transform">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18 9v3m0 0v3m0-3h3m-3 0h-3m-2-5a4 4 0 11-8 0 4 4 0 018 0zM3 20a6 6 0 0112 0v1H3v-1z"></path></svg>
                </div>
                <span class="text-xs font-bold tracking-wide">Invite Friends</span>
            </button>
        </div>
    </section>

    <!-- Tab: Video Tasks -->
    <section id="tasks" class="tab-content space-y-6">
        <div>
            <h2 class="text-2xl font-black tracking-tight text-white">Premium Video Tasks</h2>
            <p class="text-xs text-slate-400 font-bold uppercase tracking-wider">Watch 1 Minute to Claim Reward</p>
        </div>
        
        <div class="space-y-3">
            <!-- Video Item 1 -->
            <div class="bg-slate-900 border border-slate-800 p-4 rounded-3xl flex justify-between items-center">
                <div class="flex items-center gap-3">
                    <div class="w-10 h-10 bg-red-500/10 text-red-500 rounded-xl flex items-center justify-center font-bold text-sm">YT</div>
                    <div>
                        <h4 class="font-bold text-sm text-white">Video Task #01</h4>
                        <p class="text-[10px] font-bold text-emerald-400">Reward: ৳ 15.00</p>
                    </div>
                </div>
                <button onclick="simulateWatchTask(15)" class="bg-blue-600 hover:bg-blue-700 text-white font-bold text-xs px-4 py-2 rounded-xl transition-all">Watch</button>
            </div>
            <!-- Video Item 2 -->
            <div class="bg-slate-900 border border-slate-800 p-4 rounded-3xl flex justify-between items-center">
                <div class="flex items-center gap-3">
                    <div class="w-10 h-10 bg-red-500/10 text-red-500 rounded-xl flex items-center justify-center font-bold text-sm">YT</div>
                    <div>
                        <h4 class="font-bold text-sm text-white">Video Task #02</h4>
                        <p class="text-[10px] font-bold text-emerald-400">Reward: ৳ 15.00</p>
                    </div>
                </div>
                <button onclick="simulateWatchTask(15)" class="bg-blue-600 hover:bg-blue-700 text-white font-bold text-xs px-4 py-2 rounded-xl transition-all">Watch</button>
            </div>
        </div>
    </section>

    <!-- Tab: Refer System -->
    <section id="refer" class="tab-content space-y-6">
        <div>
            <h2 class="text-2xl font-black tracking-tight text-white">Refer & Earn</h2>
            <p class="text-xs text-slate-400 font-bold uppercase tracking-wider">Get ৳10 for every valid user invited</p>
        </div>

        <div class="bg-slate-900 border border-slate-800 p-6 rounded-[2rem] space-y-4">
            <p class="text-xs text-slate-400 font-medium">Share your exclusive invite link below to invite friends. Once 20 users join, you can unlock immediate cash withdrawals.</p>
            <div class="flex gap-2">
                <input type="text" id="refer-link" readonly value="https://alifincomebd.com/join?ref=user77" class="bg-slate-950 border border-slate-800 text-xs rounded-xl px-4 py-3 text-slate-300 flex-1 outline-none">
                <button onclick="copyLink()" class="bg-blue-600 text-white font-bold text-xs px-4 py-3 rounded-xl hover:bg-blue-700 transition-all">Copy</button>
            </div>
            <div class="pt-4 border-t border-slate-800 text-center">
                <button onclick="simulateRefer()" class="bg-amber-500 hover:bg-amber-600 text-slate-950 font-black text-xs px-6 py-2.5 rounded-full tracking-wider uppercase transition-all">Simulate Fake Refer (+1)</button>
            </div>
        </div>
    </section>

    <!-- Tab: Withdraw -->
    <section id="withdraw" class="tab-content space-y-6">
        <div>
            <h2 class="text-2xl font-black tracking-tight text-white">Secure Cash Out</h2>
            <p class="text-xs text-slate-400 font-bold uppercase tracking-wider">Withdraw your earnings instantly</p>
        </div>

        <div class="bg-slate-900 border border-slate-800 p-6 rounded-[2rem] space-y-4">
            <div>
                <label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest block mb-2">Select Method</label>
                <div class="grid grid-cols-3 gap-2">
                    <button onclick="selectMethod('bKash')" id="btn-bKash" class="method-btn border border-slate-800 p-3 rounded-xl flex flex-col items-center justify-center gap-1 hover:border-pink-500 transition-all">
                        <span class="text-xs font-black text-pink-500">bKash</span>
                    </button>
                    <button onclick="selectMethod('Nagad')" id="btn-Nagad" class="method-btn border border-slate-800 p-3 rounded-xl flex flex-col items-center justify-center gap-1 hover:border-orange-500 transition-all">
                        <span class="text-xs font-black text-orange-500">Nagad</span>
                    </button>
                    <button onclick="selectMethod('Rocket')" id="btn-Rocket" class="method-btn border border-slate-800 p-3 rounded-xl flex flex-col items-center justify-center gap-1 hover:border-purple-500 transition-all">
                        <span class="text-xs font-black text-purple-500">Rocket</span>
                    </button>
                </div>
            </div>

            <div>
                <label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest block mb-1">Account Number</label>
                <input type="number" id="wallet-number" placeholder="017XXXXXXXX" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white outline-none focus:border-blue-500 transition-all">
            </div>

            <div>
                <label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest block mb-1">Amount (৳)</label>
                <input type="number" id="withdraw-amount" placeholder="Minimum ৳200" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white outline-none focus:border-blue-500 transition-all">
            </div>

            <button onclick="handleWithdraw()" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-black text-sm py-4 rounded-xl tracking-wider uppercase transition-all shadow-lg shadow-blue-600/20">Submit Withdrawal Request</button>
        </div>
    </section>

</main>

<!-- Bottom Navigation Bar -->
<nav class="fixed bottom-0 left-0 right-0 max-w-md mx-auto bg-slate-900/95 backdrop-blur-xl border-t border-slate-800 px-6 py-4 flex justify-between items-center z-50 rounded-t-[2.5rem] shadow-[0_-10px_40px_rgba(0,0,0,0.3)]">
    <button onclick="switchTab('home')" class="nav-btn text-blue-500 flex flex-col items-center gap-1" data-tab="home">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
        <span class="text-[8px] font-black uppercase tracking-wider">Home</span>
    </button>
    <button onclick="switchTab('tasks')" class="nav-btn text-slate-500 flex flex-col items-center gap-1" data-tab="tasks">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"></path></svg>
        <span class="text-[8px] font-black uppercase tracking-wider">Tasks</span>
    </button>
    <button onclick="switchTab('refer')" class="nav-btn text-slate-500 flex flex-col items-center gap-1" data-tab="refer">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
        <span class="text-[8px] font-black uppercase tracking-wider">Refer</span>
    </button>
    <button onclick="switchTab('withdraw')" class="nav-btn text-slate-500 flex flex-col items-center gap-1" data-tab="withdraw">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        <span class="text-[8px] font-black uppercase tracking-wider">Withdraw</span>
    </button>
</nav>

<script>
    let currentBalance = 0;
    let totalRefers = 0;
    const requiredRefers = 20;
    let selectedPaymentMethod = '';

    // --- Tab Switcher ---
    function switchTab(tabId) {
        document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
        document.querySelectorAll('.nav-btn').forEach(btn => {
            btn.classList.remove('text-blue-500');
            btn.classList.add('text-slate-500');
        });
        
        document.getElementById(tabId).classList.add('active');
        const activeBtn = document.querySelector(`[data-tab="${tabId}"]`);
        if(activeBtn) {
            activeBtn.classList.remove('text-slate-500');
            activeBtn.classList.add('text-blue-500');
        }
    }

    // --- Selection Highlight ---
    function selectMethod(method) {
        selectedPaymentMethod = method;
        document.querySelectorAll('.method-btn').forEach(btn => {
            btn.classList.remove('border-blue-500', 'bg-slate-800');
        });
        document.getElementById(`btn-${method}`).classList.add('border-blue-500', 'bg-slate-800');
    }

    function copyLink() {
        const copyText = document.getElementById("refer-link");
        copyText.select();
        copyText.setSelectionRange(0, 99999);
        navigator.clipboard.writeText(copyText.value);
        alert("Refer link copied: " + copyText.value);
    }

    // --- Simulation Engines ---
    function simulateWatchTask(reward) {
        alert("Simulating Video Streaming... Please wait.");
        setTimeout(() => {
            currentBalance += reward;
            document.getElementById('main-balance').innerText = currentBalance.toFixed(2);
            alert(`Task Complete! ৳${reward} added to balance.`);
        }, 2000);
    }

    function simulateRefer() {
        if (totalRefers < requiredRefers) {
            totalRefers += 1;
            currentBalance += 10; 
            
            document.getElementById('refer-count').innerText = totalRefers;
            document.getElementById('main-balance').innerText = currentBalance.toFixed(2);
            
            let percentage = (totalRefers / requiredRefers) * 100;
            document.getElementById('progress-percent').innerText = `${percentage}%`;
            document.getElementById('progress-bar').style.width = `${percentage}%`;
        } else {
            alert("Maximum simulation capacity reached or system unlocked!");
        }
    }

    function handleWithdraw() {
        const accountNumber = document.getElementById('wallet-number').value;
        const amount = parseFloat(document.getElementById('withdraw-amount').value);

        if(totalRefers < requiredRefers) {
            alert(`Access Denied! You have only referred ${totalRefers} users. You must invite at least 20 users to activate withdrawal functionality.`);
            return;
        } 
        
        if(!selectedPaymentMethod) {
            alert("Please select a payment method (bKash, Nagad, or Rocket).");
            return;
        }

        if(!accountNumber || accountNumber.length < 11) {
            alert("Please enter a valid account number.");
            return;
        }

        if(isNaN(amount) || amount < 200) {
            alert("Minimum withdrawal limit is ৳200.");
            return;
        }

        if(amount > currentBalance) {
            alert("Insufficient balance!");
            return;
        }

        alert(`Withdrawal Request Submitted Successfully via ${selectedPaymentMethod}! Funds will reflect within 24 hours.`);
        currentBalance -= amount;
        document.getElementById('main-balance').innerText = currentBalance.toFixed(2);
    }

    // --- App Loader Fadeout ---
    window.addEventListener('load', () => {
        setTimeout(() => {
            document.getElementById('loading-screen').style.display = 'none';
        }, 1200);
    });
</script>
</body>
</html>
