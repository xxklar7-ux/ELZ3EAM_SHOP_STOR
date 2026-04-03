<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الــزعــيـم STORE | VIP SERVICES</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #ffb800; --red: #ff4655; --blue: #00d1ff; --dark: #050505; --card-bg: #111111; }
        body { background-color: var(--dark); color: white; font-family: 'Cairo', sans-serif; margin: 0; padding-bottom: 50px; }
        
        /* واجهة الدخول الفخمة */
        #welcome-screen { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(circle, #222, #000); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 9999; }
        .logo-box { font-size: 3.5rem; font-weight: 900; color: var(--gold); text-shadow: 0 0 20px var(--gold); margin-bottom: 30px; text-align: center; line-height: 1; }
        .enter-btn { padding: 15px 60px; background: transparent; border: 2px solid var(--gold); color: var(--gold); font-size: 1.5rem; font-weight: bold; cursor: pointer; border-radius: 50px; transition: 0.4s; box-shadow: 0 0 15px rgba(255,184,0,0.2); }
        .enter-btn:hover { background: var(--gold); color: black; box-shadow: 0 0 40px var(--gold); }

        header { text-align: center; padding: 50px 20px; background: linear-gradient(to bottom, #151515, transparent); border-bottom: 1px solid #222; }
        .section-title { border-right: 5px solid var(--gold); padding-right: 15px; margin: 40px 20px 15px; font-size: 1.6rem; color: var(--gold); font-weight: 900; }
        
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 15px; padding: 0 20px; }
        .card { background: var(--card-bg); border-radius: 20px; padding: 20px; text-align: center; border: 1px solid #222; transition: 0.3s; cursor: pointer; position: relative; overflow: hidden; }
        .card:hover, .card.active { border-color: var(--gold); transform: translateY(-8px); background: #1a1a1a; box-shadow: 0 10px 20px rgba(0,0,0,0.5); }
        .card img { width: 50px; height: 50px; margin-bottom: 15px; }
        .price { color: var(--gold); display: block; margin-top: 10px; font-weight: 900; font-size: 1.1rem; }
        .badge { position: absolute; top: 10px; left: -25px; background: var(--red); font-size: 0.7rem; padding: 5px 30px; transform: rotate(-45deg); font-weight: bold; }

        /* عروض التوفير */
        .offer-card { background: linear-gradient(145deg, #1a1a1a, #000); border: 2px solid var(--gold) !important; }

        .order-box { background: #0a0a0a; margin: 30px 20px; padding: 30px; border-radius: 20px; border: 1px solid #333; box-shadow: 0 0 30px rgba(0,0,0,0.8); }
        input { width: 100%; padding: 18px; margin: 12px 0; background: #000; border: 1px solid #333; color: white; border-radius: 12px; box-sizing: border-box; font-family: 'Cairo'; outline: none; font-size: 1rem; }
        input:focus { border-color: var(--gold); box-shadow: 0 0 10px rgba(255,184,0,0.2); }
        .send-btn { width: 100%; padding: 20px; background: linear-gradient(45deg, var(--gold), #ff8c00); border: none; border-radius: 12px; font-weight: 900; font-size: 1.5rem; cursor: pointer; margin-top: 20px; color: black; transition
