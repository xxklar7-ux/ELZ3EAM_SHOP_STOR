<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إمبراطورية الــزعــيـم | متجر الخدمات الشامل</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #ffb800; --red: #ff4655; --blue: #00d1ff; --dark: #050505; --card-bg: #111111; }
        body { background-color: var(--dark); color: white; font-family: 'Cairo', sans-serif; margin: 0; padding-bottom: 50px; scroll-behavior: smooth; }
        
        /* واجهة الدخول */
        #welcome-screen { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(circle, #222, #000); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 9999; }
        .logo-box { font-size: 3.5rem; font-weight: 900; color: var(--gold); text-shadow: 0 0 30px var(--gold); margin-bottom: 20px; text-align: center; }
        .enter-btn { padding: 15px 70px; background: transparent; border: 3px solid var(--gold); color: var(--gold); font-size: 1.5rem; font-weight: bold; cursor: pointer; border-radius: 50px; transition: 0.5s; }
        .enter-btn:hover { background: var(--gold); color: black; box-shadow: 0 0 50px var(--gold); transform: scale(1.1); }

        header { text-align: center; padding: 50px 20px; background: linear-gradient(180deg, #181818 0%, transparent 100%); }
        .section-title { border-right: 6px solid var(--gold); padding-right: 15px; margin: 40px 20px 15px; font-size: 1.6rem; color: var(--gold); font-weight: 900; }
        
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 12px; padding: 0 15px; }
        .card { background: var(--card-bg); border-radius: 18px; padding: 15px; text-align: center; border: 1px solid #222; transition: 0.4s; cursor: pointer; position: relative; overflow: hidden; }
        .card:hover, .card.active { border-color: var(--gold); transform: translateY(-5px); background: #1a1a1a; box-shadow: 0 8px 20px rgba(0,0,0,0.6); }
        .card img { width: 45px; height: 45px; margin-bottom: 10px; }
        .price { color: var(--gold); display: block; margin-top: 8px; font-weight: 900; font-size: 1.1rem; }
        .badge { position: absolute; top: 10px; right: -25px; background: var(--red); font-size: 0.6rem; padding: 4px 25px; transform: rotate(45deg); font-weight: bold; }

        .order-box { background: #0a0a0a; margin: 30px 15px; padding: 25px; border-radius: 20px; border: 1px solid #333; box-shadow: 0 0 30px rgba(0,0,0,0.8); }
        input { width: 100%; padding: 15px; margin: 10px 0; background: #000; border: 1px solid #444; color: white; border-radius: 10px; box-sizing: border-box; font-family: 'Cairo'; outline: none; }
        input:focus { border-color: var(--gold); }
        .send-btn { width: 100%; padding: 18px; background: linear-gradient(45deg, var(--gold), #ff8c00); border: none; border-radius: 10px; font-weight: 900; font-size: 1.3rem; cursor: pointer; margin-top: 15px; color: black; transition: 0.4s; }
        .send-btn:hover { box-shadow: 0 0 20px var(--gold); transform: scale(1.02); }
        
        footer { text-align: center; color: #444; padding: 30px; font-size: 0.8rem; border-top: 1px solid #111; margin-top: 50px; }
    </style>
</head>
<body>

<div id="welcome-screen">
    <div class="logo-box">الــزعــيـم<br>STORE</div>
    <button class="enter-btn" onclick="document.getElementById('welcome-screen').style.display='none'">دخول الإمبراطورية 👑</button>
</div>

<header>
    <h1 style="color: var(--gold); font-weight: 900; margin:0; font-size: 2.8rem;">الــزعــيـم STORE 👑</h1>
    <p style="color: var(--blue); font-weight: bold;">متجر الخدمات المتكاملة - شحن وسوشيال</p>
</header>

<div class="section-title">🚀 خدمات السوشيال (فيس/تيك توك/انستا)</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'سوشيال - 100 متابع')">
        <img src="https://img.icons8.com/color/48/group.png">
        <span>100 متابع</span>
        <span class="price">20 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'سوشيال - 1000 متابع')">
        <img src="https://img.icons8.com/color/48/star.png">
        <span>1000 متابع</span>
        <span class="price">100 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'سوشيال - 10,000 متابع')">
        <img src="https://img.icons8.com/color/48/crown.png">
        <span>10,000 متابع</span>
        <span class="price">1000 EGP</span>
    </div>
</div>

<div class="section-title">💎 شحن فري فاير</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'FF - 110 جوهرة')"><span>110 جوهرة</span><span class="price">60 EGP</span></div>
    <div class="card" onclick="selectItem(this, 'FF - 230 جوهرة')"><span>230 جوهرة</span><span class="price">210 EGP</span></div>
    <div class="card" onclick="selectItem(this, 'FF - 310 جوهرة')"><span>310 جوهرة</span><span class="price">400 EGP</span></div>
    <div class="card" onclick="selectItem(this, 'FF - 1060 جوهرة')"><span>1060 جوهرة</span><span class="price">550 EGP</span></div>
</div>

<div class="section-title">🔫 شدات ببجي (UC)</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'PUBG - 60 شدة')"><span>60 شدة</span><span class="price">65 EGP</span></div>
    <div class="card" onclick="selectItem(this, 'PUBG - 325 شدة')"><span>325 شدة</span><span class="price">250 EGP</span></div>
    <div class="card" onclick="selectItem(this, 'PUBG - 660 شدة')"><span>660 شدة</span><span class="price">480 EGP</span></div>
    <div class="card" onclick="selectItem(this, 'PUBG - 1800 شدة')"><span>1800 شدة</span><span class="price">1250 EGP</span></div>
</div>

<div class="section-title">✨ عرض الإمبراطور الذهبي</div>
<div class="grid">
    <div class="card active" style="border-color: var(--gold); border-width: 2px;" onclick="selectItem(this, 'عرض الإمبراطور الملكي')">
        <div class="badge">الأقوى 👑</div>
        <img src="https://img.icons8.com/fluency/48/diamond--v1.png">
        <span>عرض الإمبراطور</span>
        <p style="font-size:0.7rem; color:#888;">5K متابع + 1000 جوهرة</p>
        <span class="price">1000 EGP</span>
    </div>
</div>

<div class="order-box">
    <h3 style="text-align:center; color:var(--gold); margin:0;">إتمام الطلب 📥</h3>
    <p id="selected-text" style="text-align:center; color:var(--blue); font-weight:bold;">اختر خدمتك من الأعلى 👆</p>
    <input type="text" id="user-name" placeholder="الاسم بالكامل">
    <input type="text" id="user-id" placeholder="الـ ID أو رابط الحساب">
    <input type="number" id="user-phone" placeholder="رقم واتسابك">
    <button class="send-btn" onclick="sendToWhatsApp()">شحن الآن عبر واتساب ✅</button>
</div>

<footer>&copy; 2026 إمبراطورية الزعيم - جميع الحقوق محفوظة لـ الــزعــيـم</footer>

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
        
        // ضع رقم واتسابك هنا (كود الدولة + الرقم)
        const myNumber = "201110552701"; 

        if(!selectedPackage) { alert("اختار الخدمة الأول يا زعيم!"); return; }
        if(!name || !phone || !id) { alert("كمل بياناتك عشان نشحنلك!"); return; }

        const message = `👑 طلب جديد من الزعيم ستور 👑%0A----------------------%0A🔥 الخدمة: ${selectedPackage}%0A👤 العميل: ${name}%0A🆔 الحساب/الـ ID: ${id}%0A📞 هاتف: ${phone}%0A----------------------`;
        
        window.open(`https://wa.me/${201110552701}?text=${message}`, '_blank');
    }
</script>

</body>
</html>
