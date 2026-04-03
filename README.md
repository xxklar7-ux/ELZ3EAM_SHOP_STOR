<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الزعيم مشع - ELZ3EAM SHOP</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --gold: #ffb800;
            --neon-blue: #00d4ff;
            --neon-red: #ff4655;
            --dark-bg: #050505;
        }

        body {
            background-color: var(--dark-bg);
            color: white;
            font-family: 'Cairo', sans-serif;
            margin: 0;
            overflow-x: hidden;
        }

        /* صفحة الدخول */
        #login-screen {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: black;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .glow-text {
            font-size: 3rem;
            font-weight: 900;
            color: white;
            text-shadow: 0 0 20px var(--gold), 0 0 40px var(--gold);
            margin-bottom: 30px;
            text-align: center;
        }

        .enter-btn {
            padding: 15px 50px;
            font-size: 1.5rem;
            background: transparent;
            color: var(--gold);
            border: 2px solid var(--gold);
            cursor: pointer;
            border-radius: 50px;
            transition: 0.5s;
        }

        .enter-btn:hover {
            background: var(--gold);
            color: black;
            box-shadow: 0 0 30px var(--gold);
        }

        /* الواجهة الرئيسية */
        #main-site { display: none; padding-top: 80px; }

        header {
            position: fixed;
            top: 0; width: 100%;
            background: rgba(0,0,0,0.9);
            padding: 15px;
            text-align: center;
            border-bottom: 2px solid var(--gold);
            z-index: 999;
        }

        .section-title {
            text-align: center;
            margin: 40px 0;
            font-size: 2rem;
            color: var(--gold);
            text-decoration: underline;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .item-card {
            background: #111;
            border: 1px solid #333;
            border-radius: 15px;
            padding: 15px;
            text-align: center;
            transition: 0.3s;
        }

        .item-card:hover {
            border-color: var(--gold);
            transform: scale(1.05);
        }

        .item-card img { width: 60px; margin-bottom: 10px; }

        .price-tag { color: var(--gold); font-weight: bold; display: block; margin: 10px 0; }

        .buy-btn {
            background: var(--neon-red);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
        }

        .pubg-btn { background: var(--neon-blue); }
        .social-btn { background: #555; }

        /* نموذج التواصل */
        .contact-box {
            background: #111;
            margin: 40px 20px;
            padding: 30px;
            border-radius: 20px;
            border: 1px solid var(--gold);
        }

        input, select {
            width: 100%; padding: 12px; margin: 10px 0;
            background: #222; border: 1px solid #444;
            color: white; border-radius: 8px; box-sizing: border-box;
        }

        .final-btn {
            background: var(--gold);
            color: black;
            font-weight: bold;
            font-size: 1.3rem;
            border: none;
            width: 100%;
            padding: 15px;
            border-radius: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div id="login-screen">
    <div class="glow-text">الزعيم مشع 👑</div>
    <p>مرحباً بك في أقوى متجر خدمات ألعاب وسوشيال ميديا</p>
    <button class="enter-btn" onclick="enterSite()">دخول المتجر</button>
</div>

<div id="main-site">
    <header>
        <h2 style="margin:0; color: var(--gold);">الزعيم مشع SHOP</h2>
    </header>

    <h2 class="section-title">🔥 عروض جواهر فري فاير</h2>
    <div class="grid-container">
        <div class="item-card" onclick="setOrder('100 جوهرة فري فاير')">
            <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/external-diamond-poker-flat-icons-inmotus-design.png">
            <h3>100 جوهرة</h3>
            <span class="price-tag">عرض خاص</span>
            <button class="buy-btn">اختار</button>
        </div>
        <div class="item-card" onclick="setOrder('520 جوهرة فري فاير')">
            <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/external-diamond-poker-flat-icons-inmotus-design.png">
            <h3>520 جوهرة</h3>
            <span class="price-tag">الأكثر مبيعاً</span>
            <button class="buy-btn">اختار</button>
        </div>
    </div>

    <h2 class="section-title">🔫 عروض شدات ببجي (UC)</h2>
    <div class="grid-container">
        <div class="item-card" onclick="setOrder('60 شدة ببجي')">
            <img src="https://img.icons8.com/color/64/battlegrounds-mobile-india.png">
            <h3>60 UC</h3>
            <span class="price-tag">شحن فوري</span>
            <button class="buy-btn pubg-btn">اختار</button>
        </div>
        <div class="item-card" onclick="setOrder('325 شدة ببجي')">
            <img src="https://img.icons8.com/color/64/battlegrounds-mobile-india.png">
            <h3>325 UC</h3>
            <span class="price-tag">عرض الزعيم</span>
            <button class="buy-btn pubg-btn">اختار</button>
        </div>
    </div>

    <h2 class="section-title">🚀 زيادة متابعين سوشيال ميديا</h2>
    <div class="grid-container">
        <div class="item-card" onclick="setOrder('1000 متابع تيك توك')">
            <img src="https://img.icons8.com/color/64/tiktok.png">
            <h3>1000 متابع</h3>
            <span class="price-tag">تيك توك</span>
            <button class="buy-btn social-btn">اختار</button>
        </div>
        <div class="item-card" onclick="setOrder('1000 متابع انستقرام')">
            <img src="https://img.icons8.com/color/64/instagram-new--v1.png">
            <h3>1000 متابع</h3>
            <span class="price-tag">انستقرام</span>
            <button class="buy-btn social-btn">اختار</button>
        </div>
    </div>

    <div class="contact-box" id="order-section">
        <h2 style="color:var(--gold); text-align:center;">إتمام الطلب 📝</h2>
        <input type="text" id="selected-service" readonly placeholder="اختار خدمة من الأعلى">
        <input type="text" id="user-id" placeholder="الـ ID أو رابط الحساب">
        <input type="text" id="user-name" placeholder="اسمك">
        <input type="
