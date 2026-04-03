<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إمبراطورية الــزعــيـم - ELZ3EAM STORE</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #ffb800; --red: #ff4655; --blue: #00d1ff; --dark: #050505; --card-bg: #111111; }
        body { background-color: var(--dark); color: white; font-family: 'Cairo', sans-serif; margin: 0; padding-bottom: 50px; scroll-behavior: smooth; }
        
        /* شاشة الدخول */
        #welcome-screen { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(circle, #222, #000); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 9999; text-align: center; }
        .logo-box { font-size: 4rem; font-weight: 900; color: var(--gold); text-shadow: 0 0 30px var(--gold); margin-bottom: 20px; animation: glow 2s infinite alternate; }
        @keyframes glow { from { text-shadow: 0 0 10px var(--gold); } to { text-shadow: 0 0 40px var(--gold), 0 0 60px var(--gold); } }
        .enter-btn { padding: 15px 70px; background: transparent; border: 3px solid var(--gold); color: var(--gold); font-size: 1.6rem; font-weight: bold; cursor: pointer; border-radius: 50px; transition: 0.5s; box-shadow: 0 0 20px rgba(255,184,0,0.3); }
        .enter-btn:hover { background: var(--gold); color: black; box-shadow: 0 0 50px var(--gold); transform: scale(1.1); }

        header { text-align: center; padding: 60px 20px; background: linear-gradient(180deg, #181818 0%, transparent 100%); border-bottom: 1px solid #222; }
        .main-title { font-size: 3.5rem; color: var(--gold); margin: 0; font-weight: 900; }
        
        .section-title { border-right: 6px solid var(--gold); padding-right: 15px; margin: 50px 20px 20px; font-size: 1.8rem; color: var(--gold); text-transform: uppercase; letter-spacing: 1px; }
        
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 20px; padding: 0 20px; }
        .card { background: var(--card-bg); border-radius: 25px; padding: 25px; text-align: center; border: 1px solid #333; transition: 0.4s; cursor: pointer; position: relative; overflow: hidden; }
        .card:hover, .card.active { border-color: var(--gold); transform: translateY(-10px); background: #1a1a1a; box-shadow: 0 15px 30px rgba(0,0,0,0.7); }
        .card img { width: 60px; height: 60px; margin-bottom: 15px; filter: drop-shadow(0 0 5px rgba(255,255,255,0.2)); }
        .card span { display: block; font-weight: bold; font-size: 1.1rem; }
        .price { color: var(--gold); display: block; margin-top: 10px; font-weight: 900; font-size: 1.3rem; }
        .badge { position: absolute; top: 15px; right: -30px; background: var(--red); font-size: 0.8rem; padding: 5px 35px; transform: rotate(45deg); font-weight: bold; box-shadow: 0 2px 10px rgba(0,0,0,0.5); }

        /* قسم العروض الخاصة */
        .special-offer { background: linear-gradient(145deg, #1a1a1a, #000); border: 2px solid var(--gold) !important; box-shadow: 0 0 20px rgba(255,184,0,0.15); }

        .order-box { background: #0a0a0a; margin: 40px 20px; padding: 40px; border-radius: 30px; border: 1px solid #333; box-shadow: 0 0 40px rgba(0,0,0,0.9); }
        input { width: 100%; padding: 18px; margin: 15px 0; background: #000; border: 1px solid #444; color: white; border-radius: 15px; box-sizing: border-box; font-family: 'Cairo'; outline: none; font-size: 1.1rem; transition: 0.3s; }
        input:focus { border-color: var(--gold); box-shadow: 0 0 15px rgba(255,184,0,0.2); }
        .send-btn { width: 100%; padding: 22px; background: linear-gradient(45deg, var(--gold), #ff8c00); border: none; border-radius: 15px; font-weight: 900; font-size: 1.6rem; cursor: pointer; margin-top: 25px; color: black; transition: 0.4s; }
        .send-btn:hover { transform: scale(1.05); box-shadow: 0 10px 30px var(--gold); }
        
        footer { text-align: center; color: #666; padding: 40px; font-size: 1rem; border-top: 1px solid #222; margin-top: 50px; }
    </style>
</head>
<body>

<div id="welcome-screen">
    <div class="logo-box">الــزعــيـم<br>STORE</div>
    <p style="color:#aaa; font-size:1.2rem; margin-bottom:30px;">أقوى متجر خدمات في الوطن العربي</p>
    <button class="enter-btn" onclick="document.getElementById('welcome-screen').style.display='none'">دخول الإمبراطورية 👑</button>
</div>

<header>
    <h1 class="main-title">الــزعــيـم STORE 👑</h1>
    <p style="color: var(--blue); font-size:1.2rem; font-weight:bold;">سرعة • أمان • تميز</p>
</header>

<div class="section-title">🔵 خدمات فيسبوك (متابعين)</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'فيسبوك - 100 متابع')">
        <img src="https://img.icons8.com/color/96/facebook-new.png">
        <span>100 متابع</span>
        <span class="price">20 EGP</span>
    </div>
    <div class="card special-offer" onclick="selectItem(this, 'فيسبوك - 1000 متابع')">
        <div class="badge">توفير</div>
        <img src="https://img.icons8.com/color/96/facebook-new.png">
        <span>1000 متابع</span>
        <span class="price">100 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'فيسبوك - 10,000 متابع')">
        <img src="https://img.icons8.com/color/96/facebook-new.png">
        <span>10,000 متابع</span>
        <span class="price">1000 EGP</span>
    </div>
</div>

<div class="section-title">⚫ خدمات تيك توك</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'تيك توك - 100 متابع')">
        <img src="https://img.icons8.com/color/96/tiktok--v1.png">
        <span>100 متابع</span>
        <span class="price">20 EGP</span>
    </div>
    <div class="card special-offer" onclick="selectItem(this, 'تيك توك - 1000 متابع')">
        <div class="badge">VIP</div>
        <img src="https://img.icons8.com/color/96/tiktok--v1.png">
        <span>1000 متابع</span>
        <span class="price">100 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'تيك توك - 10,000 متابع')">
        <img src="https://img.icons8.com/color/96/tiktok--v1.png">
        <span>10,000 متابع</span>
        <span class="price">1000 EGP</span>
    </div>
</div>

<div class="section-title">📸 خدمات انستجرام</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'انستا - 100 متابع')">
        <img src="https://img.icons8.com/color/96/instagram-new--v1.png">
        <span>100 متابع</span>
        <span class="price">20 EGP</span>
    </div>
    <div class="card special-offer" onclick="selectItem(this, 'انستا - 1000 متابع')">
        <img src="https://img.icons8.com/color/96/instagram-new--v1.png">
        <span>1000 متابع</span>
        <span class="price">100 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'انستا - 10,000 متابع')">
        <img src="https://img.icons8.com/color/96/instagram-new--v1.png">
        <span>10,000 متابع</span>
        <span class="price">1000 EGP</span>
    </div>
</div>

<div class="section-title">🎮 شحن ألعاب (فري فاير وببجي)</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'فري فاير - 1060 جوهرة')">
        <div class="badge">🔥</div>
        <img src="https://img.icons8.com/external-flat-icons-inmotus-design/96/external-diamond-poker-flat-icons-inmotus-design.png">
        <span>1060 جوهرة</span>
        <span class="price">150 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'ببجي - 660 شدة')">
        <img src="https://img.icons8.com/color/96/pubg-mobile.png">
        <span>660 شدة</span>
        <span class="price">185 EGP</span>
    </div>
</div>

<div class="section-title">💎 عروض الزعيم الميكس (هدايا)</div>
<div class="grid">
    <div class="card special-offer" onclick="selectItem(this, 'عرض الإمبراطور: 5000 متابع ميكس + 1000 جوهرة')">
        <div class="badge">هدية 🎁</div>
        <img src="https://img.icons8.com/fluency/96/crown.png">
        <span>عرض الإمبراطور</span>
        <p style="font-size:0.8rem; color:#888;">5K متابع ميكس + 1K جوهرة</p>
        <span class="price">600 EGP</span>
    </div>
</div>

<div class="order-box">
    <h3 style="text-align:center; color:var(--gold); margin-top:0; font-size:2rem;">إتمام عملية الطلب 📥</h3>
    <p id="selected-text" style="text-align:center; color:var(--blue); font-weight:bold; font-size:1.3rem; margin-bottom:30px;">اختر الخدمة من الأعلى للبدء 👆</p>
    
    <input type="text" id="user-name" placeholder="اسمك الكامل">
    <input type="text" id="user-id" placeholder="الـ ID أو رابط الحساب المراد تزويده">
    <input type="number" id="user-phone" placeholder="رقم واتسابك (للتواصل)">
    
    <button class="send-btn" onclick="sendToWhatsApp()">إرسال الطلب للزعيم ✅</button>
</div>

<footer>&copy; 2026 إمبراطورية الزعيم | تصميم وتطوير الــزعــيـم</footer>

<script>
    let selectedPackage = "";

    function selectItem(element, name) {
        document.querySelectorAll('.card').forEach(c => c.classList.remove('active'));
        element.classList.add('active');
        selectedPackage = name;
        document.getElementById('selected-text').innerText = "✅ المطلوب: " + name;
        document.getElementById('selected-text').style.color = "#00ff00";
    }

    function sendToWhatsApp() {
        const name = document.getElementById('user-name').value;
        const id = document.getElementById('user-id').value;
        const phone = document.getElementById('user-phone').value;
        
        // ضع رقمك هنا (كود الدولة + الرقم)
        const myNumber = "201110552701"; 

        if(!selectedPackage) { alert("اختار الخدمة الأول يا زعيم!"); return; }
        if(!name || !phone || !id) { alert("البيانات ناقصة! الاسم والـ ID والرقم ضروريين."); return; }

        const message = `👑 طلب جديد من إمبراطورية الزعيم 👑%0A----------------------%0A💎 الخدمة: ${selectedPackage}%0A👤 العميل: ${name}%0A🆔 الحساب: ${id}%0A📞 هاتف: ${phone}%0A----------------------%0Aتم الطلب من الموقع الرسمي ⚡`;
        
        window.open(`https://wa.me/${myNumber}?text=${message}`, '_blank');
    }
</script>

</body>
</html>
