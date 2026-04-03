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
        .price { color: var(--gold); display:
