<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIDNIGHT CLUB | DESKTOP</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Kanit:ital,wght@1,900&family=Montserrat:wght@400;700&display=swap');
        :root { --brand-red: #ff0000; --dark-bg: #020505; }
        body { background: var(--dark-bg); color: #fff; font-family: 'Montserrat', sans-serif; margin: 0; }
        nav { display: flex; justify-content: space-between; padding: 20px 10%; border-bottom: 2px solid var(--brand-red); background: #000; }
        .hero { height: 50vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; border-bottom: 2px solid var(--brand-red); background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1544015759-11459bb65cc3?q=80&w=2000') center/cover; }
        .hero h1 { font-family: 'Kanit', sans-serif; font-size: 6rem; font-style: italic; filter: drop-shadow(0 0 20px var(--brand-red)); }
        .hero h1 span { display: block; color: var(--brand-red); font-size: 3rem; font-family: 'Bebas Neue'; letter-spacing: 12px; }
        .container { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; max-width: 1200px; margin: 50px auto; padding: 0 20px; }
        .card { background: #0d0000; padding: 40px; border-left: 5px solid var(--brand-red); transition: 0.3s; }
        .card:hover { transform: translateY(-10px); box-shadow: 0 10px 30px rgba(255, 0, 0, 0.3); }
        .card h2 { font-family: 'Bebas Neue', sans-serif; color: var(--brand-red); font-size: 2.2rem; margin-bottom: 15px; }
        .about-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; max-width: 1200px; margin: 0 auto 100px; padding: 0 20px; }
        .about-item { background: #111; padding: 20px; border: 1px solid #333; }
        .about-item h4 { color: var(--brand-red); font-family: 'Bebas Neue'; margin-bottom: 5px; }
        footer { text-align: center; padding: 50px; border-top: 1px solid #222; font-family: 'Bebas Neue'; color: #444; }
        .hidden { display: none; }
    </style>
</head>
<body>
    <nav><div style="font-family:'Kanit'; font-style:italic; font-size:2rem;">MIDNIGHT <span style="color:var(--brand-red)">CLUB</span></div></nav>
    
    <div id="home-view">
        <div class="hero"><h1>MIDNIGHT<span>CLUB</span></h1></div>
        <div class="container">
            <div class="card"><h2>MC STUDIO</h2><p>Exclusive pictorial sessions for all members. Showcase your custom liveries and high-performance units.</p></div>
            <div class="card"><h2>RED LEGACY</h2><p>Ang bagong haring kalsada ng gabi. Solid na samahan at disiplina ang aming pundasyon.</p></div>
            <div class="card"><h2>NIGHT DRIVING</h2><p>Sumali sa pinaka-prestihiyosong Red-themed coop sa buong Diesel n Steel server.</p></div>
        </div>
        <div style="text-align:center; margin-bottom:100px;">
            <button onclick="toggleAbout()" style="font-family:'Bebas Neue'; font-size:2rem; padding:15px 60px; color:#fff; background:transparent; border:3px solid var(--brand-red); cursor:pointer;">VIEW ABOUT 1-20</button>
        </div>
    </div>

    <div id="about-view" class="hidden">
        <div class="hero" style="height:30vh;"><h1>ABOUT<span>1-20 RULES</span></h1></div>
        <div class="about-grid" id="pc-about-list"></div>
        <div style="text-align:center; margin-bottom:100px;">
            <button onclick="toggleAbout()" style="font-family:'Bebas Neue'; font-size:2rem; padding:15px 60px; color:#fff; background:transparent; border:3px solid var(--brand-red); cursor:pointer;">GO BACK HOME</button>
        </div>
    </div>

    <footer>MAKER: <b style="color:var(--brand-red); font-size:1.5rem;">--VINCE--</b></footer>

    <script>
        const aboutData = [
            ["MC Identity", "Elite Red-themed coop sa Diesel n Steel."],
            ["Vision", "Maging pinaka-malupit na samahan sa gabi."],
            ["Red Neon", "Simbolo ng bilis at init ng samahan."],
            ["MC Studio", "Bukás ang pictorial para sa lahat ng miyembro."],
            ["Discipline", "Disiplina sa trapiko ang aming sandigan."],
            ["Brotherhood", "Walang driver ang naiiwan sa terminal."],
            ["Roleplay Focus", "Seryosong transport roleplay ang puhunan."],
            ["Engine Mastery", "Pagtuturo ng tamang engine tuning."],
            ["Livery Support", "Eksklusibong design para sa members."],
            ["Convoy Power", "Organisadong hatawan gabi-gabi."],
            ["No Toxic Policy", "Zero tolerance sa toxic behaviors."],
            ["Member Perks", "Priority sa studio photo sessions."],
            ["Route Efficiency", "Efficient farming strategies."],
            ["Midnight Events", "Weekly races and livery contests."],
            ["Leader's Command", "Sumunod sa tagubilin ni Idol Vince."],
            ["Community Bond", "Laro na naging tunay na pamilya."],
            ["Passenger Safety", "Safe driving kahit naka-hataw mode."],
            ["Modern Style", "Modernong porma ng Philippine Jeepney."],
            ["Future Goals", "Dominasyon bilang #1 Red Coop."],
            ["Solidarity", "Solid hanggang huling terminal!"]
        ];

        const pcList = document.getElementById('pc-about-list');
        aboutData.forEach((item, i) => {
            pcList.innerHTML += `<div class="about-item"><h4>${i+1}. ${item[0]}</h4><p style="font-size:0.9rem; color:#aaa;">${item[1]}</p></div>`;
        });

        function toggleAbout() {
            document.getElementById('home-view').classList.toggle('hidden');
            document.getElementById('about-view').classList.toggle('hidden');
            window.scrollTo(0,0);
        }
    </script>
</body>
</html>
