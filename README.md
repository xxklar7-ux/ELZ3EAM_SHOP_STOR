<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الــزعــيـم STORE - VIP</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #ffb800; --red: #ff4655; --blue: #00d1ff; --dark: #050505; --card-bg: #121212; }
        body { background-color: var(--dark); color: white; font-family: 'Cairo', sans-serif; margin: 0; padding-bottom: 50px; }
        
        #welcome-screen { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(circle, #1a1a1a, #000); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 9999; }
        .logo-box { font-size: 3.5rem; font-weight: 900; color: var(--gold); text-shadow: 0 0 20px var(--gold); margin-bottom: 30px; text-align: center; }
        .enter-btn { padding: 15px 50px; background: transparent; border: 2px solid var(--gold); color: var(--gold); font-size: 1.5rem; font-weight: bold; cursor: pointer; border-radius: 50px; transition: 0.4s; }
        .enter-btn:hover { background: var(--gold); color: black; box-shadow: 0 0 30px var(--gold); }

        header { text-align: center; padding: 40px 20px; background: linear-gradient(to bottom, #111, transparent); }
        .section-title { border-right: 5px solid var(--gold); padding-right: 15px; margin: 30px 20px 10px; font-size: 1.4rem; color: var(--gold); text-shadow: 0 0 5px rgba(255,184,0,0.3); }
        
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 12px; padding: 20px; }
        .card { background: var(--card-bg); border-radius: 15px; padding: 15px; text-align: center; border: 1px solid #222; transition: 0.3s; cursor: pointer; position: relative; }
        .card:hover, .card.active { border-color: var(--gold); transform: translateY(-5px); background: #1a1a1a; box-shadow: 0 0 15px rgba(255,184,0,0.2); }
        .card img { width: 45px; margin-bottom: 10px; }
        .price { color: var(--gold); display: block; margin-top: 5px; font-weight: bold; }
        .badge { position: absolute; top: -5px; right: -5px; background: var(--red); font-size: 0.7rem; padding: 3px 8px; border-radius: 5px; font-weight: bold; }

        .order-box { background: #111; margin: 20px; padding: 25px; border-radius: 15px; border: 1px solid #333; box-shadow: 0 0 20px rgba(0,0,0,0.5); }
        input { width: 100%; padding: 15px; margin: 10px 0; background: #000; border: 1px solid #333; color: white; border-radius: 10px; box-sizing: border-box; font-family: 'Cairo'; outline: none; }
        input:focus { border-color: var(--gold); }
        .send-btn { width: 100%; padding: 18px; background: linear-gradient(45deg, var(--gold), #ffa000); border: none; border-radius: 10px; font-weight: 900; font-size: 1.3rem; cursor: pointer; margin-top: 15px; color: black; transition: 0.3s; }
        .send-btn:hover { transform: scale(1.02); box-shadow: 0 0 20px var(--gold); }
        
        footer { text-align: center; color: #555; padding: 20px; font-size: 0.8rem; border-top: 1px solid #111; }
    </style>
</head>
<body>

<div id="welcome-screen">
    <div class="logo-box">الــزعــيـم<br>STORE</div>
    <button class="enter-btn" onclick="document.getElementById('welcome-screen').style.display='none'">دخول المتجر</button>
</div>

<header>
    <h1 style="color: var(--gold); font-weight: 900; margin:0; font-size: 2.8rem;">الــزعــيـم STORE 👑</h1>
    <p style="color: #aaa;">متجرك الموثوق لشحن الألعاب وخدمات السوشيال</p>
</header>

<div class="section-title">🎮 شحن العملات (الألعاب)</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'فري فاير - 1060 جوهرة')">
        <div class="badge">الأكثر طلباً</div>
        <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/external-diamond-poker-flat-icons-inmotus-design.png">
        <span>1060 جوهرة</span>
        <span class="price">150 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'ببجي - 660 شدة')">
        <img src="https://img.icons8.com/color/64/pubg-mobile.png">
        <span>660 شدة</span>
        <span class="price">185 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'ببجي - 1800 شدة')">
        <img src="https://img.icons8.com/color/64/pubg-mobile.png">
        <span>1800 شدة</span>
        <span class="price">480 EGP</span>
    </div>
</div>

<div class="section-title">🚀 خدمات السوشيال ميديا</div>
<div class="grid">
    <div class="card" onclick="selectItem(this, 'تيك توك - 1000 متابع')">
        <img src="https://img.icons8.com/color/64/tiktok.png">
        <span>تيك توك (1K)</span>
        <span class="price">60 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'انستجرام - 1000 متابع')">
        <img src="https://img.icons8.com/color/64/instagram-new.png">
        <span>انستجرام (1K)</span>
        <span class="price">45 EGP</span>
    </div>
    <div class="card" onclick="selectItem(this, 'فيسبوك - 1000 متابع')">
        <img src="https://img.icons8.com/color/64/facebook-new.png">
        <span>فيسبوك (1K)</span>
        <span class="price">55 EGP</span>
    </div>
</div>

<div class="order-box">
    <h3 style="text-align:center; color:var(--gold); margin-top:0;">إتمام الطلب 📝</h3>
    <p id="selected-text" style="text-align:center; color:var(--blue); font-weight:bold;">يرجى اختيار عرض من الأعلى 👆</p>
    <input type="text" id="user-name" placeholder="اسمك الكامل">
    <input type="text" id="user-id" placeholder="الـ ID أو رابط الحساب">
    <input type="number" id="user-phone" placeholder="رقم واتسابك للتواصل">
    <button class="send-btn" onclick="sendToWhatsApp()">إرسال الطلب للزعيم ✅</button>
</div>

<footer>&copy; 2026 جميع الحقوق محفوظة لـ الــزعــيـم STORE</footer>

<script>
    let selectedPackage = "";

    function selectItem(element, name) {
        document.querySelectorAll('.card').forEach(c => c.classList.remove('active'));
        element.classList.add('active');
        selectedPackage = name;
        document.getElementById('selected-text').innerText = "تم اختيار: " + name;
        document.getElementById('selected-text').style.color = "#00ff00";
    }

    function sendToWhatsApp() {
        const name = document.getElementById('user-name').value;
        const id = document.getElementById('user-id').value;
        const phone = document.getElementById('user-phone').value;
        
        // غير الرقم ده لرقمك أنت (كود الدولة + رقم الواتساب)
        const myNumber = "201012345678"; 

        if(!selectedPackage) { alert("يا زعيم، اختار العرض اللي عاوزه الأول!"); return; }
        if(!name || !phone || !id) { alert("كمل بياناتك (الاسم، الـ ID، والرقم) عشان نشحنلك!"); return; }

        const message = `👑 طلب جديد من الزعيم ستور 👑%0A----------------------%0A🔥 الخدمة: ${selectedPackage}%0A👤 العميل: ${name}%0A🆔 الحساب/الـ ID: ${id}%0A📞 واتساب العميل: ${phone}%0A----------------------`;
        
        const waUrl = `https://wa.me/${myNumber}?text=${message}`;
        window.open(waUrl, '_blank');
    }
</script>

</body>
</html>
