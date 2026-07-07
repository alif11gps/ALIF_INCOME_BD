<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ALIF_INCOME_BD - অফিসিয়াল আর্নিং প্ল্যাটফর্ম</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #0f172a;
            color: #1e293b;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            overflow: hidden;
        }
        /* মোবাইল স্ক্রিন সাইজ লক করার জন্য ফিক্সড কন্টেইনার */
        .app-container {
            width: 100%;
            max-width: 420px;
            height: 100vh;
            max-height: 850px;
            background-color: #f8fafc;
            display: flex;
            flex-direction: column;
            position: relative;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
            border-radius: 0px;
        }
        @media (min-width: 450px) {
            .app-container {
                border-radius: 30px;
                border: 8px solid #334155;
                height: 90vh;
            }
        }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body>

    <!-- ================= MAIN APP CONTAINER ================= -->
    <div class="app-container">

        <!-- ================= APP HEADER ================= -->
        <header class="bg-white border-b border-slate-200 px-4 py-3 flex items-center justify-between sticky top-0 z-50 shadow-sm shrink-0">
            <div class="flex items-center gap-2">
                <div class="w-7 h-7 bg-indigo-600 rounded-lg flex items-center justify-center text-white text-sm font-bold">💼</div>
                <span class="text-base font-black text-slate-800 tracking-wider">ALIF_INCOME_BD</span>
            </div>
            
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
                    <button class="bg-slate-100 text-slate-700 text-xs font-bold px-3 py-1.5 rounded-xl">
                        Log Out
                    </button>
                </div>

                <div class="bg-gradient-to-br from-indigo-700 via-indigo-800 to-slate-900 p-6 rounded-3xl text-white shadow-md relative overflow-hidden">
                    <p class="text-indigo-200 text-xs font-semibold tracking-wide">বর্তমান ব্যালেন্স</p>
                    <h2 class="text-4xl font-black mt-2 flex items-baseline gap-1">
                        <span class="text-2xl font-bold">৳</span><span>0.00</span>
                    </h2>
                    <div class="absolute right-4 bottom-4 opacity-10 text-6xl">💸</div>
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-white p-3.5 rounded-2xl border border-slate-100 shadow-sm flex items-center gap-3">
                        <div class="w-10 h-10 bg-indigo-50 text-indigo-600 rounded-xl flex items-center justify-center text-lg font-bold">⚡</div>
                        <div>
                            <span class="text-[11px] text-slate-400 block font-semibold">মোট ভিডিও টাস্ক</span>
                            <span class="text-base font-bold text-slate-800">0 / 200</span>
                        </div>
                    </div>
                    <div class="bg-white p-3.5 rounded-2xl border border-slate-100 shadow-sm flex items-center gap-3">
                        <div class="w-10 h-10 bg-emerald-50 text-emerald-600 rounded-xl flex items-center justify-center text-lg font-bold">👥</div>
                        <div>
                            <span class="text-[11px] text-slate-400 block font-semibold">সফল রেফার</span>
                            <span class="text-base font-bold text-slate-800">2 / 20</span>
                        </div>
                    </div>
                </div>

                <button onclick="switchTab('tasks')" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3.5 rounded-2xl shadow-sm transition">
                    টাস্ক ওয়ার্ক শুরু করুন
                </button>

                <!-- 🌐 নতুন সংযুক্ত: কোম্পানি পরিচিতি সেকশন -->
                <div class="bg-white border border-slate-100 p-4 rounded-2xl shadow-sm space-y-2.5">
                    <h4 class="text-xs font-bold text-slate-800 uppercase tracking-wider flex items-center gap-1">🏢 আমাদের কোম্পানি পরিচিতি</h4>
                    <p class="text-xs text-slate-600 leading-relaxed">
                        <strong class="text-indigo-600">ALIF_INCOME_BD</strong> হলো একটি আধুনিক **ডিজিটাল অ্যাডভার্টাইজিং এবং মাইক্রো-টাস্কিং প্ল্যাটফর্ম**। আমরা বিশ্বের বিভিন্ন নামী-দামী ব্র্যান্ডের বিজ্ঞাপন প্রচার ও প্রোমোশনের কাজ করে থাকি। আমাদের ব্যবহারকারীরা এখানে সহজ কিছু ডিজিটাল টাস্ক (যেমন: বিজ্ঞাপন দেখা, রেফার করা) সম্পন্ন করে ঘরে বসেই পার্ট-টাইম ইনকাম করতে পারেন।
                    </p>
                </div>
            </section>

            <!-- --- TAB 2: ভিডিও কাজ (Tasks) --- -->
            <section id="tasks" class="tab-content space-y-4">
                <div class="bg-white border border-slate-100 p-4 rounded-2xl shadow-sm text-center space-y-3">
                    <h3 class="text-base font-bold text-slate-800">📹 বিজ্ঞাপন দেখে আয়</h3>
                    <p class="text-xs text-slate-500">প্রতিটি ভিডিওর জন্য আপনি পাবেন নিশ্চিত <span class="text-emerald-600 font-bold">৳১০.০০ ইনকাম</span>। প্রতিদিন ১৫টি করে টাস্ক পাবেন।</p>
                    
                    <div class="bg-indigo-50 text-indigo-700 font-semibold text-xs py-2 px-4 rounded-xl inline-block">
                        🎁 রিওয়ার্ড: ৳১০.০০ টাকা
                    </div>

                    <div class="space-y-1.5 pt-2">
                        <div class="flex justify-between text-[11px] font-bold text-slate-500">
                            <span>আজকের ভিডিও সম্পন্ন</span>
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
            </section>

            <!-- --- TAB 3: রেফার ও লাইভ হিস্টরি (Invite & Live History) --- -->
            <section id="invite" class="tab-content space-y-4">
                <div class="bg-slate-900 text-white p-5 rounded-3xl space-y-4 shadow-lg">
                    <div class="space-y-1.5">
                        <h3 class="text-lg font-bold text-white">বন্ধুকে রেফার করুন</h3>
                        <p class="text-xs text-slate-400 leading-relaxed">আপনার রেফার লিংক শেয়ার করুন। বন্ধু সাইন আপ করলেই আপনার অ্যাকাউন্টে <span class="text-amber-400 font-bold">৳৫০.০০ TAKA</span> বোনাস যোগ হবে।</p>
                    </div>
                    
                    <div class="bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-xs py-2 px-4 rounded-xl inline-block font-bold">
                        😊 প্রতি রেফারে ৳৫০.০০ TAKA বোনাস
                    </div>

                    <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 flex justify-between items-center gap-2">
                        <span class="text-xs font-mono text-slate-300 overflow-hidden truncate">https://t.me/AlifIncomeBdBot?start=ref</span>
                        <button onclick="alert('লিংক কপি হয়েছে!')" class="p-2 bg-fuchsia-600 text-white rounded-lg text-xs font-bold shrink-0">📋</button>
                    </div>
                </div>

                <!-- 👥 নতুন সংযুক্ত: আমন্ত্রিত বন্ধুদের লাইভ হিস্টরি ও কাজের অগ্রগতি -->
                <div class="bg-white border border-slate-200 rounded-2xl p-4 shadow-sm space-y-3">
                    <div class="flex justify-between items-center border-b border-slate-100 pb-2">
                        <div>
                            <h4 class="text-xs font-bold text-slate-800 uppercase tracking-wider">📊 আমন্ত্রিত মেম্বারদের কাজের হিস্টরি</h4>
                            <p class="text-[10px] text-slate-400">কারা যুক্ত হয়েছে এবং বর্তমানে কাজ করছে</p>
                        </div>
                        <span class="bg-indigo-50 text-indigo-600 text-xs font-bold px-2.5 py-1 rounded-full">মোট: ২ জন</span>
                    </div>

                    <!-- লাইভ হিস্টরি লিস্ট -->
                    <div class="space-y-2">
                        <!-- মেম্বার ১ (অ্যাক্টিভ) -->
                        <div class="flex items-center justify-between p-2.5 bg-slate-50 border border-slate-100 rounded-xl">
                            <div class="flex items-center gap-2.5">
                                <div class="w-8 h-8 rounded-full bg-emerald-100 flex items-center justify-center text-xs font-bold text-emerald-700">RA</div>
                                <div>
                                    <h5 class="text-xs font-bold text-slate-700">Rakib Ahmed</h5>
                                    <p class="text-[10px] text-slate-400">আইডি: #584920</p>
                                </div>
                            </div>
                            <div class="text-right">
                                <span class="bg-emerald-100 text-emerald-700 text-[9px] font-bold px-2 py-0.5 rounded-full block text-center mb-1">কাজ করতেছে</span>
                                <p class="text-[9px] text-slate-500">টাস্ক সম্পন্ন: ১৫/১৫</p>
                            </div>
                        </div>

                        <!-- েব্বার ২ (পেন্ডিং/বাকি) -->
                        <div class="flex items-center justify-between p-2.5 bg-slate-50 border border-slate-100 rounded-xl">
                            <div class="flex items-center gap-2.5">
                                <div class="w-8 h-8 rounded-full bg-amber-100 flex items-center justify-center text-xs font-bold text-amber-700">SI</div>
                                <div>
                                    <h5 class="text-xs font-bold text-slate-700">Sabbir Islam</h5>
                                    <p class="text-[10px] text-slate-400">আইডি: #584115</p>
                                </div>
                            </div>
                            <div class="text-right">
                                <span class="bg-amber-100 text-amber-700 text-[9px] font-bold px-2 py-0.5 rounded-full block text-center mb-1">কাজ বাকি আছে</span>
                                <p class="text-[9px] text-slate-400">টাস্ক সম্পন্ন: ০/১৫</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- --- TAB 4: ওয়ালেট ও উইথড্র (Wallet) --- -->
            <section id="wallet" class="tab-content space-y-4">
                <button onclick="document.getElementById('withdraw-modal').classList.remove('hidden')" class="w-full bg-gradient-to-r from-indigo-500 to-purple-600 text-white font-bold py-3.5 rounded-2xl shadow flex items-center justify-center gap-2 text-sm">
                    <span>💰</span> উত্তোলন করুন
                </button>

                <!-- উত্তোলনের নতুন শর্তাবলী কার্ড -->
                <div class="bg-amber-50 border border-amber-200 p-4 rounded-2xl space-y-3">
                    <h4 class="text-xs font-bold text-amber-800 flex items-center gap-1">⚠️ উত্তোলনের শর্তাবলী (ALIF_INCOME_BD)</h4>
                    <p class="text-[11px] text-amber-700 leading-relaxed">টাকা উইথড্র করার জন্য নিচে দেওয়া যেকোনো **একটি শর্ত** অবশ্যই পূরণ করতে হবে:</p>
                    
                    <ul class="text-[11px] text-slate-600 space-y-1.5 list-disc pl-4 font-semibold">
                        <li>অন্তরূণ <span class="text-indigo-600 font-bold">২০০টি বিজ্ঞাপন/ভিডিও</span> দেখতে হবে। (আপনার বর্তমান: 0/200)</li>
                        <li><span class="text-slate-800 font-bold">অথবা</span> অন্তত <span class="text-emerald-600 font-bold">২০টি সফল রেফার</span> করতে হবে। (আপনার বর্তমান: 2/20)</li>
                        <li>সর্বনিম্ন উত্তোলনের পরিমাণ: <span class="text-rose-600 font-bold">৳১৫০০.০০ টাকা</span>।</li>
                    </ul>
                </div>
            </section>

            <!-- --- TAB 5: কাস্টমার সাপোর্ট --- -->
            <section id="support" class="tab-content space-y-4 text-center py-6">
                <div class="bg-white border border-slate-100 p-6 rounded-3xl shadow-sm space-y-4">
                    <h3 class="text-base font-bold text-slate-800">সাহায্য প্রয়োজন?</h3>
                    <div class="w-full bg-rose-500 text-white p-6 rounded-2xl space-y-3">
                        <div class="text-4xl">✈️</div>
                        <h4 class="text-lg font-black">কাস্টমার সার্ভিস</h4>
                        <p class="text-xs text-rose-100">যেকোনো সমস্যা সমাধানের জন্য টেলিগ্রামে যোগাযোগ করুন</p>
                        <div class="bg-white text-slate-900 py-2 px-4 rounded-xl font-bold inline-block text-xs mt-1">
                            @AlifIncomeBDSupport
                        </div>
                    </div>
                </div>
            </section>

        </main>

        <!-- ================= WITHDRAWAL MODAL SYSTEM ================= -->
        <div id="withdraw-modal" class="absolute inset-0 bg-black/50 z-50 hidden flex items-end justify-center">
            <div class="bg-white w-full rounded-t-3xl p-5 space-y-4 shadow-2xl">
                <div class="flex justify-between items-center border-b border-slate-100 pb-3">
                    <h3 class="text-base font-bold text-slate-800">📤 ব্যালেন্স উত্তোলন (Withdraw)</h3>
                    <button onclick="document.getElementById('withdraw-modal').classList.add('hidden')" class="text-slate-400 font-bold text-lg">✕</button>
                </div>

                <div class="space-y-3 text-xs">
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">পেইমেন্ট মেথড</label>
                        <select class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-3 text-slate-700 font-bold outline-none text-sm">
                            <option value="বিকাশ">বিকাশ (Bkash)</option>
                            <option value="নগদ">নগদ (Nagad)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">উত্তোলন নাম্বার</label>
                        <input type="text" placeholder="আপনার ফোন নম্বরটি লিখুন" class="w-full bg-slate-50 border border-slate-200 text-slate-700 font-bold rounded-xl px-3 py-3 outline-none text-sm">
                    </div>
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">পরিমাণ (৳)</label>
                        <input type="number" placeholder="নূন্যতম ৳১৫০০" class="w-full bg-slate-50 border border-slate-200 text-indigo-600 font-bold rounded-xl px-3 py-3 outline-none text-sm">
                    </div>
                </div>

                <button onclick="alert('উত্তোলনের শর্ত (২০০ ভিডিও অথবা ২০ রেফার) পূরণ হয়নি!')" class="w-full bg-indigo-600 text-white font-bold py-3.5 rounded-xl text-sm">
                    উত্তোলন রিকোয়েস্ট পাঠান
                </button>
            </div>
        </div>

        <!-- ================= APP NAVIGATION BOTTOM BAR ================= -->
        <nav class="absolute bottom-0 left-0 right-0 bg-white border-t border-slate-200 px-2 py-2 flex justify-around items-center z-50 shadow-[0_-2px_10px_rgba(0,0,0,0.03)] shrink-0">
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

    </div>

    <!-- ================= JAVASCRIPT TAB SYSTEM ================= -->
    <script>
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('text-indigo-600');
                btn.classList.add('text-slate-400');
            });
            
            const activeIndex = { 'home': 0, 'tasks': 1, 'invite': 2, 'wallet': 3, 'support': 4 }[tabId];
            if(activeIndex !== undefined) {
                document.querySelectorAll('.nav-btn')[activeIndex].classList.add('text-indigo-600');
                document.querySelectorAll('.nav-btn')[activeIndex].classList.remove('text-slate-400')
