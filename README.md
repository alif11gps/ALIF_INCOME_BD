<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ALIF_INCOME_BD - অফিসিয়াল আর্নিং প্ল্যাটফর্ম</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #f1f5f9;
            color: #1e293b;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="max-w-md mx-auto bg-slate-50 min-h-screen flex flex-col shadow-2xl relative">

    <!-- ================= APP HEADER ================= -->
    <header class="bg-white border-b border-slate-200 px-4 py-3 flex items-center justify-between sticky top-0 z-50 shadow-sm">
        <div class="flex items-center gap-2">
            <div class="w-7 h-7 bg-indigo-600 rounded-lg flex items-center justify-center text-white text-sm font-bold">💼</div>
            <span class="text-base font-black text-slate-800 tracking-wider">ALIF_INCOME_BD</span>
        </div>
        
        <!-- Balance Area -->
        <div class="flex items-center gap-2">
            <div class="bg-indigo-50 px-3 py-1 rounded-full border border-indigo-100 flex items-center gap-1.5">
                <span class="text-indigo-600 text-xs font-bold">৳</span>
                <span id="nav-balance" class="font-bold text-indigo-700 text-sm">0.00</span>
            </div>
            <div class="w-8 h-8 rounded-full bg-slate-200 flex items-center justify-center font-bold text-slate-700 text-xs border border-slate-300">
                MD
            </div>
        </div>
    </header>

    <!-- ================= MAIN CONTENT AREA ================= -->
    <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-4 pb-24 space-y-4">
        
        <!-- --- TAB 1: হোম ড্যাশবোর্ড --- -->
        <section id="home" class="tab-content active space-y-4">
            <!-- User Summary Profile Card -->
            <div class="bg-white p-4 rounded-3xl border border-slate-100 shadow-sm flex items-center justify-between">
                <div class="flex items-center gap-3">
                    <div class="w-12 h-12 rounded-full border-2 border-indigo-500 p-0.5">
                        <div class="w-full h-full rounded-full bg-indigo-100 flex items-center justify-center text-lg">👤</div>
                    </div>
                    <div>
                        <div class="flex items-center gap-1">
                            <h3 class="font-bold text-slate-800 text-sm">MD</h3>
                            <span class="text-blue-500 text-xs">✓</span>
                        </div>
                        <p class="text-[11px] text-slate-400">মেম্বার প্রোফাইল</p>
                    </div>
                </div>
                <button onclick="switchTab('member')" class="bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold px-3 py-1.5 rounded-xl transition">
                    Log Out
                </button>
            </div>

            <!-- Modern Balance Card -->
            <div class="bg-gradient-to-br from-indigo-700 via-indigo-800 to-slate-900 p-6 rounded-3xl text-white shadow-md relative overflow-hidden">
                <p class="text-indigo-200 text-xs font-semibold tracking-wide">বর্তমান ব্যালেন্স</p>
                <h2 class="text-4xl font-black mt-2 flex items-baseline gap-1">
                    <span class="text-2xl font-bold">৳</span><span id="main-balance">0.00</span>
                </h2>
                <div class="absolute right-4 bottom-4 opacity-10 text-6xl">💸</div>
            </div>

            <!-- Quick Task Counter Row -->
            <div class="grid grid-cols-2 gap-3">
                <div class="bg-white p-3.5 rounded-2xl border border-slate-100 shadow-sm flex items-center gap-3">
                    <div class="w-10 h-10 bg-indigo-50 text-indigo-600 rounded-xl flex items-center justify-center text-lg font-bold">⚡</div>
                    <div>
                        <span class="text-[11px] text-slate-400 block font-semibold">আজকের টাস্ক</span>
                        <span class="text-base font-bold text-slate-800">0 / 15</span>
                    </div>
                </div>
                <div class="bg-white p-3.5 rounded-2xl border border-slate-100 shadow-sm flex items-center gap-3">
                    <div class="w-10 h-10 bg-emerald-50 text-emerald-600 rounded-xl flex items-center justify-center text-lg font-bold">👥</div>
                    <div>
                        <span class="text-[11px] text-slate-400 block font-semibold">সফল রেফার</span>
                        <span class="text-base font-bold text-slate-800">0</span>
                    </div>
                </div>
            </div>

            <button onclick="switchTab('tasks')" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3.5 rounded-2xl shadow-sm transition active:scale-[0.99]">
                নতুন কাজগুলি দেখুন
            </button>
        </section>

        <!-- --- TAB 2: ভিডিও কাজ (Tasks) --- -->
        <section id="tasks" class="tab-content space-y-4">
            <div class="bg-white border border-slate-100 p-4 rounded-2xl shadow-sm text-center space-y-3">
                <h3 class="text-base font-bold text-slate-800">📹 বিজ্ঞাপন দেখে আয় করুন</h3>
                <p class="text-xs text-slate-500">প্রতিটি বিজ্ঞাপন বা ভিডিও দেখার জন্য আপনি পাবেন নিশ্চিত <span class="text-emerald-600 font-bold">৳১০.০০ ইনকাম</span>।</p>
                
                <div class="bg-indigo-50 text-indigo-700 font-semibold text-xs py-2 px-4 rounded-xl inline-block">
                    🎁 রিওয়ার্ড: ৳১০.০০ টাকা
                </div>

                <!-- Progress Bar -->
                <div class="space-y-1.5 pt-2">
                    <div class="flex justify-between text-[11px] font-bold text-slate-500">
                        <span>আজকের টাস্ক সম্পন্ন</span>
                        <span>0 / 15</span>
                    </div>
                    <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden">
                        <div class="bg-indigo-600 h-full w-[0%]"></div>
                    </div>
                </div>

                <button onclick="alert('ভিডিও লোড হচ্ছে... অনুগ্রহ করে ১০ সেকেন্ড অপেক্ষা করুন।')" class="w-full bg-rose-500 hover:bg-rose-600 text-white font-bold py-3 rounded-xl shadow-sm transition mt-2">
                    বিজ্ঞাপন দেখুন
                </button>
            </div>

            <!-- Official Telegram Card -->
            <div class="bg-white border border-slate-100 p-4 rounded-2xl shadow-sm flex items-center justify-between">
                <div class="flex items-center gap-3">
                    <div class="w-10 h-10 bg-sky-100 text-sky-600 rounded-full flex items-center justify-center text-xl">📢</div>
                    <div>
                        <h4 class="text-xs font-bold text-slate-800 uppercase">ALIF_INCOME_BD OFFICIAL</h4>
                        <p class="text-[11px] text-slate-400">পুরস্কার: ৳৫০.০০ বোনাস</p>
                    </div>
                </div>
                <button class="bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold px-4 py-2 rounded-xl transition">
                    সম্পন্ন
                </button>
            </div>
        </section>

        <!-- --- TAB 3: রেফার (Invite) --- -->
        <section id="invite" class="tab-content space-y-4">
            <div class="bg-slate-900 text-white p-5 rounded-3xl space-y-4 shadow-lg relative">
                <div class="space-y-1.5">
                    <h3 class="text-lg font-bold text-white">বন্ধুকে রেফার করুন এবং আয় করুন</h3>
                    <p class="text-xs text-slate-400 leading-relaxed">আপনার রেফার লিংকটি শেয়ার করুন এবং আপনার বন্ধুদের আমন্ত্রণ জানান। আপনার বন্ধু সাইন আপ করলেই আপনি <span class="text-amber-400 font-bold">৳৫০.০০ TAKA</span> বোনাস পাবেন।</p>
                </div>
                
                <div class="bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-xs py-2 px-4 rounded-xl inline-block font-bold">
                    😊 প্রতি রেফারে ৳৫০.০০ TAKA বোনাস
                </div>

                <!-- Referral Link Box -->
                <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 flex justify-between items-center gap-2">
                    <span class="text-xs font-mono text-slate-300 overflow-hidden truncate">https://t.me/AlifIncomeBdBot?start=ref</span>
                    <button onclick="alert('লিংক কপি হয়েছে!')" class="p-2 bg-fuchsia-600 text-white rounded-lg text-xs font-bold shrink-0">📋</button>
                </div>

                <div class="grid grid-cols-2 gap-3 pt-2">
                    <button onclick="alert('লিংক কপি হয়েছে!')" class="bg-gradient-to-r from-pink-600 to-rose-600 text-white text-xs font-bold py-2.5 rounded-xl">লিংক কপি করুন</button>
                    <button class="bg-indigo-600 text-white text-xs font-bold py-2.5 rounded-xl">শেয়ার করুন</button>
                </div>
            </div>

            <!-- Referral Stats -->
            <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm flex justify-between items-center">
                <span class="text-xs font-bold text-slate-700">রেফার করা বন্ধুদের তালিকা</span>
                <span class="text-xs bg-indigo-50 text-indigo-600 px-2.5 py-1 rounded-full font-bold">মোট: 0</span>
            </div>
        </section>

        <!-- --- TAB 4: ওয়ালেট ও উইথড্র (Wallet) --- -->
        <section id="wallet" class="tab-content space-y-4">
            <!-- Top Withdraw Action Button -->
            <button onclick="document.getElementById('withdraw-modal').classList.remove('hidden')" class="w-full bg-gradient-to-r from-indigo-500 to-purple-600 text-white font-bold py-3.5 rounded-2xl shadow flex items-center justify-center gap-2 text-sm">
                <span>💰</span> উত্তোলন করুন
            </button>

            <!-- Quick Grid Menu Layout -->
            <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm space-y-3">
                <h4 class="text-xs font-bold text-slate-400 uppercase tracking-wider">মেনু</h4>
                <div class="grid grid-cols-2 gap-2 text-xs font-bold text-slate-700">
                    <div class="p-3 bg-slate-50 rounded-xl flex items-center gap-2 cursor-pointer hover:bg-slate-100"><span class="text-indigo-500">🕒</span> লেনদেনের ইতিহাস</div>
                    <div class="p-3 bg-slate-50 rounded-xl flex items-center gap-2 cursor-pointer hover:bg-slate-100"><span class="text-emerald-500">ℹ️</span> সহায়তা</div>
                    <div class="p-3 bg-slate-50 rounded-xl flex items-center gap-2 cursor-pointer hover:bg-slate-100"><span class="text-rose-500">📈</span> উত্তোলনের ইতিহাস</div>
                    <div class="p-3 bg-slate-50 rounded-xl flex items-center gap-2 cursor-pointer hover:bg-slate-100"><span class="text-amber-500">🏆</span> লিডারবোর্ড</div>
                </div>
            </div>

            <!-- Withdraw Rules Card -->
            <div class="bg-amber-50/60 border border-amber-200/60 p-4 rounded-2xl space-y-2.5">
                <h4 class="text-xs font-bold text-amber-800 flex items-center gap-1">⚠️ উত্তোলনের শর্তাবলী</h4>
                <p class="text-[11px] text-amber-700 leading-relaxed">ALIF_INCOME_BD প্ল্যাটফর্ম থেকে টাকা উত্তোলনের জন্য আপনার অ্যাকাউন্টে সর্বনিম্ন <span class="font-bold">৳১৫০০.০০ টাকা</span> ব্যালেন্স থাকতে হবে। প্রতি ভিডিওর জন্য ১০ টাকা এবং রেফারেল বোনাস সরাসরি মূল ব্যালেন্সে যোগ হবে।</p>
            </div>
        </section>

        <!-- --- TAB 5: কাস্টমার সাপোর্ট --- -->
        <section id="support" class="tab-content space-y-4 text-center py-6">
            <div class="bg-white border border-slate-100 p-6 rounded-3xl shadow-sm space-y-4">
                <h3 class="text-base font-bold text-slate-800">সাহায্য প্রয়োজন?</h3>
                <div class="w-full bg-rose-500 text-white p-6 rounded-2xl space-y-3 relative overflow-hidden">
                    <div class="text-4xl">✈️</div>
                    <h4 class="text-lg font-black">কাস্টমার সার্ভিস</h4>
                    <p class="text-xs text-rose-100">যেকোনো সমস্যা সমাধানের জন্য আমাদের সাথে যোগাযোগ করুন</p>
                    <div class="bg-white text-slate-900 py-2 px-4 rounded-xl font-bold inline-block text-xs mt-1">
                        @AlifIncomeBDSupport
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- ================= WITHDRAWAL MODAL SYSTEM ================= -->
    <div id="withdraw-modal" class="fixed inset-0 bg-black/50 z-50 hidden flex items-end justify-center max-w-md mx-auto">
        <div class="bg-white w-full rounded-t-3xl p-5 space-y-4 shadow-2xl animate-slide-up">
            <div class="flex justify-between items-center border-b border-slate-100 pb-3">
                <h3 class="text-base font-bold text-slate-800">📤 ব্যালেন্স উত্তোলন (Withdraw)</h3>
                <button onclick="document.getElementById('withdraw-modal').classList.add('hidden')" class="text-slate-400 font-bold text-lg hover:text-slate-600">✕</button>
            </div>

            <!-- Withdraw Notice -->
            <div class="bg-indigo-50 border border-indigo-100 p-3 rounded-xl text-[11px] text-indigo-700 leading-relaxed">
                📌 অন্তত <strong>১৫টি টাস্ক</strong> সম্পন্ন করতে হবে। সর্বনিম্ন উইথড্র পরিমাণ <strong>৳১৫০০</strong> টাকা।
            </div>

            <!-- Payment gateway selection -->
            <div class="space-y-3 text-xs">
                <div>
                    <label class="text-slate-500 font-bold block mb-1">পেইমেন্ট মেথড</label>
                    <select class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-3 text-slate-700 font-bold outline-none focus:border-indigo-500 text-sm">
                        <option value="বিকাশ">বিকাশ (Bkash)</option>
                        <option value="নগদ">নগদ (Nagad)</option>
                    </select>
                </div>
                <div>
                    <label class="text-slate-500 font-bold block mb-1">উত্তোলন নাম্বার / বিকাশ নম্বর</label>
                    <input type="text" placeholder="আপনার ফোন নম্বরটি লিখুন" class="w-full bg-slate-50 border border-slate-200 text-slate-700 font-bold rounded-xl px-3 py-3 outline-none focus:border-indigo-500 text-sm">
                </div>
                <div>
                    <label class="text-slate-500 font-bold block mb-1">পরিমাণ (৳)</label>
                    <input type="number" placeholder="নূন্যতম ৳১৫০০" class="w-full bg-slate-50 border border-slate-200 text-indigo-600 font-bold rounded-xl px-3 py-3 outline-none focus:border-indigo-500 text-sm">
                </div>
            </div>

            <button onclick="alert('আপনার ব্যালেন্স পর্যাপ্ত নয়!')" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3.5 rounded-xl text-sm transition">
                উত্তোলন রিকোয়েস্ট পাঠান
            </button>
        </div>
    </div>

    <!-- ================= APP NAVIGATION BOTTOM BAR ================= -->
    <nav class="fixed bottom-0 left-0 right-0 max-w-md mx-auto bg-white border-t border-slate-200 px-2 py-2 flex justify-around items-center z-50 shadow-[0_-2px_10px_rgba(0,0,0,0.03)]">
        <button onclick="switchTab('home')" class="nav-btn flex flex-col items-center gap-1 text-indigo-600 font-bold text-[10px] flex-1">
            <span class="text-lg">🏠</span> হোম
        </button>
        <button onclick="switchTab('tasks')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
            <span class="text-lg">📋</span> কাজ
        </button>
        <button onclick="switchTab('invite')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
            <span class="text-lg">👥</span> রেফার
        </button>
        <button onclick="switchTab('wallet')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
            <span class="text-lg">💳</span> ওয়ালেট
        </button>
        <button onclick="switchTab('support')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
            <span class="text-lg">🎧</span> সাপোর্ট
        </button>
    </nav>

    <!-- ================= JAVASCRIPT TAB NAVIGATION SYSTEM ================= -->
    <script>
        function switchTab(tabId) {
            // Hide all tabs
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            // Show target tab
            document.getElementById(tabId).classList.add('active');
            
            // Reset nav colors
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('text-indigo-600');
                btn.classList.add('text-slate-400');
            });
            
            // Highlight active navigation button
            const activeIndex = { 'home': 0, 'tasks': 1, 'invite': 2, 'wallet': 3, 'support': 4 }[tabId];
            if(activeIndex !== undefined) {
                document.querySelectorAll('.nav-btn')[activeIndex].classList.add('text-indigo-600');
                document.querySelectorAll('.nav-btn')[activeIndex].classList.remove('text-slate-400');
            }
        }
    </script>
</body>
</html>
