<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ELZ3EAM SHOP - شحن جواهر فري فاير</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #ff4655; /* لون فري فاير الأحمر الناري */
            --secondary: #ffb800; /* لون الذهب */
            --dark: #0f1722;
            --card-bg: rgba(255, 255, 255, 0.05);
        }

        body {
            background: radial-gradient(circle at center, #1a2a3a 0%, #0f1722 100%);
            color: white;
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            min-height: 100vh;
        }

        header {
            background: linear-gradient(90deg, var(--primary), #8b0000);
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.5);
            border-bottom: 3px solid var(--secondary);
        }

        header h1 {
            margin: 0;
            font-size: 2.5rem;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
        }

        .container {
            max-width: 800px;
            margin: 30px auto;
            padding: 20px;
        }

        .promo-text {
            text-align: center;
            color: var(--secondary);
            font-weight: bold;
            font-size: 1.2rem;
            margin-bottom: 30px;
            animation: blink 1.5s infinite;
        }

        @keyframes blink {
            0% { opacity: 1; }
            50% { opacity: 0.5; }
            100% { opacity: 1; }
        }

        .diamond-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-bottom: 40px;
        }

        .diamond-card {
            background: var(--card-bg);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: 0.3s;
            position: relative;
            overflow: hidden;
        }

        .diamond-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
            background: rgba(255, 70, 85, 0.1);
        }

        .diamond-card.selected {
            border: 2px solid var(--secondary);
            background: rgba(255, 184, 0, 0.15);
        }

        .diamond-card img {
            width: 50px;
            margin-bottom: 10px;
        }

        .diamond-card h3 {
            margin: 10px 0;
            font-size: 1.5rem;
        }

        .diamond-card p {
            color: var(--secondary);
            font-weight: bold;
        }

        .order-form {
            background: var(--card-bg);
            padding: 30px;
            border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .input-group {
            margin-bottom: 20px;
        }

        .input-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }

        .input-group input {
            width: 100%;
            padding: 12px;
            border-radius: 8px;
            border: 1px solid #333;
            background: #050a10;
            color: white;
            font-family: 'Cairo';
            box-sizing: border-box;
        }

        .btn-submit {
            width: 100%;
            padding: 15px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            border: none;
            border-radius: 10px;
            color: white;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
            text-transform: uppercase;
        }

        .btn-submit:hover {
            transform: scale(1.02);
            box-shadow: 0 0 20px rgba(255, 70, 85, 0.4);
        }

        footer {
            text-align: center;
            padding: 40px;
            font-size: 0.9rem;
            color: #666;
        }
    </style>
</head>
<body>

<header>
    <h1>ELZ3EAM SHOP</h1>
</header>

<div class="container">
    <div class="promo-text">🔥 أقوى عروض شحن جواهر فري فاير - تسليم فوري 🔥</div>

    <h2 style="text-align: center;">1. اختر كمية الجواهر</h2>
    <div class="diamond-grid">
        <div class="diamond-card" onclick="selectPack(this, '100 جوهرة')">
            <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/000000/external-diamond-poker-flat-icons-inmotus-design.png" alt="جواهر">
            <h3>100</h3>
            <p>جوهرة</p>
        </div>
        <div class="diamond-card" onclick="selectPack(this, '310 جوهرة')">
            <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/000000/external-diamond-poker-flat-icons-inmotus-design.png" alt="جواهر">
            <h3>310</h3>
            <p>جوهرة</p>
        </div>
        <div class="diamond-card" onclick="selectPack(this, '520 جوهرة')">
            <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/000000/external-diamond-poker-flat-icons-inmotus-design.png" alt="جواهر">
            <h3>520</h3>
            <p>جوهرة</p>
        </div>
        <div class="diamond-card" onclick="selectPack(this, '1060 جوهرة')">
            <img src="https://img.icons8.com/external-flat-icons-inmotus-design/64/000000/external-diamond-poker-flat-icons-inmotus-design.png" alt="جواهر">
            <h3>1060</h3>
            <p>جوهرة</p>
        </div>
    </div>

    <div class="order-form">
        <h2 style="text-align: center; margin-top: 0;">2. بيانات الحساب</h2>
        <div class="input-group">
            <label>اسمك في اللعبة</label>
            <input type="text" id="playerName" placeholder="اكتب اسمك هنا...">
        </div>
        <div class="input-group">
            <label>الـ ID الخاص بك</label>
            <input type="number" id="playerID" placeholder="اكتب الـ ID المكون من أرقام">
        </div>
        <div class="input-group">
            <label>رقم هاتف (واتساب)</label>
            <input type="tel" id="playerPhone" placeholder="01xxxxxxxxx">
        </div>
        <button class="btn-submit" onclick="sendOrder()">شحن الآن ✅</button>
    </div>
</div>

<footer>
    &copy; 2026 جميع الحقوق محفوظة لـ ELZ3EAM SHOP
</footer>

<script>
    let selectedAmount = "";

    function selectPack(element, amount) {
        // إزالة الاختيار من الكل
        document.querySelectorAll('.diamond-card').forEach(card => card.classList.remove('selected'));
        // إضافة الاختيار للكارت المضغطوط عليه
        element.classList.add('selected');
