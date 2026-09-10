<!DOCTYPE html>
<html lang="om" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ferhan Shaamil | فرحان شامل</title>
<meta name="description" content="Ferhan Shaamil — Da'ii, Barsiisaa Qur'aanaa fi Beekumsa Shari'aa, Software Engineering Student. Markaza Uweysii Ibnu Aamir.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth}
:root{
  --bg:#040d09;--bg2:#0a1f15;--card:rgba(11,44,30,.72);--card2:#0b2419;
  --green:#0d9e6e;--green-d:#0d5138;--gold:#d6b45d;--gold-l:#f2d98d;
  --white:#f7f5ed;--text:#d1ddd6;--muted:#98aea4;--border:rgba(214,180,93,.25);
  --glow:0 0 40px rgba(214,180,93,.15);
}
body{
  font-family:'Cairo',Arial,sans-serif;
  background:radial-gradient(circle at 10% 20%,rgba(214,180,93,.08),transparent 30%),
             radial-gradient(circle at 90% 70%,rgba(13,158,110,.12),transparent 35%),
             var(--bg);
  color:var(--white);line-height:1.9;min-height:100vh;overflow-x:hidden;
}
a{color:inherit;text-decoration:none}
.container{width:min(1180px,92%);margin:0 auto}

/* ===== NAVBAR ===== */
nav{position:fixed;top:0;left:0;right:0;z-index:999;background:rgba(4,13,9,.9);
  backdrop-filter:blur(20px);-webkit-backdrop-filter:blur(20px);
  border-bottom:1px solid var(--border);padding:0 5%;transition:.3s}
.nav-inner{display:flex;justify-content:space-between;align-items:center;min-height:75px}
.logo{display:flex;align-items:center;gap:12px}
.logo-icon{width:44px;height:44px;border-radius:50%;border:1px solid var(--gold);
  display:grid;place-items:center;font-size:22px;color:var(--gold-l);
  background:radial-gradient(circle,rgba(214,180,93,.15),transparent 70%);box-shadow:var(--glow)}
.logo-text strong{display:block;color:var(--gold-l);font-size:15px;letter-spacing:.5px}
.logo-text small{display:block;color:var(--muted);font-size:10px;font-family:'Amiri',serif;direction:rtl}
.nav-links{display:flex;gap:20px;list-style:none;font-size:13px;align-items:center}
.nav-links a{color:var(--text);transition:.3s;font-weight:600;position:relative;padding:4px 0}
.nav-links a::after{content:'';position:absolute;bottom:0;left:0;width:0;height:2px;background:var(--gold);transition:.3s}
.nav-links a:hover{color:var(--gold-l)}
.nav-links a:hover::after{width:100%}
.nav-cta{border:1px solid var(--gold);padding:8px 16px;border-radius:30px;color:var(--gold-l)!important}
.menu-btn{display:none;font-size:28px;cursor:pointer;color:var(--gold-l);user-select:none}

/* ===== HERO ===== */
.hero{min-height:100vh;display:flex;align-items:center;padding:150px 0 80px;position:relative;overflow:hidden}
.hero::before{content:"";position:absolute;width:500px;height:500px;
  background:radial-gradient(circle,rgba(13,158,110,.2),transparent 70%);border-radius:50%;
  top:-100px;right:-100px;z-index:-1;animation:float 8s ease-in-out infinite}
.hero::after{content:"";position:absolute;width:400px;height:400px;
  background:radial-gradient(circle,rgba(214,180,93,.15),transparent 70%);border-radius:50%;
  bottom:-100px;left:-100px;z-index:-1;animation:float 10s ease-in-out infinite reverse}
@keyframes float{0%,100%{transform:translate(0,0)}50%{transform:translate(-30px,30px)}}
.hero-grid{display:grid;grid-template-columns:1.15fr .85fr;gap:50px;align-items:center}
.badge{display:inline-block;border:1px solid var(--border);background:rgba(214,180,93,.08);
  padding:8px 18px;border-radius:40px;color:var(--gold-l);font-size:13px;margin-bottom:20px;
  font-weight:700;animation:pulse 3s ease-in-out infinite}
