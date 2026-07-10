<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ALIF_INCOME_BD</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { background-color: #f0f2f5; font-family: sans-serif; }
        .app-card { background: white; border-radius: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        .nav-bar { background: #2d3436; color: white; position: fixed; bottom: 0; width: 100%; max-width: 420px; border-radius: 20px 20px 0 0; display: flex; justify-content: space-around; padding: 15px; }
    </style>
</head>
<body class="flex justify-center items-center min-h-screen">

<div class="w-full max-w-[420px] h-screen bg-[#f8fafc] overflow-hidden relative pb-20">
    <!-- Header -->
    <div class="bg-[#5c4ae0] p-6 rounded-b-[40px] text-white">
        <div class="flex justify-between items-center mb-4">
            <span class="text-xl font-bold">ALIF_INCOME_BD</span>
            <div class="bg-white/20 p-2 rounded-full">🎧</div>
        </div>
        <div class="bg-white/10 p-4 rounded-xl text-center">
            <p class="text-xs opacity-80">TOTAL BALANCE</p>
            <h2 class="text-3xl font-bold">৳<span id="balance">0.00</span></h2>
        </div>
    </div>

    <!-- Main Section -->
    <div class="p-4 space-y-4">
        <div class="grid grid-cols-2 gap-4">
            <div class="app-card p-4 text-center">
                <p class="text-[10px] text-gray-500">Earned</p>
                <p class="font-bold">৳<span id="earned">0.00</span></p>
            </div>
            <div class="app-card p-4 text-center">
                <p class="text-[10px] text-gray-500">Referrals</p>
                <p class="font-bold"><span id="ref-count">0</span></p>
            </div>
        </div>

        <!-- Ads -->
        <div class="app-card p-4">
            <p class="font-bold mb-2">Daily Ads</p>
            <button onclick="watchAd()" class="w-full bg-blue-500 text-white py-3 rounded-lg font-bold">ভিডিও দেখুন (১০টি)</button>
            <p class="text-xs mt-2 text-center">আজকের ভিডিও: <span id="ad-count">0</span>/10</p>
        </div>

        <!-- Withdraw -->
        <div class="app-card p-4 space-y-2">
            <p class="font-bold">Withdraw (Min ৳1500)</p>
            <select id="method" class="w-full p-2 border rounded">
                <option>বিকাশ</option>
                <option>নগদ</option>
            </select>
            <input id="number" type="text" placeholder="Number" class="w-full p-2 border rounded">
            <button onclick="withdraw()" class="w-full bg-slate-800 text-white py-2 rounded font-bold">Request Withdraw</button>
        </div>
    </div>

    <!-- Navigation -->
    <div class="nav-bar">
        <span>🏠</span>
        <span>🏆</span>
        <span>👤</span>
    </div>
</div>

<script>
    let balance = 0, earned = 0, refs = 0, ads = 0, totalVideos = 0;

    function watchAd() {
        if(ads < 10) {
            ads++; totalVideos++; balance += 10; earned += 10;
            updateUI(); alert("৳১০ যোগ হয়েছে!");
        } else { alert("আজকের লিমিট শেষ!"); }
    }

    function withdraw() {
        if(balance >= 1500 && (totalVideos >= 200 || refs >= 20)) {
            alert("উত্তোলন রিকোয়েস্ট সফল হয়েছে!");
        } else {
            alert("শর্ত পূরণ হয়নি! (ন্যূনতম ১৫০০ টাকা এবং ২০০ ভিডিও বা ২০ রেফার প্রয়োজন)");
        }
    }

    function updateUI() {
        document.getElementById('balance').innerText = balance.toFixed(2);
        document.getElementById('earned').innerText = earned.toFixed(2);
        document.getElementById('ref-count').innerText = refs;
        document.getElementById('ad-count').innerText = ads;
    }
</script>
</body>
</html>
