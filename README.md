!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ভিডিও দেখে টাকা ইনকাম রেফার করে টাকা ইনকাম কমপক্ষে 20 টা রেফার করতে হবে তারপর উত্তোলন</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;500;600;700&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --emerald-900: #064e3b;
            --emerald-800: #065f46;
            --amber-500: #f59e0b;
        }
        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: #f8fafc;
            user-select: none;
        }
        .font-arabic {
            font-family: 'Amiri', serif;
        }
        .islamic-gradient {
            background: linear-gradient(135deg, #064e3b 0%, #065f46 50%, #047857 100%);
        }
        .glass {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        ::-webkit-scrollbar { display: none; }
        .tab-content { display: none; }
        .tab-content.active { display: block; animation: fadeIn 0.4s ease-out; }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .prayer-card.completed {
            background-color: #fbbf24 !important;
            color: #064e3b !important;
            border-color: #fbbf24 !important;
        }
    </style>
<script type="importmap">
{
  "imports": {
    "react": "https://esm.sh/react@^19.2.3",
    "react-dom/": "https://esm.sh/react-dom@^19.2.3/",
    "react/": "https://esm.sh/react@^19.2.3/",
    "@heroicons/react/": "https://esm.sh/@heroicons/react@^2.2.0/"
  }
}
</script>
</head>
<body class="max-w-md mx-auto bg-slate-50 min-h-screen shadow-2xl relative">

    <!-- Loading Screen -->
    <div id="loading-screen" class="fixed inset-0 z-[100] bg-white flex flex-col items-center justify-center">
        <div class="w-16 h-16 border-4 border-emerald-100 border-t-emerald-700 rounded-full animate-spin"></div>
        <p class="mt-4 font-bold text-emerald-900">আল-মুবিন লোড হচ্ছে...</p>
    </div>

    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white/80 backdrop-blur-md px-6 py-4 flex justify-between items-center border-b border-slate-100">
        <div class="flex items-center gap-3">
            <div class="w-10 h-10 bg-emerald-800 rounded-2xl flex items-center justify-center text-white font-bold shadow-lg shadow-emerald-900/20">M</div>
            <div>
                <h1 class="font-black text-emerald-950 leading-none">আল-মুবিন</h1>
                <span class="text-[9px] font-bold text-amber-600 tracking-widest uppercase">ইসলামিক হাব</span>
            </div>
        </div>
        <div id="current-location" class="text-[10px] bg-slate-100 px-3 py-1 rounded-full text-slate-500 font-bold">ঢাকা, বাংলাদেশ</div>
    </header>

    <!-- Global Quran Player Widget -->
    <div id="quran-player-bar" class="fixed bottom-24 left-4 right-4 bg-emerald-900 text-white p-3 rounded-2xl shadow-2xl z-40 hidden animate-in slide-in-from-bottom duration-300">
        <div class="flex items-center gap-3">
            <div id="player-disk" class="w-10 h-10 bg-amber-500 rounded-full flex items-center justify-center animate-spin-slow">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19V6l12-3v13M9 19c0 1.105-1.343 2-3 2s-3-.895-3-2 1.343-2 3-2 3 .895 3 2zm12-3c0 1.105-1.343 2-3 2s-3-.895-3-2 1.343-2 3-2 3 .895 3 2zM9 10l12-3"></path></svg>
            </div>
            <div class="flex-1 overflow-hidden">
                <p id="playing-surah-name" class="font-bold text-xs truncate">সূরা প্লে হচ্ছে</p>
                <div class="h-1 bg-white/20 rounded-full mt-1 w-full overflow-hidden">
                    <div id="player-progress" class="h-full bg-amber-400 w-0"></div>
                </div>
            </div>
            <button onclick="toggleAudio()" class="w-8 h-8 flex items-center justify-center bg-white/10 rounded-full">
                <span id="play-pause-icon">⏸</span>
            </button>
            <button onclick="closeAudio()" class="text-white/40">✕</button>
        </div>
    </div>

    <!-- Main Content -->
    <main class="p-5 pb-32">
        
        <!-- Tab: Home -->
        <section id="home" class="tab-content active space-y-6">
            <!-- Hero Hijri Card -->
            <div class="islamic-gradient rounded-[2.5rem] p-6 text-white shadow-xl relative overflow-hidden">
                <div class="relative z-10">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-amber-300 font-bold text-sm">আসসালামু আলাইকুম</p>
                            <h2 class="text-2xl font-black mt-1">পরবর্তী সালাত</h2>
                            <p id="next-prayer-info" class="text-amber-200 font-black text-lg mt-1 tracking-tight">লোড হচ্ছে...</p>
                        </div>
                        <div class="glass p-2 rounded-2xl text-center min-w-[80px]">
                            <span id="hijri-month" class="text-[10px] font-black block uppercase tracking-tighter">লোড হচ্ছে...</span>
                            <span id="hijri-day" class="text-lg font-black leading-none">--</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-2 gap-4 mt-8">
                        <div class="glass rounded-3xl p-4">
                            <p class="text-[10px] text-emerald-100 font-bold uppercase mb-1">সেহরি শেষ</p>
                            <p id="time-imsak" class="text-xl font-black text-amber-300">--:-- --</p>
                        </div>
                        <div class="glass rounded-3xl p-4">
                            <p class="text-[10px] text-emerald-100 font-bold uppercase mb-1">ইফতারের সময়</p>
                            <p id="time-maghrib" class="text-xl font-black text-amber-300">--:-- --</p>
                        </div>
                    </div>
                </div>
                <div class="absolute -bottom-10 -left-10 w-40 h-40 bg-white/5 rounded-full blur-3xl"></div>
            </div>

            <!-- Prayer Grid -->
            <div>
                <div class="flex justify-between items-center mb-4">
                    <h3 class="font-black text-emerald-900 text-lg">নামাজের সময়সূচী</h3>
                    <span id="hijri-year-bn" class="text-[10px] font-bold text-slate-400 bg-slate-100 px-2 py-0.5 rounded-full uppercase">---</span>
                </div>
                <div class="grid grid-cols-3 gap-3" id="prayer-times-grid"></div>
            </div>

            <!-- Premium Tracker -->
            <div class="bg-emerald-950 rounded-[2.5rem] p-6 text-white shadow-2xl relative overflow-hidden border border-emerald-800">
                <div class="flex justify-between items-end mb-4">
                    <div>
                        <h4 class="font-black text-amber-400">প্রিমিয়াম সালাত ট্র্যাকার</h4>
                        <p class="text-[10px] text-emerald-200 uppercase font-bold tracking-widest">ব্যক্তিগত ইবাদত ডায়েরি</p>
                    </div>
                    <span id="tracker-percent" class="text-3xl font-black text-white">0%</span>
                </div>
                <div class="h-3 bg-emerald-900 rounded-full overflow-hidden mb-6">
                    <div id="tracker-progress-bar" class="h-full bg-gradient-to-r from-amber-600 to-amber-300 transition-all duration-700 w-0"></div>
                </div>
                <div class="grid grid-cols-5 gap-2" id="tracker-buttons"></div>
            </div>
        </section>

        <!-- Tab: Quran -->
        <section id="quran" class="tab-content space-y-6">
            <div class="mb-4">
                <h2 class="text-2xl font-black text-emerald-950 leading-tight">আল-কুরআন</h2>
                <p class="text-xs text-slate-400 font-bold uppercase tracking-wider">তেলাওয়াত ও বঙ্গানুবাদ</p>
            </div>
            <div id="surah-list" class="space-y-3"></div>
        </section>

        <!-- Tab: Dua -->
        <section id="dua" class="tab-content space-y-6">
            <div class="mb-4">
                <h2 class="text-2xl font-black text-emerald-950 leading-tight">দোয়া ও জিকির</h2>
                <p class="text-xs text-slate-400 font-bold uppercase tracking-wider">মাসনুন দোয়া সমূহ</p>
            </div>
            <div id="dua-list" class="space-y-6"></div>
        </section>

        <!-- Tab: Names -->
        <section id="names" class="tab-content space-y-6">
            <div class="mb-4">
                <h2 class="text-2xl font-black text-emerald-950 leading-tight">আল্লাহর ৯৯ নাম</h2>
                <p class="text-xs text-slate-400 font-bold uppercase tracking-wider">অর্থ ও ফজিলত</p>
            </div>
            <div id="names-grid" class="grid grid-cols-2 gap-4"></div>
        </section>

    </main>

    <!-- Bottom Navigation -->
    <nav class="fixed bottom-0 left-0 right-0 max-w-md mx-auto bg-white/95 backdrop-blur-xl border-t border-slate-100 px-6 py-4 flex justify-between items-center z-50 rounded-t-[2.5rem] shadow-[0_-10px_40px_rgba(0,0,0,0.05)]">
        <button onclick="switchTab('home')" class="nav-btn active text-emerald-700 flex flex-col items-center gap-1" data-tab="home">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[9px] font-black uppercase">হোম</span>
        </button>
        <button onclick="switchTab('quran')" class="nav-btn text-slate-400 flex flex-col items-center gap-1" data-tab="quran">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"></path></svg>
            <span class="text-[9px] font-black uppercase">কুরআন</span>
        </button>
        <button onclick="switchTab('dua')" class="nav-btn text-slate-400 flex flex-col items-center gap-1" data-tab="dua">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px] font-black uppercase">দোয়া</span>
        </button>
        <button onclick="switchTab('names')" class="nav-btn text-slate-400 flex flex-col items-center gap-1" data-tab="names">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px] font-black uppercase">নামসমূহ</span>
        </button>
    </nav>

    <audio id="global-audio"></audio>

    <script>
        // --- DATA ---
        const HIJRI_MONTHS_BN = {
            "Muharram": "মুহাররম", "Safar": "সফর", "Rabi' al-awwal": "রবিউল আউয়াল",
            "Rabi' al-thani": "রবিউস সানি", "Jumada al-ula": "জমাদিউল আউয়াল",
            "Jumada al-akhira": "জমাদিউস সানি", "Rajab": "রজব", "Sha'ban": "শাবান",
            "Ramadan": "রমজান", "Shawwal": "শাওয়াল", "Dhu al-Qi'dah": "জিলকদ",
            "Dhu al-Hijjah": "জিলহজ্জ"
        };

        const DUAS = [
            {
                title: "আয়াতুল কুরসি",
                arabic: "اللَّهُ لَا إِلَهَ إِلَّا هُوَ الْحَيُّ الْقَيُّومُ ۚ لَا تَأْخُذُهُ سِنَةٌ وَلَا نَوْمٌ ۚ لَهُ مَا فِي السَّمَاوَاتِ وَمَا فِي الْأَرْضِ ۗ مَنْ ذَا الَّذِي يَشْفَعُ عِنْدَهُ إِلَّا بِإِذْنِهِ ۚ يَعْلَمُ مَا بَيْنَ أَيْدِيهِمْ وَمَا خَلْفَهُمْ ۖ وَلَا يُحِيطُونَ بِشَيْءٍ مِنْ عِلْمِهِ إِلَّا بِمَا شَاءَ ۚ وَسِعَ كُرْسِيُّهُ السَّمَاوَاتِ وَالْأَرْضَ ۖ وَلَا يَئُودُهُ حِفْظُهُمَا ۚ وَهُوَ الْعَلِيُّ الْعَظِيمُ",
                pronunciation: "আল্লাহু লা ইলাহা ইল্লা হুয়াল হাইয়ুল কাইয়ুম। লা তা’খুযুহু সিনাতুঁ ওয়ালা নাউম। লাহু মা ফিস সামাওয়াতি ওয়ামা ফিল আরদ। মান যাল্লাযি ইয়াশফাউ ইনদাহু ইল্লা বিইযনিহি। ইয়ালামু মা বাইনা আইদিহিম ওয়ামা খালফাহুম, ওয়ালা ইউহিতুনা বিশাইয়িম মিন ইলমিহি ইল্লা বিমা শা-আ। ওয়াসিয়া কুরসিইউহুস সামাওয়াতি ওয়াল আরদ, ওয়ালা ইয়াউদুহু হিফযুহুমা ওয়া হুয়াল আলিইউর আজিম।",
                meaning: "আল্লাহ, তিনি ছাড়া অন্য কোনো উপাস্য নেই, তিনি চিরঞ্জীব, সবকিছুর ধারক। তাঁকে তন্দ্রাও স্পর্শ করতে পারে না এবং নিদ্রাও নয়। আসমান ও যমীনে যা কিছু রয়েছে, সবই তাঁর।"
            },
            {
                title: "সাইয়্যিদুল ইস্তিগফার",
                arabic: "اللَّهُمَّ أَنْتَ رَبِّي لَا إِلَهَ إِلَّا أَنْتَ، خَلَقْتَنِي وَأَنَا عَبْدُكَ، وَأَنَا عَلَى عَهْدِكَ وَوَعْدِكَ مَا اسْتَطَعْتُ، أَعُوذُ بِكَ مِنْ شَرِّ مَا صَنَعْتُ، أَبُوءُ لَكَ بِنِعْمَتِكَ عَلَيَّ، وَأَبُوءُ لَكَ بِذَنْبِي فَاغْفِرْ لِي، فَإِنَّهُ لَا يَغْفِرُ الذُّنُوبَ إِلَّا أَنْتَ",
                pronunciation: "আল্লাহুম্মা আন্তা রাব্বি লা ইলাহা ইল্লা আন্তা। খালাকতানি ওয়া আনা আবদুকা ওয়া আনা আলা আহদিকা ওয়া ওয়াদিকা মাসতাতাতু। আউযুবিকা মিন শাররি মা সানাতু। আবুউ লাকা বিনিমাতিকা আলাইয়্যা ওয়া আবুউ লাকা বিযাম্বি ফাগফিরলি। ফায়িননাহু লা ইয়াগফিরুয যুনুবা ইল্লা আন্তা।",
                meaning: "হে আল্লাহ! আপনিই আমার প্রতিপ্রতিপালক। আপনি ছাড়া কোনো ইলাহ নেই। আপনিই আমাকে সৃষ্টি করেছেন এবং আমি আপনার গোলাম।"
            }
        ];

        const ALLAH_NAMES = [
            { ar: "الله", bn: "আল্লাহ", meaning: "একমাত্র উপাস্য" },
            { ar: "الرَّحْمَنُ", bn: "আর-রহমান", meaning: "পরম দয়ালু" },
            { ar: "الرَّحِيمُ", bn: "আর-রহিম", meaning: "অতি দয়ালু" },
            { ar: "الْمَلِكُ", bn: "আল-মালিক", meaning: "সর্বাধিপতি" },
            { ar: "الْقُدُّوسُ", bn: "আল-কুদুস", meaning: "অতি পবিত্র" },
            { ar: "السَّلَامُ", bn: "আস-সালাম", meaning: "শান্তিদাতা" },
            { ar: "الْمُؤْمِنُ", bn: "আল-মু'মিন", meaning: "নিরাপত্তাদাতা" },
            { ar: "الْمُهَيْمِنُ", bn: "আল-Muhaymin", meaning: "রক্ষণাবেক্ষণকারী" },
            { ar: "الْعَزِيزُ", bn: "আল-Aziz", meaning: "মহা পরাক্রমশালী" },
            { ar: "الْجَبَّارُ", bn: "আল-Jabbar", meaning: "দুর্নিবার" }
        ];

        let prayerProgress = JSON.parse(localStorage.getItem('al_mubin_progress')) || {
            fajr: false, dhuhr: false, asr: false, maghrib: false, isha: false
        };

        let cachedTimings = null;

        // --- INIT ---
        function init() {
            getLocation();
            renderDuas();
            renderNames();
            fetchQuran();
            updateTracker();
            setupAudioPlayer();
            setTimeout(() => document.getElementById('loading-screen').classList.add('hidden'), 800);
        }

        // --- LOCATION & PRAYER ---
        function getLocation() {
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(
                    pos => fetchPrayerTimes(pos.coords.latitude, pos.coords.longitude),
                    err => fetchPrayerTimes(23.8103, 90.4125)
                );
            } else fetchPrayerTimes(23.8103, 90.4125);
        }

        async function fetchPrayerTimes(lat, lng) {
            try {
                const date = new Date().toLocaleDateString('en-GB').split('/').reverse().join('-');
                const res = await fetch(`https://api.aladhan.com/v1/timings/${date}?latitude=${lat}&longitude=${lng}&method=2`);
                const data = await res.json();
                cachedTimings = data.data.timings;
                renderPrayerTimes(cachedTimings);
                renderHijri(data.data.date.hijri);
                startNextPrayerCountdown();
            } catch (e) { console.error("API Error", e); }
        }

        function convertTo12H(time) {
            if(!time) return "--:--";
            let [h, m] = time.split(':');
            let ampm = h >= 12 ? 'PM' : 'AM';
            h = h % 12 || 12;
            return `${h}:${m} ${ampm}`;
        }

        function renderPrayerTimes(times) {
            document.getElementById('time-imsak').innerText = convertTo12H(times.Imsak);
            document.getElementById('time-maghrib').innerText = convertTo12H(times.Maghrib);
            const grid = [
                {n: 'ফজর', t: times.Fajr, i: '🌅'}, {n: 'যোহর', t: times.Dhuhr, i: '☀️'}, {n: 'আসর', t: times.Asr, i: '🌤️'},
                {n: 'মাগরিব', t: times.Maghrib, i: '🌇'}, {n: 'এশা', t: times.Isha, i: '🌙'}, {n: 'সূর্যোদয়', t: times.Sunrise, i: '🔆'}
            ];
            document.getElementById('prayer-times-grid').innerHTML = grid.map(p => `
                <div class="bg-white p-4 rounded-3xl shadow-sm border border-slate-100 flex flex-col items-center">
                    <span class="text-xl mb-1">${p.i}</span>
                    <span class="text-[10px] font-bold text-slate-400 uppercase">${p.n}</span>
                    <span class="text-[13px] font-black text-emerald-900">${convertTo12H(p.t)}</span>
                </div>
            `).join('');
        }

        function renderHijri(hijri) {
            document.getElementById('hijri-month').innerText = HIJRI_MONTHS_BN[hijri.month.en] || hijri.month.en;
            document.getElementById('hijri-day').innerText = hijri.day;
            document.getElementById('hijri-year-bn').innerText = `${hijri.year} হিজরি`;
        }

        function startNextPrayerCountdown() {
            if (!cachedTimings) return;
            const updateNext = () => {
                const now = new Date();
                const prayers = [
                    {n: 'ফজর', t: cachedTimings.Fajr}, {n: 'যোহর', t: cachedTimings.Dhuhr}, {n: 'আসর', t: cachedTimings.Asr},
                    {n: 'মাগরিব', t: cachedTimings.Maghrib}, {n: 'এশা', t: cachedTimings.Isha}
                ];
                let next = null;
                for (let p of prayers) {
                    const [h, m] = p.t.split(':');
                    const pDate = new Date(); pDate.setHours(h, m, 0);
                    if (pDate > now) { next = { ...p, date: pDate }; break; }
                }
                if (!next) { 
                    const [h, m] = prayers[0].t.split(':');
                    const pDate = new Date(); pDate.setDate(pDate.getDate() + 1); pDate.setHours(h, m, 0);
                    next = { ...prayers[0], date: pDate };
                }
                const diff = next.date - now;
                const hh = Math.floor(diff / 3600000);
                const mm = Math.floor((diff % 3600000) / 60000);
                document.getElementById('next-prayer-info').innerText = `${next.n}: ${hh} ঘণ্টা ${mm} মি. বাকি`;
            };
            updateNext(); setInterval(updateNext, 60000);
        }

        // --- TRACKER ---
        function updateTracker() {
            const keys = ['fajr', 'dhuhr', 'asr', 'maghrib', 'isha'];
            const names = {fajr:'ফজর', dhuhr:'যোহর', asr:'আসর', maghrib:'মাগরিব', isha:'এশা'};
            const count = keys.filter(k => prayerProgress[k]).length;
            const pct = (count / 5) * 100;
            document.getElementById('tracker-percent').innerText = `${pct}%`;
            document.getElementById('tracker-progress-bar').style.width = `${pct}%`;
    