@keyframes pulse{0%,100%{box-shadow:0 0 0 0 rgba(214,180,93,.3)}50%{box-shadow:0 0 0 12px rgba(214,180,93,0)}}
.hero h1{font-size:clamp(38px,6vw,74px);line-height:1.05;font-weight:900;letter-spacing:-1px;margin-bottom:5px}
.hero h1 span{background:linear-gradient(135deg,var(--gold-l),var(--gold));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.hero-arabic{font-family:'Amiri',serif;font-size:clamp(24px,3.5vw,38px);
  color:var(--gold-l);margin:10px 0 15px;direction:rtl;line-height:1.6}
.hero-sub{font-size:clamp(15px,2vw,19px);color:var(--gold);margin-bottom:18px;font-weight:700}
.hero-desc{color:var(--muted);font-size:15px;max-width:650px;margin-bottom:10px}
.hero-buttons{display:flex;flex-wrap:wrap;gap:15px;margin-top:30px}
.btn{padding:13px 28px;border-radius:35px;font-weight:700;font-size:14px;
  transition:.3s;display:inline-block;border:1px solid var(--gold);cursor:pointer}
.btn-primary{background:linear-gradient(135deg,var(--gold-l),var(--gold));color:#07130d;border:none}
.btn-primary:hover{transform:translateY(-4px);box-shadow:0 15px 40px rgba(214,180,93,.35)}
.btn-outline{background:transparent;color:var(--white)}
.btn-outline:hover{background:rgba(214,180,93,.1);border-color:var(--gold-l);transform:translateY(-3px)}
.hero-card{border:1px solid var(--border);background:var(--card);backdrop-filter:blur(15px);
  border-radius:35px;padding:40px 28px;text-align:center;box-shadow:0 30px 80px rgba(0,0,0,.4);transition:.4s}
.hero-card:hover{transform:translateY(-8px);border-color:var(--gold);box-shadow:0 40px 100px rgba(0,0,0,.5)}
.hero-symbol{width:140px;height:140px;margin:0 auto 22px;border-radius:50%;
  border:2px solid var(--gold);display:grid;place-items:center;font-size:65px;
  background:radial-gradient(circle,rgba(214,180,93,.2),transparent 65%);
  box-shadow:0 0 40px rgba(214,180,93,.25),inset 0 0 30px rgba(214,180,93,.1);
  animation:glow 4s ease-in-out infinite}
@keyframes glow{0%,100%{box-shadow:0 0 40px rgba(214,180,93,.25),inset 0 0 30px rgba(214,180,93,.1)}
  50%{box-shadow:0 0 60px rgba(214,180,93,.4),inset 0 0 40px rgba(214,180,93,.2)}}
.hero-card h3{color:var(--gold-l);font-size:22px;margin-bottom:5px}
.hero-card .ar{font-family:'Amiri',serif;font-size:22px;color:var(--gold);direction:rtl;margin:5px 0}
.hero-card p{color:var(--muted);font-size:13px}

/* ===== SECTIONS ===== */
section{padding:100px 0}
.section-head{text-align:center;max-width:800px;margin:0 auto 55px}
.section-mini{color:var(--gold);text-transform:uppercase;letter-spacing:4px;font-size:12px;font-weight:700}
.section-head h2{font-size:clamp(30px,5vw,48px);margin:10px 0}
.section-head h2 span{color:var(--gold-l)}
.section-head p{color:var(--muted);font-size:15px}
.section-head .arabic-sub{font-family:'Amiri',serif;color:var(--gold-l);font-size:22px;margin-top:5px;direction:rtl}

/* ===== CARDS ===== */
.card{background:var(--card);border:1px solid var(--border);border-radius:25px;
  padding:32px 28px;backdrop-filter:blur(10px);transition:.4s;position:relative;overflow:hidden}
.card::before{content:"";position:absolute;top:0;left:0;width:100%;height:3px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
  transform:translateX(-100%);transition:.6s}
.card:hover::before{transform:translateX(0)}
.card:hover{transform:translateY(-6px);border-color:var(--gold);box-shadow:0 20px 50px rgba(0,0,0,.3)}
.card h3{color:var(--gold-l);font-size:22px;margin-bottom:15px}
.card p{color:var(--muted);font-size:14px;margin-bottom:12px}

/* ===== ABOUT ===== */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:25px}
.skills{display:flex;flex-wrap:wrap;gap:9px;margin-top:20px}
.skill{border:1px solid var(--border);border-radius:20px;padding:6px 12px;
  color:var(--gold-l);background:rgba(214,180,93,.05);font-size:11px}

/* ===== WORK ===== */
.work-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px}
.work-item{background:var(--card);border:1px solid var(--border);border-radius:20px;
  padding:28px 20px;text-align:center;transition:.4s;position:relative;overflow:hidden}
.work-item::after{content:"";position:absolute;inset:0;
  background:radial-gradient(circle at center,rgba(214,180,93,.1),transparent 70%);
  opacity:0;transition:.4s}
.work-item:hover{transform:translateY(-8px);border-color:var(--gold)}
.work-item:hover::after{opacity:1}
.work-item .icon{font-size:42px;margin-bottom:12px;position:relative;z-index:1}
.work-item h4{color:var(--gold-l);font-size:16px;margin-bottom:8px;position:relative;z-index:1}
.work-item p{color:var(--muted);font-size:12px;position:relative;z-index:1}

/* ===== EDUCATION ===== */
.edu-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.edu-card{background:var(--card);border:1px solid var(--border);border-radius:22px;
  padding:28px 22px;transition:.4s;position:relative;overflow:hidden}
.edu-card:hover{transform:translateY(-8px);border-color:var(--gold);box-shadow:0 20px 50px rgba(0,0,0,.3)}
.edu-card::before{content:"";position:absolute;top:0;left:0;right:0;height:4px;
  background:linear-gradient(90deg,var(--gold),var(--gold-l),var(--gold));
  background-size:200% 100%;animation:shine 3s linear infinite}
