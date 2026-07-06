<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ALIF_INCOME_BD - অফিসিয়াল গেমিং প্ল্যাটফর্ম</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #0b121f;
            color: #ffffff;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .gold-glow { text-shadow: 0 0 12px rgba(245, 158, 11, 0.6); }
        .game-overlay {
            background-color: rgba(11, 18, 31, 0.95);
            backdrop-filter: blur(8px);
        }
        #aviator-canvas {
            background-color: #101726;
            position: relative;
            overflow: hidden;
        }
        .plane {
            position: absolute;
            bottom: 20px;
            left: 20px;
            font-size: 32px;
            transition: all 0.1s linear;
        }
    </style>
</head>
<body class="max-w-md mx-auto min-h-screen flex flex-col border-x border-slate-800 shadow-2xl relative">

    <!-- ================= APP HEADER ================= -->
    <header class="bg-[#1e293b] border-b border-emerald-500/20 px-4 py-3 flex items-center justify-between sticky top-0 z-50 shadow-md">
        <div class="flex items-center gap-2">
            <span class="text-lg font-black text-emerald-400 tracking-wider">ALIF_INCOME_BD</span>
            <div class="bg-emerald-500/20 text-emerald-400 text-[10px] px-2 py-0.5 rounded-full font-bold flex items-center gap-1 animate-pulse">
                <span>●</span> লাইভ
            </div>
        </div>
        
        <!-- User Profile & Balance Area -->
        <div class="flex items-center gap-3">
            <div class="bg-slate-900/80 px-3 py-1.5 rounded-xl border border-slate-700 flex items-center gap-2">
                <span class="text-yellow-400 text-sm font-bold">৳</span>
                <span id="nav-balance" class="font-mono font-bold text-amber-400 text-sm">0.00</span>
            </div>
            <div onclick="switchTab('member')" class="cursor-pointer flex items-center gap-1">
                <div class="w-8 h-8 rounded-full bg-gradient-to-tr from-emerald-500 to-teal-600 flex items-center justify-center font-bold text-white text-xs border border-emerald-400 shadow">
                    MD
                </div>
            </div>
        </div>
    </header>

    <!-- ================= MAIN CONTENT AREA ================= -->
    <main class="flex-1 overflow-y-auto no-scrollbar px-3 py-4 pb-24 space-y-4">
        
        <!-- --- TAB 1: হোম (গেমিং ড্যাশবোর্ড) --- -->
        <section id="home" class="tab-content active space-y-4">
            
            <!-- Banner Slider Placeholder -->
            <div class="bg-gradient-to-r from-purple-900 to-indigo-900 p-4 rounded-2xl border border-indigo-500/30 shadow-lg relative overflow-hidden">
                <div class="absolute -right-4 -bottom-4 opacity-20 text-7xl">🎰</div>
                <span class="bg-amber-500 text-slate-950 font-bold text-[10px] px-2 py-0.5 rounded uppercase tracking-wider">অফার</span>
                <h2 class="text-lg font-black mt-1 text-white">প্রতিদিন আপনার প্রথম জমায়</h2>
                <p class="text-xs mt-0.5 font-bold text-amber-300">১০০% বোনাস ক্যাশব্যাক উপভোগ করুন!</p>
            </div>

            <!-- Live Jackpot Ticker -->
            <div class="bg-gradient-to-b from-amber-950/40 to-slate-900 p-3 rounded-2xl border-2 border-amber-500/50 shadow-xl text-center space-y-1.5">
                <span class="text-[11px] font-bold text-amber-400 tracking-widest uppercase block">🔥 GRAND JACKPOT 🔥</span>
                <div class="flex justify-center gap-1 font-mono text-2xl font-black text-amber-400 tracking-wider gold-glow">
                    <span>৳</span>
                    <span id="jackpot-counter">7,20,81,649</span>
                </div>
            </div>

            <!-- Game Categories Grid -->
            <div>
                <div class="flex gap-2 pb-2 overflow-x-auto no-scrollbar text-xs font-bold">
                    <button class="bg-emerald-500 text-slate-950 px-4 py-2 rounded-xl shrink-0 shadow-md">🔥 জনপ্রিয়</button>
                    <button class="bg-slate-800 text-slate-400 px-4 py-2 rounded-xl shrink-0 hover:bg-slate-700 transition">🎰 স্লটস</button>
                    <button class="bg-slate-800 text-slate-400 px-4 py-2 rounded-xl shrink-0 hover:bg-slate-700 transition">🐟 ফিশিং</button>
                    <button class="bg-slate-800 text-slate-400 px-4 py-2 rounded-xl shrink-0 hover:bg-slate-700 transition">🃏 লাইভ ক্যাসিনো</button>
                </div>

                <!-- Game Cards Grid Layout -->
                <div class="grid grid-cols-2 gap-3 mt-3">
                    <!-- Game 1 -->
                    <div onclick="openGame('superace')" class="bg-slate-800 border border-slate-700 rounded-2xl overflow-hidden shadow-md cursor-pointer group active:scale-95 transition">
                        <div class="h-28 bg-gradient-to-br from-red-600 to-amber-600 flex items-center justify-center relative font-black text-2xl tracking-tighter text-white shadow-inner">
                            Super Ace
                            <div class="absolute bottom-2 right-2 bg-black/60 text-[10px] px-1.5 py-0.5 rounded text-amber-400">JILI</div>
                        </div>
                        <div class="p-2.5 text-center bg-slate-800">
                            <h4 class="text-xs font-bold text-slate-200 group-hover:text-emerald-400 transition">সুপার এইস</h4>
                            <span class="text-[10px] text-emerald-400 font-mono">RTP: 97.8%</span>
                        </div>
                    </div>

                    <!-- Game 2 -->
                    <div onclick="openGame('aviator')" class="bg-slate-800 border border-slate-700 rounded-2xl overflow-hidden shadow-md cursor-pointer group active:scale-95 transition">
                        <div class="h-28 bg-gradient-to-br from-rose-700 to-purple-900 flex items-center justify-center relative font-black text-2xl tracking-tighter text-white">
                            🚀 Aviator
                            <div class="absolute bottom-2 right-2 bg-black/60 text-[10px] px-1.5 py-0.5 rounded text-rose-400">Spribe</div>
                        </div>
                        <div class="p-2.5 text-center bg-slate-800">
                            <h4 class="text-xs font-bold text-slate-200 group-hover:text-emerald-400 transition">এভিয়েটর</h4>
                            <span class="text-[10px] text-rose-400 font-mono">Multi: Up to 100x</span>
                        </div>
                    </div>

                    <!-- Game 3 -->
                    <div onclick="openGame('fortunegems')" class="bg-slate-800 border border-slate-700 rounded-2xl overflow-hidden shadow-md cursor-pointer group active:scale-95 transition">
                        <div class="h-28 bg-gradient-to-br from-yellow-600 to-emerald-800 flex items-center justify-center relative font-black text-xl tracking-tighter text-white">
                            Fortune Gems
                        </div>
                        <div class="p-2.5 text-center bg-slate-800">
                            <h4 class="text-xs font-bold text-slate-200 group-hover:text-emerald-400 transition">ফরচুন জেমস</h4>
                            <span class="text-[10px] text-emerald-400 font-mono">RTP: 96.5%</span>
                        </div>
                    </div>

                    <!-- Game 4 -->
                    <div onclick="openGame('crazytime')" class="bg-slate-800 border border-slate-700 rounded-2xl overflow-hidden shadow-md cursor-pointer group active:scale-95 transition">
                        <div class="h-28 bg-gradient-to-br from-fuchsia-700 to-indigo-900 flex items-center justify-center relative font-black text-xl tracking-tighter text-white">
                            Crazy Time
                        </div>
                        <div class="p-2.5 text-center bg-slate-800">
                            <h4 class="text-xs font-bold text-slate-200 group-hover:text-emerald-400 transition">ক্রেজি টাইম</h4>
                            <span class="text-[10px] text-purple-400 font-mono">লাইভ শো</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- --- TAB 2: প্রমোশন --- -->
        <section id="promotion" class="tab-content space-y-4">
            <h2 class="text-lg font-bold text-emerald-400">🎁 বোনাস ও প্রমোশন</h2>
            
            <div class="bg-slate-800 border border-slate-700 p-4 rounded-2xl space-y-3 shadow">
                <div class="bg-emerald-500 text-slate-950 font-bold text-[11px] px-2.5 py-0.5 rounded-full inline-block">নতুন মেম্বার</div>
                <h3 class="text-sm font-bold text-white">প্রথম ডিপোজিটে ১০০% ওয়েলকাম বোনাস!</h3>
                <p class="text-xs text-slate-400 leading-relaxed">সর্বনিম্ন ৳৫০০ ডিপোজিট করে আপনার ব্যালেন্স দ্বিগুণ করে নিন। জয়ের সুযোগ আরও বেশি!</p>
            </div>

            <div class="bg-slate-800 border border-slate-700 p-4 rounded-2xl space-y-3 shadow">
                <div class="bg-amber-500 text-slate-950 font-bold text-[11px] px-2.5 py-0.5 rounded-full inline-block">প্রতিদিনের রিওয়ার্ড</div>
                <h3 class="text-sm font-bold text-white">ডেইলি সাইন-ইন লাকি ড্র</h3>
                <p class="text-xs text-slate-400 leading-relaxed">প্রতিদিন লগইন করুন এবং জিতে নিন একটি আইফোন ১৭ প্রো ম্যাক্স জেতার আকর্ষণীয় সুযোগ!</p>
            </div>
        </section>

        <!-- --- TAB 3: ডিপোজিট --- -->
        <section id="deposit" class="tab-content space-y-4">
            <div class="bg-slate-800 border border-slate-700 p-5 rounded-2xl space-y-4 shadow-xl">
                <div>
                    <h2 class="text-base font-bold text-emerald-400">📥 অ্যাকাউন্ট রিচার্জ করুন</h2>
                    <p class="text-[11px] text-slate-400 mt-0.5">১ মিনিটের মধ্যে নিরাপদ ও দ্রুত ডিপোজিট সম্পন্ন করুন</p>
                </div>

                <!-- Payment Methods Selector -->
                <div class="grid grid-cols-2 gap-3">
                    <button onclick="selectMethod('বিকাশ')" id="btn-bkash" class="bg-slate-900 border-2 border-pink-600/80 p-3 rounded-xl flex items-center justify-center gap-2 font-bold text-sm text-white transition shadow-sm">
                        <span>💗</span> বিকাশ (Bkash)
                    </button>
                    <button onclick="selectMethod('নগদ')" id="btn-nagad" class="bg-slate-900 border-2 border-slate-700 p-3 rounded-xl flex items-center justify-center gap-2 font-bold text-sm text-slate-300 transition shadow-sm">
                        <span>🧡</span> নগদ (Nagad)
                    </button>
                </div>

                <!-- Fast Amount Selection -->
                <div class="space-y-2">
                    <label class="text-xs font-bold text-slate-400">টাকার পরিমাণ নির্বাচন করুন:</label>
                    <div class="grid grid-cols-4 gap-2 text-xs font-bold">
                        <button onclick="setAmount(300)" class="bg-slate-900 hover:bg-slate-700 border border-slate-700 p-2.5 rounded-lg transition text-slate-200">৳৩০০</button>
                        <button onclick="setAmount(500)" class="bg-slate-900 hover:bg-slate-700 border border-slate-700 p-2.5 rounded-lg transition text-slate-200">৳৫০০</button>
                        <button onclick="setAmount(1000)" class="bg-slate-900 hover:bg-slate-700 border border-slate-700 p-2.5 rounded-lg transition text-slate-200">৳১,০০০</button>
                        <button onclick="setAmount(5000)" class="bg-slate-900 hover:bg-slate-700 border border-slate-700 p-2.5 rounded-lg transition text-slate-200">৳৫,০০০</button>
                    </div>
                </div>

                <!-- Custom Amount Input -->
                <div class="space-y-1.5">
                    <label class="text-xs font-bold text-slate-400">ডিপোজিট পরিমাণ লিখুন (৳):</label>
                    <input type="number" id="dep-amount" placeholder="৳৩০০ - ৳৫০,০০০" class="w-full bg-slate-900 border border-slate-700 text-amber-400 font-mono font-bold rounded-xl px-3 py-3 outline-none focus:border-emerald-500 text-sm">
                </div>

                <!-- Transaction Reference Input -->
                <div class="space-y-1.5">
                    <label class="text-xs font-bold text-slate-400">যে নম্বর থেকে টাকা পাঠিয়েছেন:</label>
                    <input type="text" id="dep-phone" placeholder="আপনার বিকাশ/নগদ নাম্বার দিন" class="w-full bg-slate-900 border border-slate-700 text-slate-200 font-bold rounded-xl px-3 py-3 outline-none focus:border-emerald-500 text-sm">
                </div>

                <button onclick="processDeposit()" class="w-full bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-600 hover:to-teal-700 font-bold text-slate-950 py-3.5 rounded-xl text-sm shadow-md transition transform active:scale-95">
                    ডিপোজিট রিকোয়েস্ট পাঠান
                </button>
            </div>
        </section>

        <!-- --- TAB 4: ইনভাইট --- -->
        <section id="invite" class="tab-content space-y-4">
            <div class="bg-slate-800 border border-slate-700 p-5 rounded-2xl space-y-4 shadow-lg">
                <h2 class="text-base font-bold text-emerald-400 flex items-center gap-2">👥 বন্ধুদের আমন্ত্রণ জানান</h2>
                <p class="text-xs text-slate-400 leading-relaxed">আপনার ইনভাইট লিংক শেয়ার করুন। আপনার রেফার করা বন্ধু প্রথম ডিপোজিট করলেই আপনি পাবেন সাথে সাথে <span class="text-emerald-400 font-bold">৳১০০ বোনাস</span>!</p>
                
                <div class="bg-slate-900 p-3.5 rounded-xl border border-slate-700 flex justify-between items-center gap-2">
                    <span class="text-xs font-mono text-emerald-400 select-all overflow-hidden truncate">http://alifincomebd.com/reg?ref=alife1</span>
                    <button onclick="alert('ইনভাইট লিংক কপি হয়েছে!')" class="p-2 bg-emerald-500 text-slate-950 rounded-lg text-xs font-bold tracking-wide shadow transition shrink-0 active:scale-95">কপি</button>
                </div>
            </div>
        </section>

        <!-- --- TAB 5: মেম্বার প্রফাইল ও উইথড্র --- -->
        <section id="member" class="tab-content space-y-4">
            <!-- Profile Info Box -->
            <div class="bg-slate-800 p-4 rounded-2xl border border-slate-700 flex items-center justify-between gap-3">
                <div class="flex items-center gap-3">
                    <div class="w-12 h-12 rounded-full bg-slate-700 flex items-center justify-center text-xl shadow">👤</div>
                    <div>
                        <h3 class="font-bold text-white flex items-center gap-1.5 text-sm">alife1 <span class="bg-amber-500 text-slate-950 font-bold text-[9px] px-1.5 py-0.2 rounded">VIP 1</span></h3>
                        <p class="text-[11px] text-slate-400 font-mono mt-0.5">আইডি: #8493122</p>
                    </div>
                </div>
                <div class="text-right">
                    <span class="text-[10px] text-slate-400 block">মোট ব্যালেন্স</span>
                    <span id="profile-balance" class="text-base font-bold text-amber-400 font-mono">৳0.00</span>
                </div>
            </div>

            <!-- Withdrawal Box -->
            <div class="bg-slate-800 border border-slate-700 p-5 rounded-2xl space-y-4 shadow-lg">
                <h2 class="text-base font-bold text-rose-400">📤 ব্যালেন্স উত্তোলন (Withdraw)</h2>
                
                <div class="space-y-3 text-xs">
                    <div>
                        <label class="text-slate-400 font-bold block mb-1">পেমেন্ট গেটওয়ে</label>
                        <select id="withdraw-method" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-3 py-3 text-slate-200 font-bold outline-none focus:border-rose-500 text-sm">
                            <option value="বিকাশ">বিকাশ (Bkash)</option>
                            <option value="নগদ">নগদ (Nagad)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-slate-400 font-bold block mb-1">উত্তোলন করার নাম্বার</label>
                        <input type="text" id="withdraw-account" placeholder="আপনার পার্সোনাল নম্বরটি দিন" class="w-full bg-slate-900 border border-slate-700 text-slate-200 font-bold rounded-xl px-3 py-3 outline-none focus:border-rose-500 text-sm">
                    </div>
                    <div>
                        <label class="text-slate-400 font-bold block mb-1">উত্তোলনের পরিমাণ (৳)</label>
                        <input type="number" id="withdraw-amount" placeholder="সর্বনিম্ন ৳৫০০" class="w-full bg-slate-900 border border-slate-700 text-amber-400 font-bold font-mono rounded-xl px-3 py-3 outline-none focus:border-rose-500 text-sm">
                    </div>
                </div>

                <button onclick="processWithdraw()" class="w-full bg-gradient-to-r from-rose-500 to-red-600 hover:from-rose-600 hover:to-red-700 font-bold text-white py-3.5 rounded-xl text-sm shadow-md transition transform active:scale-95">
                    উত্তোলন রিকোয়েস্ট পাঠান
                </button>
            </div>

            <div class="bg-slate-900/60 p-3 rounded-xl border border-dashed border-amber-500/20 text-[11px] text-center text-slate-400">
                🛡️ অ্যাডমিন ড্যাশবোর্ড মোড সক্রিয়। সমস্ত গেমপ্লে মেকানিজম এবং লাভ-ক্ষতির হার মালিকের কন্ট্রোল প্যানেল দ্বারা নির্ধারিত।
            </div>
        </section>

    </main>

    <!-- ================= GAME MODAL INTERACTIVE SYSTEM ================= -->
    <div id="game-modal" class="game-overlay fixed inset-0 z-50 hidden flex flex-col max-w-md mx-auto">
        <div class="bg-slate-900 px-4 py-3 flex justify-between items-center border-b border-slate-800">
            <h3 id="modal-game-title" class="text-sm font-bold text-emerald-400">গেম লোড হচ্ছে...</h3>
            <button onclick="closeGame()" class="text-white bg-rose-600 hover:bg-rose-700 px-3 py-1 rounded-lg text-xs font-bold transition">গেম থেকে বের হন</button>
        </div>
        
        <div class="flex-1 flex flex-col justify-center items-center p-4">
            
            <!-- AVIATOR GAME ENGINE UI -->
            <div id="engine-aviator" class="w-full hidden space-y-4">
                <div id="aviator-canvas" class="w-full h-48 rounded-xl border border-rose-500/30 flex flex-col justify-between p-3">
                    <div class="flex justify-between items-center">
                        <span class="text-xs text-rose-500 font-bold font-mono">Live Multiplier</span>
                        <span id="aviator-status" class="text-[10px] bg-emerald-600 text-slate-950 px-1.5 py-0.2 rounded font-bold">READY TO FLY</span>
                    </div>
                    <div id="aviator-mult" class="text-center text-4xl font-black text-rose-500 font-mono my-auto">1.00x</div>
                    <div class="text-[10px] text-slate-400 text-center">প্লেনটি ক্র্যাশ (Crash) করার আগে ক্যাশআউট করুন!</div>
                    <div id="aviator-plane" class="plane">🚀</div>
                </div>
                <div class="bg-slate-900 p-3 rounded-xl border border-slate-800 space-y-2.5">
                    <div class="flex justify-between text-xs text-slat
