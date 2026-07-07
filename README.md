<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ALIF_INCOME_BD</title>
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
        .app-container {
            width: 100%;
            max-width: 420px;
            height: 100vh;
            max-height: 850px;
            background-color: #f3f4f6;
            display: flex;
            flex-direction: column;
            position: relative;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
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

    <div class="app-container">

        <!-- ================= APP HEADER ================= -->
        <header class="bg-white px-4 py-4 flex flex-col items-center justify-center sticky top-0 z-50 shrink-0">
            <div class="w-14 h-14 bg-gradient-to-b from-indigo-500 to-indigo-800 rounded-2xl flex items-center justify-center text-white text-2xl shadow-md">💼</div>
            <span class="text-xl font-black text-slate-800 tracking-wider mt-2">ALIF_INCOME_BD</span>
        </header>

        <!-- ================= MAIN CONTENT AREA ================= -->
        <main class="flex-1 overflow-y-auto no-scrollbar px-4 py-2 pb-24 space-y-4">
            
            <!-- --- TAB 1: হোম ড্যাশবোর্ড --- -->
            <section id="home" class="tab-content active space-y-4">
                <!-- প্রোফাইল কার্ড -->
                <div class="bg-white p-3 rounded-2xl border border-slate-100 flex items-center justify-between shadow-sm">
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-full border-2 border-indigo-500 p-0.5 overflow-hidden">
                            <div class="w-full h-full rounded-full bg-indigo-100 flex items-center justify-center text-lg font-bold text-indigo-700">MD</div>
                        </div>
                        <div>
                            <div class="flex items-center gap-1">
                                <h3 class="font-bold text-slate-800 text-sm">MD</h3>
                                <span class="bg-indigo-600 text-white rounded-full w-3.5 h-3.5 flex items-center justify-center text-[8px]">✓</span>
                            </div>
                            <p class="text-[11px] text-slate-400">অফিসিয়াল প্রোফাইল</p>
                        </div>
                    </div>
                    <div class="w-8 h-8 rounded-full bg-slate-100 flex items-center justify-center text-slate-600 relative cursor-pointer">
                        🔔<span class="absolute top-1 right-1 w-2 h-2 bg-rose-500 rounded-full"></span>
                    </div>
                </div>

                <!-- ব্যালেন্স কার্ড -->
                <div class="bg-gradient-to-br from-indigo-700 via-indigo-800 to-slate-900 p-6 rounded-3xl text-white shadow-md relative overflow-hidden">
                    <p class="text-indigo-200 text-xs font-semibold tracking-wide">বর্তমান ব্যালেন্স</p>
                    <h2 class="text-5xl font-black mt-2 flex items-baseline gap-1">
                        <span class="text-3xl font-bold">৳</span><span id="main-balance">0.00</span>
                    </h2>
                </div>

                <!-- কুইক টাস্ক গ্রিড -->
                <h4 class="text-xs font-bold text-slate-500 uppercase tracking-wider pl-1">দ্রুত টাস্ক</h4>
                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm flex flex-col justify-between h-24">
                        <div class="w-8 h-8 bg-indigo-50 text-indigo-600 rounded-xl flex items-center justify-center text-sm font-bold">⚡</div>
                        <div>
                            <span class="text-[11px] text-slate-400 block font-semibold">আজকের টাস্ক</span>
                            <span id="task-count-view" class="text-base font-bold text-slate-800">0 / 15</span>
                        </div>
                    </div>
                    <div class="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm flex flex-col justify-between h-24">
                        <div class="w-8 h-8 bg-emerald-50 text-emerald-600 rounded-xl flex items-center justify-center text-sm font-bold">👥</div>
                        <div>
                            <span class="text-[11px] text-slate-400 block font-semibold">সফল রেফার</span>
                            <span id="refer-count-view" class="text-base font-bold text-slate-800">0 / 20</span>
                        </div>
                    </div>
                </div>

                <button onclick="switchTab('tasks')" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3.5 rounded-2xl shadow-sm transition text-sm">
                    টাস্ক ওয়ার্ক শুরু করুন
                </button>
            </section>

            <!-- --- TAB 2: ভিডিও কাজ (Tasks) --- -->
            <section id="tasks" class="tab-content space-y-4">
                <div class="bg-white border border-slate-100 p-5 rounded-2xl shadow-sm text-center space-y-4">
                    <h3 class="text-base font-bold text-slate-800">📹 বিজ্ঞাপন দেখে আয়</h3>
                    <p class="text-xs text-slate-500 leading-relaxed">প্রতিটি ভিডিও বিজ্ঞাপন দেখার জন্য আপনি পাবেন নিশ্চিত <span class="text-emerald-600 font-bold">৳১০.০০ ইনকাম</span>। প্রতিদিন ১৫টি করে টাস্ক দেওয়া হবে।</p>
                    
                    <div class="bg-indigo-50 text-indigo-700 font-bold text-xs py-2 px-4 rounded-xl inline-block">
                        💵 রিওয়ার্ড: ৳১০.০০ টাকা
                    </div>

                    <div class="space-y-1.5 pt-2 text-left">
                        <div class="flex justify-between text-[11px] font-bold text-slate-500">
                            <span>আজকের ভিডিও সম্পন্ন</span>
                            <span id="today-task-text">0 / 15</span>
                        </div>
                        <div class="w-full bg-slate-100 h-2 rounded-full overflow-hidden">
                            <div id="task-progress" class="bg-indigo-600 h-full w-[0%] transition-all duration-300"></div>
                        </div>
                    </div>

                    <button onclick="watchAd()" class="w-full bg-rose-500 hover:bg-rose-600 text-white font-bold py-3 rounded-xl shadow-sm transition text-sm">
                        বিজ্ঞাপন দেখুন
                    </button>
                </div>
            </section>

            <!-- --- TAB 3: রেফার (Invite) --- -->
            <section id="invite" class="tab-content space-y-4">
                <div class="bg-slate-900 text-white p-5 rounded-3xl space-y-4 shadow-lg">
                    <div class="space-y-1.5">
                        <h3 class="text-base font-bold text-white">বন্ধুকে রেফার করুন এবং আয় করুন</h3>
                        <p class="text-xs text-slate-400 leading-relaxed">আপনার রেফার লিংকটি শেয়ার করুন এবং আপনার বন্ধুদের আমন্ত্রণ জানান। বন্ধু সাইন আপ করলেই আপনার অ্যাকাউন্টে <span class="text-amber-400 font-bold">৳৫০.০০ TAKA</span> বোনাস পাবেন।</p>
                    </div>
                    
                    <div class="bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-xs py-2 px-4 rounded-xl inline-block font-bold">
                        🎁 প্রতি রেফারে ৳৫০.০০ TAKA বোনাস
                    </div>

                    <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 flex justify-between items-center gap-2">
                        <span class="text-xs font-mono text-slate-300 overflow-hidden truncate">t.me/AlifIncomeBdBot?start=ref</span>
                        <button onclick="alert('লিংক কপি হয়েছে!')" class="p-2 bg-fuchsia-600 text-white rounded-lg text-xs font-bold shrink-0">📋</button>
                    </div>
                </div>

                <!-- ডেমো বাটন রেফার সংখ্যা টেস্ট করার জন্য (ডেভেলপমেন্ট পারপাস) -->
                <div class="bg-white p-3 rounded-xl text-center space-y-2 border border-slate-200">
                    <p class="text-[11px] text-slate-500 font-bold">⚙️ টেস্টিং প্যানেল (রেফার সংখ্যা বাড়ানোর জন্য চাপুন)</p>
                    <div class="flex gap-2">
                        <button onclick="addFakeRefer()" class="flex-1 bg-slate-200 text-slate-700 font-bold text-xs py-1.5 rounded-lg">+১টি রেফার যুক্ত করুন</button>
                        <button onclick="addMaxFake()" class="flex-1 bg-indigo-100 text-indigo-700 font-bold text-xs py-1.5 rounded-lg">সব টাস্ক ও রেফার ফুল করুন</button>
                    </div>
                </div>
            </section>

            <!-- --- TAB 4: ওয়ালেট ও উইথড্র (Wallet) --- -->
            <section id="wallet" class="tab-content space-y-4">
                <button onclick="openWithdrawModal()" class="w-full bg-gradient-to-r from-indigo-500 to-purple-600 text-white font-bold py-3.5 rounded-2xl shadow flex items-center justify-center gap-2 text-sm">
                    <span>💰</span> উত্তোলন করুন
                </button>

                <!-- উত্তোলনের শর্তাবলী কার্ড -->
                <div class="bg-white border border-slate-200 p-4 rounded-2xl space-y-3 shadow-sm">
                    <h4 class="text-xs font-bold text-slate-800 uppercase tracking-wide border-b border-slate-100 pb-2">📋 উত্তোলনের যোগ্যতা ও রেকর্ড</h4>
                    
                    <div class="space-y-2.5">
                        <div class="flex items-start gap-2 text-xs">
                            <span id="cond-video-icon" class="text-rose-500 font-bold">❌</span>
                            <p class="text-slate-600">অন্তত <span class="font-bold text-slate-800">২০০টি ভিডিও</span> দেখতে হবে। <br><span class="text-[11px] text-slate-400">(আপনার বর্তমান: <span id="cond-video-text">0</span>/200)</span></p>
                        </div>
                        <div class="flex items-start gap-2 text-xs">
                            <span id="cond-refer-icon" class="text-rose-500 font-bold">❌</span>
                            <p class="text-slate-600">অন্তত <span class="font-bold text-slate-800">২০টি সফল রেফার</span> করতে হবে। <br><span class="text-[11px] text-slate-400">(আপনার বর্তমান: <span id="cond-refer-text">0</span>/20)</span></p>
                        </div>
                    </div>

                    <div class="bg-slate-50 p-3 rounded-xl border border-slate-100 text-center text-[11px] text-slate-500 font-semibold">
                        সর্বনিম্ন উত্তোলনের পরিমাণ: <span class="text-rose-600 font-bold">৳১৫০০.০০ টাকা</span>
                    </div>
                </div>
            </section>

            <!-- --- TAB 5: কাস্টমার সাপোর্ট --- -->
            <section id="support" class="tab-content space-y-4 text-center py-4">
                <div class="bg-white border border-slate-200 p-6 rounded-3xl shadow-sm space-y-4">
                    <h3 class="text-base font-bold text-slate-800">সাহায্য প্রয়োজন?</h3>
                    <div class="w-full bg-rose-500 text-white p-6 rounded-2xl space-y-2 shadow-md">
                        <div class="text-4xl">✈️</div>
                        <h4 class="text-lg font-black">কাস্টমার সার্ভিস</h4>
                        <p class="text-xs text-rose-100">যেকোনো সমস্যা সমাধানের জন্য সরাসরি টেলিগ্রামে যোগাযোগ করুন</p>
                        <div class="bg-white text-slate-900 py-2 px-5 rounded-xl font-bold inline-block text-xs mt-2 tracking-wide">
                            @AlifIncomeBDSupport
                        </div>
                    </div>
                </div>
            </section>

        </main>

        <!-- ================= WITHDRAWAL MODAL SYSTEM ================= -->
        <div id="withdraw-modal" class="absolute inset-0 bg-black/60 z-50 hidden flex items-end justify-center">
            <div class="bg-white w-full rounded-t-3xl p-5 space-y-4 shadow-2xl transition-all">
                <div class="flex justify-between items-center border-b border-slate-100 pb-3">
                    <h3 class="text-base font-bold text-slate-800">📤 ব্যালেন্স উত্তোলন (Withdraw)</h3>
                    <button onclick="document.getElementById('withdraw-modal').classList.add('hidden')" class="text-slate-400 font-bold text-lg p-1">✕</button>
                </div>

                <div class="space-y-3 text-xs">
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">পেইমেন্ট মেথড</label>
                        <select id="pay-method" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-3 text-slate-700 font-bold outline-none text-sm">
                            <option value="Bkash">বিকাশ (Bkash)</option>
                            <option value="Nagad">নগদ (Nagad)</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">উত্তোলন নাম্বার</label>
                        <input id="pay-number" type="text" placeholder="আপনার ফোন নম্বরটি লিখুন" class="w-full bg-slate-50 border border-slate-200 text-slate-700 font-bold rounded-xl px-3 py-3 outline-none text-sm">
                    </div>
                    <div>
                        <label class="text-slate-500 font-bold block mb-1">পরিমাণ (৳)</label>
                        <input id="pay-amount" type="number" placeholder="নূন্যতম ৳১৫০০" class="w-full bg-slate-50 border border-slate-200 text-indigo-600 font-bold rounded-xl px-3 py-3 outline-none text-sm">
                    </div>
                </div>

                <button onclick="processWithdrawal()" class="w-full bg-indigo-600 text-white font-bold py-3.5 rounded-xl text-sm shadow-md">
                    উত্তোলন রিকোয়েস্ট পাঠান
                </button>
            </div>
        </div>

        <!-- ================= APP NAVIGATION BOTTOM BAR ================= -->
        <nav class="absolute bottom-0 left-0 right-0 bg-white border-t border-slate-200 px-2 py-2 flex justify-around items-center z-50 shadow-[0_-2px_10px_rgba(0,0,0,0.03)] shrink-0">
            <button onclick="switchTab('home')" class="nav-btn flex flex-col items-center gap-1 text-indigo-600 font-bold text-[10px] flex-1">
                <span class="text-lg">🏠</span> Home
            </button>
            <button onclick="switchTab('tasks')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">📋</span> My Jobs
            </button>
            <button onclick="switchTab('invite')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">👥</span> Referral
            </button>
            <button onclick="switchTab('wallet')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">💳</span> Wallet
            </button>
            <button onclick="switchTab('support')" class="nav-btn flex flex-col items-center gap-1 text-slate-400 font-bold text-[10px] flex-1">
                <span class="text-lg">🎧</span> Support
            </button>
        </nav>

    </div>

    <!-- ================= JAVASCRIPT DATA SYSTEM ================= -->
    <script>
        // গ্লোবাল ভ্যারিয়েবল স্টেট মেইনটেইন করার জন্য
        let balance = 0.00;
        let todayTasks = 0;
        let totalVideoWatched = 0;
        let totalRefers = 0;

        function updateUI() {
            document.getElementById('main-balance').innerText = balance.toFixed(2);
            document.getElementById('task-count-view').innerText = todayTasks + " / 15";
            document.getElementById('refer-count-view').innerText = totalRefers + " / 20";
            
            // টাস্ক পেজ আপডেট
            document.getElementById('today-task-text').innerText = todayTasks + " / 15";
            let progressPercent = (todayTasks / 15) * 100;
            document.getElementById('task-progress').style.width = progressPercent + "%";

            // ওয়ালেট পেজ আপডেট
            document.getElementById('cond-video-text').innerText = totalVideoWatched;
            document.getElementById('cond-refer-text').innerText = totalRefers;

            // কন্ডিশনাল টিক বা ক্রস চিহ্ন আপডেট
            if (totalVideoWatched >= 200) {
                document.getElementById('cond-video-icon').innerText = "✓";
                document.getElementById('cond-video-icon').className = "text-emerald-500 font-bold";
            } else {
                document.getElementById('cond-video-icon').innerText = "❌";
                document.getElementById('cond-video-icon').className = "text-rose-500 font-bold";
            }

            if (totalRefers >= 20) {
                document.getElementById('cond-refer-icon').innerText = "✓";
                document.getElementById('cond-refer-icon').className = "text-emerald-500 font-bold";
            } else {
                document.getElementById('cond-refer-icon').innerText = "❌";
                document.getElementById('cond-refer-icon').className = "text-rose-500 font-bold";
            }
        }

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
                document.querySelectorAll('.nav-btn')[activeIndex].classList.remove('text-slate-400');
            }
        }

        function watchAd() {
            if (todayTasks >= 15) {
                alert("আপনার আজকের ১৫টি ভিডিও দেখার লিমিট শেষ! আগামীকাল আবার চেষ্টা করুন।");
                return;
            }
            alert("বিজ্ঞাপন লোড হচ্ছে... অনুগ্রহ করে ৫ সেকেন্ড অপেক্ষা করুন।");
            setTimeout(() => {
                todayTasks++;
                totalVideoWatched++;
                balance += 10;
                updateUI();
                alert("টাস্ক সফল! আপনার অ্যাকাউন্টে ৳১০.০০ যোগ করা হয়েছে।");
            }, 1000);
        }

        // টেস্টিং ফাংশনসমূহ (রেফার বাড়ানোর জন্য)
        function addFakeRefer() {
            totalRefers++;
            balance += 50; // প্রতি রেফারে ৫০ টাকা
            updateUI();
            alert("সফলভাবে ১টি রেফার এবং ৳৫০ বোনাস যুক্ত হয়েছে!");
        }

        function addMaxFake() {
            totalRefers = 20;
            totalVideoWatched = 200;
            todayTasks = 15;
            balance = 1550.00; // উইথড্র লিমিটের উপরে টাকা সেটআপ
            updateUI();
            a