@keyframes shine{0%{background-position:0% 50%}100%{background-position:200% 50%}}
.edu-card .icon{font-size:40px;margin-bottom:12px}
.edu-card h4{color:var(--gold-l);font-size:18px;margin-bottom:8px}
.edu-card p{color:var(--muted);font-size:13px}
.edu-card .duration{display:inline-block;margin-top:14px;padding:5px 14px;border-radius:20px;
  background:rgba(214,180,93,.1);border:1px solid var(--border);color:var(--gold-l);
  font-size:12px;font-weight:700}
.materials{display:flex;flex-wrap:wrap;gap:8px;margin-top:16px;padding-top:16px;border-top:1px solid var(--border)}
.mat-btn{display:inline-flex;align-items:center;gap:5px;padding:7px 13px;border-radius:20px;
  font-size:11px;font-weight:700;transition:.3s;border:1px solid var(--border);
  background:rgba(255,255,255,.03);color:var(--text)}
.mat-btn:hover{transform:translateY(-2px) scale(1.05)}
.mat-btn.pdf{color:#ff8a8a;border-color:rgba(255,138,138,.3)}
.mat-btn.pdf:hover{background:rgba(255,138,138,.1);border-color:#ff8a8a}
.mat-btn.video{color:#8ac6ff;border-color:rgba(138,198,255,.3)}
.mat-btn.video:hover{background:rgba(138,198,255,.1);border-color:#8ac6ff}
.mat-btn.audio{color:#8affb5;border-color:rgba(138,255,181,.3)}
.mat-btn.audio:hover{background:rgba(138,255,181,.1);border-color:#8affb5}
.mat-btn.text{color:var(--gold-l);border-color:var(--border)}
.mat-btn.text:hover{background:rgba(214,180,93,.1);border-color:var(--gold)}

/* ===== SCHEDULE ===== */
.schedule-grid{display:grid;grid-template-columns:1fr 1fr;gap:25px;max-width:800px;margin:0 auto}
.schedule-card{background:var(--card);border:1px solid var(--border);border-radius:22px;
  padding:35px 25px;text-align:center;transition:.4s}
.schedule-card:hover{transform:translateY(-5px);border-color:var(--gold)}
.schedule-card .icon{font-size:48px;margin-bottom:12px}
.schedule-card h4{color:var(--gold-l);font-size:20px;margin-bottom:10px}
.schedule-card p{color:var(--text);font-size:16px;font-weight:600}

/* ===== MARKAZA ===== */
.markaza-box{border:1px solid var(--gold);border-radius:32px;padding:60px 30px;
  background:radial-gradient(circle at center,rgba(13,158,110,.15),transparent 60%),rgba(8,25,18,.85);
  text-align:center;position:relative;overflow:hidden}
.markaza-box::before{content:"۞";position:absolute;font-size:350px;
  color:rgba(214,180,93,.03);top:50%;left:50%;transform:translate(-50%,-50%);z-index:0}
.markaza-box h2{color:var(--gold-l);font-size:clamp(28px,4vw,42px);margin-bottom:15px;position:relative;z-index:1}
.markaza-box .ar{font-family:'Amiri',serif;font-size:24px;color:#eee4c8;direction:rtl;
  margin:15px 0;position:relative;z-index:1;line-height:1.8}
.markaza-box p{color:var(--muted);max-width:800px;margin:0 auto 12px;font-size:16px;position:relative;z-index:1}

/* ===== VISION ===== */
.vision-box{border:1px solid var(--gold);border-radius:32px;padding:50px 30px;
  background:radial-gradient(circle at center,rgba(13,158,110,.12),transparent 60%),rgba(8,25,18,.85);
  text-align:center}
.vision-box p{color:var(--muted);max-width:800px;margin:0 auto;font-size:16px}

/* ===== MESSAGE ===== */
.message-box{border:1px solid var(--border);border-radius:28px;padding:50px 30px;
  background:var(--card);text-align:center;position:relative}
.message-box blockquote{font-size:clamp(22px,3.5vw,34px);color:var(--gold-l);
  font-weight:700;line-height:1.6;margin-bottom:20px;font-family:'Amiri',serif;direction:rtl}
.message-box p{color:var(--muted);font-size:16px;max-width:750px;margin:0 auto}

/* ===== PROJECTS ===== */
.project-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.project{background:var(--card);border:1px solid var(--border);border-radius:22px;
  padding:28px;transition:.4s}
.project:hover{transform:translateY(-8px);border-color:var(--gold);box-shadow:0 20px 50px rgba(0,0,0,.3)}
.project h4{color:var(--gold-l);font-size:18px;margin-bottom:10px}
.project p{color:var(--muted);font-size:13px}

/* ===== SOCIAL ===== */
.social-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;max-width:900px;margin:0 auto}
.social-card{background:var(--card);border:1px solid var(--border);border-radius:25px;
  padding:30px 20px;text-align:center;transition:.4s;position:relative;overflow:hidden}
.social-card::before{content:"";position:absolute;top:-50%;left:-50%;width:200%;height:200%;
  background:radial-gradient(circle,rgba(214,180,93,.08),transparent 60%);opacity:0;transition:.5s}
.social-card:hover{transform:translateY(-8px);border-color:var(--gold);box-shadow:0 20px 50px rgba(0,0,0,.3)}
.social-card:hover::before{opacity:1}
.social-card .s-icon{font-size:42px;margin-bottom:12px;position:relative;z-index:1;transition:.3s}
.social-card:hover .s-icon{transform:scale(1.15)}
.social-card h4{color:var(--gold-l);font-size:17px;margin-bottom:6px;position:relative;z-index:1}
.social-card a{display:inline-block;color:var(--muted);font-size:12px;word-break:break-word;
  transition:.3s;position:relative;z-index:1}
.social-card a:hover{color:var(--gold-l)}

/* ===== CTA ===== */
.cta{text-align:center;padding:100px 20px;background:radial-gradient(circle,rgba(214,180,93,.1),transparent 55%);position:relative;overflow:hidden}
.cta .ar{font-family:'Amiri',serif;font-size:32px;color:var(--gold-l);direction:rtl;margin-bottom:15px}
.cta h2{font-size:clamp(32px,5vw,52px);color:var(--gold-l);margin:15px 0}
.cta p{color:var(--muted);max-width:600px;margin:0 auto 25px;font-size:16px}

/* ===== FOOTER ===== */
footer{border-top:1px solid var(--border);background:#020906;padding:50px 0;text-align:center}
footer strong{color:var(--gold-l);font-size:16px}
footer .ar{font-family:'Amiri',serif;font-size:24px;color:var(--gold);direction:rtl;margin:8px 0}
footer p{color:var(--muted);font-size:13px;margin:4px 0}
.footer-socials{margin-top:20px;display:flex;justify-content:center;gap:20px;flex-wrap:wrap}
.footer-socials a{color:var(--muted);font-size:26px;transition:.3s;display:inline-block}
.footer-socials a:hover{color:var(--gold-l);transform:scale(1.2) translateY(-3px)}

/* ===== FLOATING ===== */
.wa{position:fixed;bottom:25px;left:25px;width:58px;height:58px;border-radius:50%;
  background:linear-gradient(135deg,#25d366,#128c7e);display:grid;place-items:center;
  font-size:28px;z-index:500;box-shadow:0 10px 35px rgba(37,211,102,.4);transition:.3s;
  animation:waPulse 2s ease-in-out infinite}
.wa:hover{transform:scale(1.1);box-shadow:0 15px 45px rgba(37,211,102,.6)}
@keyframes waPulse{0%,100%{box-shadow:0 10px 35px rgba(37,211,102,.4)}
  50%{box-shadow:0 10px 35px rgba(37,211,102,.4),0 0 0 15px rgba(37,211,102,0)}}
.scroll-top{position:fixed;bottom:25px;right:25px;width:50px;height:50px;border-radius:50%;
  background:var(--card);border:1px solid var(--gold);color:var(--gold-l);
  display:grid;place-items:center;font-size:22px;cursor:pointer;z-index:500;
  opacity:0;visibility:hidden;transition:.3s}
.scroll-top.show{opacity:1;visibility:visible}
.scroll-top:hover{background:var(--gold);color:#07130d;transform:translateY(-4px)}

/* ===== RESPONSIVE ===== */
@media(max-width:900px){
  .nav-links{position:absolute;top:75px;left:0;width:100%;background:var(--bg2);
    flex-direction:column;padding:25px;gap:15px;display:none;border-bottom:1px solid var(--border)}
  .nav-links.active{display:flex}
  .menu-btn{display:block}
  .hero-grid,.about-grid{grid-template-columns:1fr;text-align:center}
  .hero-desc{margin:0 auto}
  .hero-buttons{justify-content:center}
  .work-grid{grid-template-columns:1fr 1fr}
  .edu-grid{grid-template-columns:1fr 1fr}
  .project-grid{grid-template-columns:1fr}
  .social-grid{grid-template-columns:1fr 1fr}
  .schedule-grid{grid-template-columns:1fr}
}
@media(max-width:550px){
  .work-grid,.edu-grid,.social-grid{grid-template-columns:1fr}
  .hero{padding-top:120px}
  section{padding:70px 0}
  .vision-box,.message-box{padding:35px 20px}
  .markaza-box{padding:40px 20px}
  .wa{width:52px;height:52px;font-size:24px}
}
</style>
</head>
<body>

<!-- ===== NAVBAR ===== -->
<nav id="navbar">
  <div class="container nav-inner">
    <a href="#home" class="logo">
      <div class="logo-icon">🌿</div>
      <div class="logo-text">
        <strong>FERHAN SHAAMIL</strong>
        <small>فرحان شامل</small>
      </div>
    </a>
    <div class="menu-btn" onclick="toggleMenu()">☰</div>
    <ul class="nav-links" id="navLinks">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#work">Work</a></li>
      <li><a href="#education">Barnoota</a></li>
      <li><a href="#markaza">Markaza</a></li>
      <li><a href="#vision">Vision</a></li>
      <li><a href="#social">Social</a></li>
      <li><a href="#contact" class="nav-cta">Contact</a></li>
    </ul>
  </div>
</nav>

<!-- ===== HERO ===== -->
<section class="hero" id="home">
  <div class="container hero-grid">
    <div>
      <div class="badge">🌿✨ OFFICIAL PERSONAL WEBSITE</div>
      <h1>FERHAN<br><span>SHAAMIL</span></h1>
      <div class="hero-arabic">فرحان شامل</div>
      <div class="hero-sub">Da'ii • Barsiisaa Qur'aanaa Fi Beekumsa Shari'aa • Barataa Software Engineering</div>
      <p class="hero-desc">
        Ani Ferhan Shaamil, Barsiisaa Markaza Uweysii Ibnu Aamir,
        Da'ii Fi Nama Dhaloota Qur'aanaa, Beekumsa Shari'aa Fi Akkaataa Jireenyaa
        Gaarii Irratti Kakaasuudha.
      </p>
      <p class="hero-desc" style="margin-top:10px">
        Kaayyoon Koo Beekumsa Qofa Dabarsuu Osoo Hin Taane, Beekumsa Sana
        Jireenya Keessatti Hojiiirra Oolchuuf Dhaloota Qopheessuudha.
      </p>
      <p class="hero-desc" style="margin-top:10px">
        Qur'aana Jaalachuu, Diinii Hubachuu, Akhlaaqa Gaarii Horachuu Fi
        Teknooloojii Sirriitti Fayyadamuun Dhaloota Boruu Ijaaruuf Nan Hojjedha.
      </p>
      <div class="hero-buttons">
        <a href="#about" class="btn btn-primary">👤 Waa'ee Kiyya</a>
        <a href="#education" class="btn btn-outline">📚 Barnoota</a>
      </div>
    </div>
    <div class="hero-card">
      <div class="hero-symbol">🌿</div>
      <h3>Ferhan Shaamil</h3>
      <div class="ar">فرحان شامل</div>
      <p>Da'ii • Barsiisaa • Software Engineering Student</p>
      <p style="margin-top:15px">📖 Qur'aana<br>🕌 Da'waa<br>💻 Technology</p>
    </div>
  </div>
</section>

<!-- ===== ABOUT ===== -->
<section id="about">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">About Me</div>
      <h2>🌿 Waa'ee <span>Kiyya</span></h2>
      <p>Ferhan Shaamil — Da'ii, Barsiisaa Qur'aanaa Fi Beekumsa Shari'aa, Akkasumas Barataa Software Engineering Ti.</p>
    </div>
    <div class="about-grid">
      <div class="card">
        <h3>👤 Eenyu Ani?</h3>
        <p>Ani Barsiisaa Markaza Uweysii Ibnu Aamir, Da'ii Fi Nama Dhaloota Qur'aanaa, Beekumsa Shari'aa Fi Akkaataa Jireenyaa Gaarii Irratti Kakaasuudha.</p>
        <p>Kaayyoon Koo Beekumsa Qofa Dabarsuu Osoo Hin Taane, Beekumsa Sana Jireenya Keessatti Hojiiirra Oolchuuf Dhaloota Qopheessuudha.</p>
        <p>Qur'aana Jaalachuu, Diinii Hubachuu, Akhlaaqa Gaarii Horachuu Fi Teknooloojii Sirriitti Fayyadamuun Dhaloota Boruu Ijaaruuf Nan Hojjedha.</p>
      </div>
      <div class="card">
        <h3>🎯 Kaayyoo Kiyya</h3>
        <p>Dhaloonni Keenya Qur'aana Isaa Akka Beeku, Rabbii Isaa Akka Beeku, Nabiyyii Isaa ﷺ Akka Jaalatu, Diinii Isaa Akka Hubatu Fi Jireenya Isaa Akka Gaariitti Ijaaru Gumaacha Gochuu.</p>
        <div class="skills">
          <span class="skill">📖 Qur'aana</span>
          <span class="skill">🕌 Da'waa</span>
          <span class="skill">📚 Shari'aa</span>
          <span class="skill">🌱 Tarbiyaa</span>
          <span class="skill">💻 Software Engineering</span>
          <span class="skill">🌐 Web Development</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== WORK ===== -->
<section id="work" style="background:rgba(7,22,15,.4)">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">What I Do</div>
      <h2>💡 Waan Ani Irratti <span>Hojjedhu</span></h2>
    </div>
    <div class="work-grid">
      <div class="work-item"><div class="icon">📖</div><h4>Qur'aana</h4><p>Qur'aana Barachuu, Barsiisuu Fi Jaalala Qur'aanaa Dhaloota Keessatti Cimsuu.</p></div>
      <div class="work-item"><div class="icon">🕌</div><h4>Da'waa</h4><p>Nama Gara Kheeyrii, Beekumsaa, Tawhiidaa Fi Hojii Gaarii Waamuu.</p></div>
      <div class="work-item"><div class="icon">📚</div><h4>Beekumsa Shari'aa</h4><p>Aqiidaa, Fiqhii, Seenaa Nabiyyii ﷺ Fi Barnoota Islaamaa Babal'isuu.</p></div>
      <div class="work-item"><div class="icon">🌱</div><h4>Tarbiyaa Fi Akhlaaqa</h4><p>Dhaloota Akhlaaqa Gaarii, Naamusa, Obsa Fi Itti Gaafatamummaa Qabu Ijaaruu.</p></div>
      <div class="work-item"><div class="icon">💻</div><h4>Software Engineering</h4><p>Teknooloojii Hubachuu Fi Furmaata Dijitaalaa Bu'a Qabeessa Uumuu.</p></div>
      <div class="work-item"><div class="icon">🌐</div><h4>Web Development</h4><p>Websitewwan Ammayyaa, Saffisaa Fi Fayyadamtootaaf Mijataa Ta'an Ijaaruu.</p></div>
      <div class="work-item"><div class="icon">🎨</div><h4>Digital Design</h4><p>Design Dijitaalaa Bareedaa, Qulqulluu Fi Ergaa Qabu Uumuu.</p></div>
      <div class="work-item"><div class="icon">🚀</div><h4>Teknooloojii Fi Barnoota</h4><p>Teknooloojii Akka Meeshaa Barnootaa, Da'waa Fi Tajaajila Hawaasaatti Fayyadamu.</p></div>
    </div>
  </div>
</section>

<!-- ===== EDUCATION ===== -->
<section id="education">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">Education Programs</div>
      <h2>📚 Sagantaalee <span>Barnootaa</span></h2>
      <p>Barnoota Qur'aanaa fi Beekumsa Shari'aa sadarkaa adda addaatiin.</p>
    </div>
    <div class="edu-grid">

      <div class="edu-card">
        <div class="icon">🔤</div>
        <h4>Qaacidda Nooraniyyaa</h4>
        <p>Sadarkaa jalqabaa fi daa'immaniif.</p>
        <span class="duration">🌱 Jalqabaaf</span>
        <div class="materials">
          <a href="kitaabota/nooraniyyaa.pdf" target="_blank" class="mat-btn pdf">📄 PDF</a>
          <a href="https://youtube.com/@ferhanshaamil" target="_blank" class="mat-btn video">🎥 Video</a>
          <a href="https://t.me/Ferhan_Shaamil" target="_blank" class="mat-btn audio">🎧 Sagalee</a>
          <a href="kitaabota/nooraniyyaa-text.pdf" target="_blank" class="mat-btn text">📝 Barreeffama</a>
        </div>
      </div>

      <div class="edu-card">
        <div class="icon">📖</div>
        <h4>Tilawaa fi Tajwiid</h4>
        <p>Makhaarij, Sifaat fi Ahkaama Tajwiid.</p>
        <span class="duration">⏳ 3 Ji'a</span>
        <div class="materials">
          <a href="kitaabota/tajwiid.pdf" target="_blank" class="mat-btn pdf">📄 PDF</a>
          <a href="https://youtube.com/@ferhanshaamil" target="_blank" class="mat-btn video">🎥 Video</a>
          <a href="https://t.me/Ferhan_Shaamil" target="_blank" class="mat-btn audio">🎧 Sagalee</a>
          <a href="kitaabota/tajwiid-text.pdf" target="_blank" class="mat-btn text">📝 Barreeffama</a>
        </div>
      </div>

      <div class="edu-card">
        <div class="icon">☝️</div>
        <h4>Aqiidaa</h4>
        <p>Tawhiida fi bu'uura Aqiidaa Islaamaa.</p>
        <span class="duration">⏳ 2 Ji'a</span>
        <div class="materials">
          <a href="kitaabota/aqiidaa.pdf" target="_blank" class="mat-btn pdf">📄 PDF</a>
          <a href="https://youtube.com/@ferhanshaamil" target="_blank" class="mat-btn video">🎥 Video</a>
          <a href="https://t.me/Ferhan_Shaamil" target="_blank" class="mat-btn audio">🎧 Sagalee</a>
          <a href="kitaabota/aqiidaa-text.pdf" target="_blank" class="mat-btn text">📝 Barreeffama</a>
        </div>
      </div>

      <div class="edu-card">
        <div class="icon">⚖️</div>
        <h4>Fiqhii fi Ahkaam</h4>
        <p>Ahkaama ibaadaa fi jireenyaa.</p>
        <span class="duration">⏳ 3 Ji'a</span>
        <div class="materials">
          <a href="kitaabota/fiqhii.pdf" target="_blank" class="mat-btn pdf">📄 PDF</a>
          <a href="https://youtube.com/@ferhanshaamil" target="_blank" class="mat-btn video">🎥 Video</a>
          <a href="https://t.me/Ferhan_Shaamil" target="_blank" class="mat-btn audio">🎧 Sagalee</a>
          <a href="kitaabota/fiqhii-text.pdf" target="_blank" class="mat-btn text">📝 Barreeffama</a>
        </div>
      </div>

      <div class="edu-card">
        <div class="icon">🌙</div>
        <h4>Seenaa Nabiyyii ﷺ</h4>
        <p>Jireenya fi Akhlaaqa Nabiyyii ﷺ.</p>
        <span class="duration">⏳ 2 Ji'a</span>
        <div class="materials">
          <a href="kitaabota/siiraa.pdf" target="_blank" class="mat-btn pdf">📄 PDF</a>
          <a href="https://youtube.com/@ferhanshaamil" target="_blank" class="mat-btn video">🎥 Video</a>
          <a href="https://t.me/Ferhan_Shaamil" target="_blank" class="mat-btn audio">🎧 Sagalee</a>
          <a href="kitaabota/siiraa-text.pdf" target="_blank" class="mat-btn text">📝 Barreeffama</a>
        </div>
      </div>

      <div class="edu-card">
        <div class="icon">✨</div>
        <h4>Sagantaa Guutuu</h4>
        <p>Qur'aana, Tajwiida, Aqiidaa, Fiqhii fi Seeraa.</p>
        <span class="duration">⏳ Ji'a 4</span>
        <div class="materials">
          <a href="kitaabota/sagantaa-guutuu.pdf" target="_blank" class="mat-btn pdf">📄 PDF</a>
          <a href="https://youtube.com/@ferhanshaamil" target="_blank" class="mat-btn video">🎥 Video</a>
          <a href="https://t.me/Ferhan_Shaamil" target="_blank" class="mat-btn audio">🎧 Sagalee</a>
          <a href="kitaabota/sagantaa-guutuu-text.pdf" target="_blank" class="mat-btn text">📝 Barreeffama</a>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ===== SCHEDULE ===== -->
<section style="background:rgba(7,22,15,.4)">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">Learning Schedule</div>
      <h2>📅 <span>Sagantaa</span></h2>
    </div>
    <div class="schedule-grid">
      <div class="schedule-card">
        <div class="icon">📅</div>
        <h4>Guyyaa</h4>
        <p>Sanbata hanga Kamisaatti.</p>
      </div>
      <div class="schedule-card">
        <div class="icon">⏰</div>
        <h4>Sa'aatii</h4>
        <p>2:30 PM — 5:30 PM</p>
      </div>
    </div>
  </div>
</section>

<!-- ===== MARKAZA ===== -->
<section id="markaza">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">Islamic Education Center</div>
      <h2>🌿 Markaza <span>Uweysii</span></h2>
      <p>Iddoo Qur'aanaa, Beekumsa Shari'aa fi Tarbiyaa.</p>
    </div>
    <div class="markaza-box">
      <h2>🌿✨ MARKAZA UWEYSII IBNU AAMIR ✨🌿</h2>
      <div class="ar">مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ<br>لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</div>
      <p>
        Markazni Uweysii Ibnu Aamir iddoo Qur'aana, Tajwiida, Aqiidaa, Fiqhii,
        Seenaa Nabiyyii ﷺ fi Akhlaaqa itti baratan.
      </p>
      <div class="ar" style="font-size:28px;color:var(--gold-l)">
        نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،<br>
        وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ
      </div>
      <p style="margin-top:20px">
        <a href="https://tinyurl.com/Uweysii-inbu-aamir-center" target="_blank" class="btn btn-primary">🕌 Markaza Website</a>
      </p>
    </div>
  </div>
</section>

<!-- ===== VISION ===== -->
<section id="vision" style="background:rgba(7,22,15,.3)">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">My Vision</div>
      <h2>🌟 Mul'ata <span>Kiyya</span></h2>
    </div>
    <div class="vision-box">
      <p>Dhaloota Qur'aana Jaalatu, Diinii Isaa Hubatu, Akhlaaqa Gaarii Horatu, Beekumsa Barbaadu Fi Teknooloojii Karaa Gaarii Ta'een Fayyadamu Ijaaruu.</p>
    </div>
  </div>
</section>

<!-- ===== MESSAGE ===== -->
<section>
  <div class="container">
    <div class="section-head">
      <div class="section-mini">My Message</div>
      <h2>✨ Ergaa <span>Kiyya</span></h2>
    </div>
    <div class="message-box">
      <blockquote>«بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ»</blockquote>
      <blockquote>"Beekumsa Baradhu, Dhaloota Ijaari, Jireenya Kee Ifa Godhi."</blockquote>
      <p>Jireenyi Nama Tokkoo Yeroo Inni Ofii Isaatiif Qofa Jiraatu Caalaa, Yeroo Inni Nama Biraa Fayyadu Hiika Guddaa Qaba. Beekumsi Yeroo Qoodamu Babal'ata; Dhaloonni Yeroo Qajeelfamu Ijaaramuu Danda'a.</p>
    </div>
  </div>
</section>

<!-- ===== PROJECTS ===== -->
<section style="background:rgba(7,22,15,.4)">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">My Work</div>
      <h2>🚀 <span>Projects</span></h2>
      <p>Hojiiwwan fi pirojektoota ani irratti hojjedhu.</p>
    </div>
    <div class="project-grid">
      <div class="project">
        <h4>🌿 Markaza Uweysii Website</h4>
        <p>Website Markaza Uweysii Ibnu Aamir, barnoota Qur'aanaa fi Beekumsa Shari'aa beeksisuuf qophaa'e.</p>
      </div>
      <div class="project">
        <h4>💻 Ferhan Portfolio</h4>
        <p>Website dhuunfaa koo kan Da'waa, barnoota fi Software Engineering walitti fidu.</p>
      </div>
      <div class="project">
        <h4>📚 Digital Learning</h4>
        <p>Yaada platformii barnootaa dijitaalaa Qur'aanaa fi beekumsaaf.</p>
      </div>
    </div>
  </div>
</section>

<!-- ===== SOCIAL ===== -->
<section id="social">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">Follow Me</div>
      <h2>📱 Nu <span>Hordofaa</span></h2>
      <p>Karaa armaan gaditiin na qunnamuu dandeessu</p>
    </div>
    <div class="social-grid">
      <div class="social-card">
        <div class="s-icon">📘</div>
        <h4>Facebook</h4>
        <a href="https://www.facebook.com/share/1D9P96HFwe/" target="_blank">facebook.com/share/1D9P96HFwe</a>
      </div>
      <div class="social-card">
        <div class="s-icon">🎵</div>
        <h4>TikTok</h4>
        <a href="https://www.tiktok.com/@mirkanihararge" target="_blank">@mirkanihararge</a>
      </div>
      <div class="social-card">
        <div class="s-icon">▶️</div>
        <h4>YouTube</h4>
        <a href="https://youtube.com/@ferhanshaamil" target="_blank">@ferhanshaamil</a>
      </div>
      <div class="social-card">
        <div class="s-icon">✈️</div>
        <h4>Telegram</h4>
        <a href="https://t.me/Ferhan_Shaamil" target="_blank">t.me/Ferhan_Shaamil</a>
      </div>
      <div class="social-card">
        <div class="s-icon">💬</div>
        <h4>WhatsApp</h4>
        <a href="https://wa.me/251915455051" target="_blank">+251 915 455 051</a>
      </div>
      <div class="social-card">
        <div class="s-icon">📧</div>
        <h4>Email</h4>
        <a href="mailto:Ferhanshaamil@gmail.com">Ferhanshaamil@gmail.com</a>
      </div>
    </div>
  </div>
</section>

<!-- ===== CTA ===== -->
<section class="cta" id="contact">
  <div class="container">
    <div class="ar">خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ</div>
    <h2>🤝 Nu Qunnami</h2>
    <p>
      Da'waa, barnoota, technology ykn hojii waliin hojjechuu irratti mari'achuuf na qunnami.<br><br>
      📧 <strong>Ferhanshaamil@gmail.com</strong><br>
      📞 <strong>+251 915 455 051</strong>
    </p>
    <a href="https://wa.me/251915455051" target="_blank" class="btn btn-primary">📱 WhatsApp</a>
  </div>
</section>

<!-- ===== FOOTER ===== -->
<footer>
  <div class="container">
    <strong>FERHAN SHAAMIL</strong>
    <div class="ar">فرحان شامل</div>
    <p>🕌 Da'ii • 📖 Barsiisaa Qur'aanaa fi Beekumsa Shari'aa • 💻 Software Engineering Student</p>
    <div class="footer-socials">
      <a href="https://www.facebook.com/share/1D9P96HFwe/" target="_blank" title="Facebook">📘</a>
      <a href="https://www.tiktok.com/@mirkanihararge" target="_blank" title="TikTok">🎵</a>
      <a href="https://youtube.com/@ferhanshaamil" target="_blank" title="YouTube">▶️</a>
      <a href="https://t.me/Ferhan_Shaamil" target="_blank" title="Telegram">✈️</a>
      <a href="https://wa.me/251915455051" target="_blank" title="WhatsApp">💬</a>
      <a href="mailto:Ferhanshaamil@gmail.com" title="Email">📧</a>
    </div>
    <p style="margin-top:20px">© 2026 Ferhan Shaamil. All Rights Reserved.</p>
  </div>
</footer>

<!-- ===== FLOATING ===== -->
<a href="https://wa.me/251915455051" target="_blank" class="wa" title="WhatsApp">💬</a>
<div class="scroll-top" onclick="window.scrollTo({top:0,behavior:'smooth'})" id="scrollTop">↑</div>

<script>
function toggleMenu(){document.getElementById("navLinks").classList.toggle("active")}
document.querySelectorAll(".nav-links a").forEach(l=>l.addEventListener("click",()=>document.getElementById("navLinks").classList.remove("active")));

const scrollTop=document.getElementById('scrollTop');
window.addEventListener('scroll',()=>{
  scrollTop.classList.toggle('show',window.scrollY>400);
  document.getElementById('navbar').style.boxShadow=window.scrollY>50?'0 10px 40px rgba(0,0,0,.4)':'none';
});

const observer=new IntersectionObserver((entries)=>{
  entries.forEach(e=>{if(e.isIntersecting){e.target.style.opacity='1';e.target.style.transform='translateY(0)';}});
},{threshold:.1});
document.querySelectorAll('section').forEach(s=>{
  s.style.opacity='0';s.style.transform='translateY(30px)';
  s.style.transition='opacity .8s ease, transform .8s ease';
  observer.observe(s);
});
</script>

</body>
</html>
