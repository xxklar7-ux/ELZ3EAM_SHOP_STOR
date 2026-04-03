<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الــزعــيـم STORE - 4K</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #ffb800; --red: #ff4655; --blue: #00d1ff; --dark: #050505; --card-bg: #121212; }
        body { background-color: var(--dark); color: white; font-family: 'Cairo', sans-serif; margin: 0; padding-bottom: 50px; }
        
        /* واجهة الدخول */
        #welcome-screen { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(circle, #1a1a1a, #000); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 9999; }
        .logo-box { font-size: 3.5rem; font-weight: 900; color: var(--gold); text-shadow: 0 0 20px var(--gold); margin-bottom: 30px; text-align: center; }
        .enter-btn { padding: 15px 50px; background: transparent; border: 2px solid var(--gold); color: var(--gold); font-size: 1.5rem; font-weight: bold; cursor: pointer; border-radius: 50px; transition: 0.4s; }
        .enter-btn:hover { background: var(--gold); color: black; box-shadow: 0 0 30px var(--gold); }

        header { text-align: center; padding: 40px 20px; background: linear-gradient(to bottom, #111, transparent); }
        .section-title { border-right: 5px solid var(--gold); padding-right: 15px; margin: 30px 20px 10px; font-size: 1.4rem; color: var(--gold); }
        
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 12px; padding: 20px; }
        .card { background: var(--card-bg); border-radius: 15px; padding: 15px; text-align: center; border: 1px solid #222; transition: 0.3s; cursor: pointer; position: relative; }
        .card:hover, .card.active { border-color: var(--gold); transform: translateY(-5px); background: #1a1a1a; }
        .card img { width: 50px; margin-bottom: 10px; }
        .price { color: var(--gold); display: block; margin-top: 5px; font-weight: bold; }
        .badge { position: absolute; top: -5px; right: -5px; background: var(--red); font-size: 0.7rem; padding: 3px 8px; border-radius: 5px; font-weight: bold; }

        .order-box { background: #111; margin: 20px; padding: 25px; border-radius: 15px; border: 1px solid #333; }
        input { width: 100%; padding: 15px; margin: 10px 0; background: #000; border: 1px solid #333; color: white; border-radius: 10px; box-sizing: border-box; font-family: 'Cairo'; }
        .send-btn { width: 100%; padding: 18px; background: linear-gradient(45deg, var(--gold), #ffa000); border: none; border-radius: 10px; font-weight: 900; font-size: 1.3rem; cursor: pointer; margin-top: 15px; }
        
        footer { text-align: center; color: #555; padding: 20px; font-size: 0.8rem; }
    </style>
</head>
<body>

<div id="welcome-screen">
    <div class="logo-box">الــزعــيـم<br>STORE</div>
    <button class="enter-btn" onclick="document.getElementById('welcome-screen').style.display='none'">دخول المتجر</button>
</div>

<header>
    <h1 style="color: var(--gold); font-weight: 900; margin:0;">الــزعــيـم STORE 👑</h1>
    <p>الأقوى في عالم الشحن والخدمات</p>
</header>

<div class="section-title">💎 شحن فري فاير</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'فري فاير - 1060 جوهرة')">
        <div class="badge">عرض</div>
        <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/external-diamond-poker-flat-icons-inmotus-design.png">
        <span>1060 جوهرة</span>
        <span class="price">150 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'فري فاير - 2310 جوهرة')">
        <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/external-diamond-poker-flat-icons-inmotus-design.png">
        <span>2310 جوهرة</span>
        <span class="price">300 EGP</span>
    </div>
</div>

<div class="section-title">🔫 شحن ببجي</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'ببجي - 660 شدة')">
        <img src="https://img.icons8.com/color/64/pubg-mobile.png">
        <span>660 شدة</span>
        <span class="price">180 EGP</span>
    </div>
</div>

<div class="section-title">✨ خدمات السوشيال ميديا</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, '1000 متابع تيك توك')">
        <img src="https://img.icons8.com/color/64/tiktok.png">
        <span>1000 متابع</span>
        <span class="price">50 EGP</span>
    </div>
</div>

<div class="section-title">🌸 قسم العطور</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'عطر الزعيم الملكي')">
        <img src="https://img.icons8.com/fluency/64/perfume-bottle.png">
        <span>عطر ملكي</span>
        <span class="price">450 EGP</span>
    </div>
</div>

<div class="order-box">
    <h3 style="text-align:center; color:var(--gold);">اتمام الطلب 📝</h3>
    <p id="selected-text" style="text-align:center; color:var(--blue);">لم يتم اختيار عرض بعد</p>
    <input type="text" id="user-name" placeholder="الاسم / اسم الحساب">
    <input type="text" id="user-id" placeholder="الـ ID (للألعاب)">
    <input type="number" id="user-phone" placeholder="رقم الواتساب الخاص بك">
    <button class="send-btn" onclick="sendToWhatsApp()">إرسال الطلب للزعيم ✅</button>
</div>

<footer>&copy; 2026 تصميم وبرمجة الــزعــيـم</footer>

<script>
    let selectedPackage = "";

    function selectItem(element, name) {
        document.querySelectorAll('.card').forEach(c => c.classList.remove('active'));
        element.classList.add('active');
        selectedPackage = name;
        document.getElementById('selected-text').innerText = "تم اختيار: " + name;
    }

    function sendToWhatsApp() {
        const name = document.getElementById('user-name').value;
        const id = document.getElementById('user-id').value;
        const phone = document.getElementById('user-phone').value;
        
        // ضع رقمك هنا (كود الدولة + الرقم)
        const myNumber = "201012345678"; 

        if(!selectedPackage) { alert("اختار العرض الأول يا زعيم!"); return; }
        if(!name || !phone) { alert("اكتب اسمك ورقمك عشان نتواصل معاك!"); return; }

        const message = `👑 طلب جديد من متجر الزعيم 👑%0A----------------------%0A🔥 الخدمة: ${selectedPackage}%0A👤 الاسم: ${name}%0A🆔 الـ ID: ${id}%0A📞 هاتف العميل: ${phone}%0A----------------------`;
        
        window.open(`https://wa.me/${myNumber}?text=${message}`, '_blank');
    }
</script>

</body>
</html>
