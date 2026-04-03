<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ELZ3EAM SHOP - شحن جواهر</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@700;900&display=swap" rel="stylesheet">
    <style>
        body { background: #0f1722; color: white; font-family: 'Cairo', sans-serif; text-align: center; margin: 0; padding: 20px; }
        .header { background: linear-gradient(45deg, #ff4655, #ffb800); padding: 20px; border-radius: 15px; margin-bottom: 20px; box-shadow: 0 5px 15px rgba(0,0,0,0.3); }
        .card { background: rgba(255,255,255,0.05); padding: 15px; border-radius: 10px; border: 1px solid #333; margin: 10px auto; max-width: 400px; }
        .diamond-btn { background: #1a2a3a; border: 1px solid #ff4655; color: white; padding: 15px; margin: 5px; border-radius: 8px; cursor: pointer; width: 45%; transition: 0.3s; }
        .selected { background: #ff4655; border-color: #fff; transform: scale(1.05); }
        input { width: 90%; padding: 12px; margin: 10px 0; border-radius: 5px; border: none; background: #050a10; color: white; text-align: center; }
        .btn-send { width: 90%; padding: 15px; background: #ffb800; color: #000; border: none; border-radius: 5px; font-weight: bold; cursor: pointer; font-size: 1.2rem; }
    </style>
</head>
<body>

<div class="header">
    <h1>ELZ3EAM SHOP 👑</h1>
</div>

<h3>1. اختر الكمية 🔥</h3>
<div style="max-width: 500px; margin: auto;">
    <button class="diamond-btn" onclick="select(this, '100 جوهرة')">100 جوهرة</button>
    <button class="diamond-btn" onclick="select(this, '310 جوهرة')">310 جوهرة</button>
    <button class="diamond-btn" onclick="select(this, '520 جوهرة')">520 جوهرة</button>
    <button class="diamond-btn" onclick="select(this, '1060 جوهرة')">1060 جوهرة</button>
</div>

<div class="card">
    <h3>2. بياناتك 📝</h3>
    <input type="text" id="name" placeholder="اسمك في اللعبة">
    <input type="number" id="id" placeholder="ID اللاعب">
    <input type="number" id="phone" placeholder="رقم واتسابك">
    <button class="btn-send" onclick="send()">شحن الآن ✅</button>
</div>

<script>
    let amount = "";
    function select(btn, val) {
        document.querySelectorAll('.diamond-btn').forEach(b => b.classList.remove('selected'));
        btn.classList.add('selected');
        amount = val;
    }

    function send() {
        const n = document.getElementById('name').value;
        const i = document.getElementById('id').value;
        const p = document.getElementById('phone').value;
        
        // غير الرقم ده لرقمك الحقيقي عشان الطلبات تجيلك أنت
        const myNum = "201012345678"; 

        if(!amount || !n || !i || !p) {
            alert("يا زعيم، اختار الجواهر واكتب بياناتك الأول!");
            return;
        }

        const msg = `طلب شحن من الزعيم 👑%0Aالكمية: ${amount}%0Aالاسم: ${n}%0Aالـ ID: ${i}%0Aرقم العميل: ${p}`;
        window.open(`https://wa.me/${myNum}?text=${msg}`, '_blank');
    }
</script>

</body>
</html>
