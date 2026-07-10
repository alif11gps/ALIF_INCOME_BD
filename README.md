<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <title>ALIF_INCOME_BD - অফিসিয়াল আর্নিং প্ল্যাটফর্ম</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* লোডিং স্ক্রিন স্টাইল */
        #splash-screen {
            position: fixed;
            inset: 0;
            background-color: #0f172a;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 0.5s ease;
        }
        .logo-text { color: white; font-size: 24px; font-weight: 900; letter-spacing: 2px; }
        
        body { font-family: 'Hind Siliguri', sans-serif; background-color: #0f172a; color: #1e293b; user-select: none; -webkit-tap-highlight-color: transparent; display: flex; justify-content: center; align-items: center; min-height: 100vh; margin: 0; }
        .app-container { width: 100%; max-width: 420px; height: 100vh; max-height: 850px; background-color: #f8fafc; display: flex; flex-direction: column; position: relative; overflow: hidden; box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5); }
        @media (min-width: 450px) { .app-container { border-radius: 30px; border: 8px solid #334155; height: 90vh; } }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body>

    <div id="splash-screen">
        <div class="w-16 h-16 bg-indigo-600 rounded-2xl flex items-center justify-center text-white text-xl font-bold mb-4 animate-bounce">ALIF</div>
        <div class="logo-text">ALIF_INCOME_BD</div>
    </div>

    <div class="app-container">
        <header class="bg-white border-b border-slate-200 px-4 py-3 flex items-center justify-between sticky top-0 z-50 shadow-sm shrink-0">
            <div class="flex items-center gap-2">
                <div class="w-7 h-7 bg-indigo-600 rounded-lg flex items-center justify-center text-white text-sm font-bold">💼</div>
                <span class="text-base font-black text-slate-800 tracking-wider">ALIF_INCOME_BD</span>
            </div>
            <div class="bg-indigo-50 px-3 py-1 rounded-full border border-indigo-100 flex items-center gap-1.5">
                <span class="text-indigo-600 text-xs font-bold">৳</span>
                <span id="nav-balance" class="font-bold text-indigo-700 text-sm">0.00</span>
            </div>
        </header>

        </div>

    <script>
        // লোডিং লোগো হাইড করা
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('splash-screen').style.opacity = '0';
                setTimeout(() => {
                    document.getElementById('splash-screen').style.display = 'none';
                }, 500);
            }, 2000); // ২ সেকেন্ড লোগো দেখাবে
        });

        // আপনার আগের জাভাস্ক্রিপ্ট লজিক এখানে বসান...
    </script>
</body>
</html>
