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

<!DOCTYPE html>
<html lang="om">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ferhan Shaamil | Da'ii • Islamic Educator • Software Engineering Student</title>

  <meta name="description" content="Official personal website of Ferhan Shaamil — Da'ii, Teacher at Markaza Uweysii Ibnu Aamir, and Software Engineering Student.">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #06130f;
      color: #f5f5f5;
      line-height: 1.7;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      width: 90%;
      max-width: 1150px;
      margin: auto;
    }

    /* ================= HEADER ================= */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(6, 19, 15, 0.92);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(212, 175, 55, 0.15);
    }

    nav {
      min-height: 75px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 20px;
      font-weight: 800;
      letter-spacing: 1px;
      color: #d4af37;
    }

    .logo span {
      color: #ffffff;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    .nav-links a {
      color: #ddd;
      font-size: 14px;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: #d4af37;
    }

    /* ================= HERO ================= */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding-top: 100px;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 500px;
      height: 500px;
      background: #0d5c46;
      filter: blur(150px);
      opacity: 0.25;
      top: 100px;
      left: -200px;
    }

    .hero-content {
      max-width: 800px;
      position: relative;
      z-index: 2;
    }

    .small-title {
      color: #d4af37;
      font-size: 15px;
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-bottom: 15px;
    }

    .hero h1 {
      font-size: clamp(45px, 9vw, 90px);
      line-height: 1;
      margin-bottom: 20px;
      font-weight: 900;
    }

    .hero h1 span {
      color: #d4af37;
    }

    .arabic-title {
      font-size: clamp(22px, 4vw, 35px);
      direction: rtl;
      color: #e8d99b;
      margin-bottom: 20px;
      font-weight: bold;
    }

    .hero-subtitle {
      font-size: 20px;
      color: #b9c8c1;
      margin-bottom: 25px;
    }

    .hero-description {
      max-width: 700px;
      color: #9eada6;
      font-size: 16px;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 13px 25px;
      border-radius: 30px;
      display: inline-block;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn-primary {
      background: #d4af37;
      color: #06130f;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      background: #f0cf58;
    }

    .btn-outline {
      border: 1px solid #d4af37;
      color: #d4af37;
    }

    .btn-outline:hover {
      background: #d4af37;
      color: #06130f;
    }

    /* ================= SECTIONS ================= */

    section {
      padding: 100px 0;
    }

    .section-title {
      text-align: center;
      margin-bottom: 55px;
    }

    .section-title span {
      color: #d4af37;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 2px;
    }

    .section-title h2 {
      font-size: 38px;
      margin-top: 8px;
    }

    .section-title p {
      color: #9eada6;
      margin-top: 10px;
    }

    /* ================= ABOUT ================= */

    .about-grid {
      display: grid;
      grid-template-columns: 1.2fr 1fr;
      gap: 30px;
    }

    .card {
      background: #0a1d17;
      border: 1px solid rgba(212, 175, 55, 0.15);
      border-radius: 20px;
      padding: 30px;
    }

    .card h3 {
      color: #d4af37;
      margin-bottom: 15px;
    }

    .card p {
      color: #b5c2bc;
    }

    /* ================= IDENTITY ================= */

    .identity-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .identity-box {
      padding: 30px;
      text-align: center;
      background: linear-gradient(145deg, #0a2119, #07150f);
      border-radius: 20px;
      border: 1px solid rgba(212, 175, 55, 0.15);
    }

    .identity-icon {
      font-size: 40px;
      margin-bottom: 15px;
    }

    .identity-box h3 {
      margin-bottom: 8px;
    }

    .identity-box p {
      color: #9eada6;
      font-size: 14px;
    }

    /* ================= MARKAZA ================= */

    .markaza-box {
      background: linear-gradient(135deg, #0b261d, #07150f);
      border: 1px solid rgba(212, 175, 55, 0.25);
      border-radius: 25px;
      padding: 50px 30px;
      text-align: center;
    }

    .markaza-box h2 {
      color: #d4af37;
      margin-bottom: 15px;
      font-size: 30px;
    }

    .arabic {
      direction: rtl;
      font-size: 25px;
      color: #e8d99b;
      margin: 20px 0;
      line-height: 2;
    }

    .markaza-box p {
      color: #b9c8c1;
      max-width: 750px;
      margin: auto;
    }

    .quote {
      margin-top: 25px;
      font-size: 20px;
      color: #d4af37;
      font-weight: bold;
    }

    /* ================= PROGRAMS ================= */

    .program-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .program {
      background: #0a1d17;
      padding: 25px;
      border-radius: 18px;
      border: 1px solid rgba(212, 175, 55, 0.12);
      transition: 0.3s;
    }

    .program:hover {
      transform: translateY(-6px);
      border-color: rgba(212, 175, 55, 0.45);
    }

    .program-icon {
      font-size: 32px;
      margin-bottom: 10px;
    }

    .program h3 {
      margin-bottom: 8px;
    }

    .program p {
      color: #9eada6;
      font-size: 14px;
    }

    .duration {
      display: inline-block;
      margin-top: 12px;
      color: #d4af37;
      font-size: 13px;
    }

    /* ================= DA'WAH ================= */

    .dawah {
      background: #081a14;
    }

    .dawah-content {
      max-width: 850px;
      margin: auto;
      text-align: center;
    }

    .dawah-content p {
      color: #b9c8c1;
      font-size: 17px;
      margin-bottom: 25px;
    }

    /* ================= TECHNOLOGY ================= */

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      justify-content: center;
    }

    .skill {
      border: 1px solid rgba(212, 175, 55, 0.3);
      color: #e8d99b;
      padding: 10px 18px;
      border-radius: 30px;
      background: #0a1d17;
    }

    /* ================= LANGUAGES ================= */

    .languages {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
    }

    .language {
      text-align: center;
      padding: 20px;
      background: #0a1d17;
      border-radius: 15px;
    }

    .language strong {
      display: block;
      color: #d4af37;
      margin-bottom: 5px;
    }

    .language span {
      color: #9eada6;
      font-size: 13px;
    }

    /* ================= PROJECTS ================= */

    .projects {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .project {
      padding: 30px;
      background: #0a1d17;
      border-radius: 20px;
      border: 1px solid rgba(212, 175, 55, 0.15);
    }

    .project h3 {
      color: #d4af37;
      margin-bottom: 12px;
    }

    .project p {
      color: #9eada6;
      font-size: 14px;
    }

    /* ================= CONTACT ================= */

    .contact-box {
      max-width: 800px;
      margin: auto;
      text-align: center;
      padding: 50px 30px;
      border-radius: 25px;
      background: linear-gradient(145deg, #0b261d, #07150f);
      border: 1px solid rgba(212, 175, 55, 0.2);
    }

    .contact-box h2 {
      font-size: 35px;
      margin-bottom: 15px;
    }

    .contact-box p {
      color: #9eada6;
      margin-bottom: 25px;
    }

    /* ================= FOOTER ================= */

    footer {
      padding: 35px 0;
      text-align: center;
      border-top: 1px solid rgba(212, 175, 55, 0.12);
      color: #81918a;
      font-size: 13px;
    }

    footer strong {
      color: #d4af37;
    }

    /* ================= MOBILE ================= */

    @media (max-width: 850px) {

      .nav-links {
        display: none;
      }

      .about-grid,
      .identity-grid,
      .program-grid,
      .projects,
      .languages {
        grid-template-columns: 1fr;
      }

      .hero {
        text-align: center;
      }

      .hero-content {
        margin: auto;
      }

      .buttons {
        justify-content: center;
      }

      .hero h1 {
        font-size: 50px;
      }

      section {
        padding: 75px 0;
      }

      .section-title h2 {
        font-size: 30px;
      }
    }
  </style>
</head>

<body>

<!-- ================= HEADER ================= -->

<header>
  <div class="container">
    <nav>

      <div class="logo">
        FERHAN <span>SHAAMIL</span>
      </div>

      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#dawah">Da'wah</a></li>
        <li><a href="#markaza">Markaza</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#technology">Technology</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>

    </nav>
  </div>
</header>


<!-- ================= HERO ================= -->

<section class="hero" id="home">

  <div class="container">

    <div class="hero-content">

      <div class="small-title">
        Official Personal Website
      </div>

      <h1>
        FERHAN <span>SHAAMIL</span>
      </h1>

      <div class="arabic-title">
        داعية ومعلّم للقرآن والعلوم الشرعية
      </div>

      <div class="hero-subtitle">
        Barsiisaa • Da'ii • Barataa Software Engineering
      </div>

      <p class="hero-description">
        Ani Ferhan Shaamil AbdulGafur, barsiisaa Markaza Uweysii Ibnu Aamir,
        Da'ii fi barataa Software Engineering ti.
        Kaayyoon koo Qur'aanaa fi beekumsa sirrii barsiisuu,
        dhaloota ijaaruu fi teknooloojii karaa gaarii ta'een fayyadamuudha.
      </p>

      <div class="buttons">
        <a href="#about" class="btn btn-primary">
          👤 About Me
        </a>

        <a href="#markaza" class="btn btn-outline">
          🕌 Markaza Uweysii
        </a>
      </div>

    </div>

  </div>

</section>


<!-- ================= ABOUT ================= -->

<section id="about">

  <div class="container">

    <div class="section-title">
      <span>About Me</span>
      <h2>👤 Waa'ee Koo</h2>
      <p>Nama ani ta'e, hojii koo fi kaayyoo koo.</p>
    </div>

    <div class="about-grid">

      <div class="card">

        <h3>🌿 Ferhan Shaamil AbdulGafur</h3>

        <p>
          Ani barsiisaa Markaza Uweysii Ibnu Aamir,
          Da'ii fi barataa Software Engineering ti.
          Barnoota Qur'aanaa fi علوم شرعية irratti barsiisuu,
          beekumsa babal'isuu fi dhaloota akhlaaqa gaarii qabu ijaaruun
          hojii koo keessaa isa ijoodha.
        </p>

        <br>

        <p>
          Akkasumas teknooloojii ammayyaa akka meeshaa barnootaa,
          da'waa fi tajaajila hawaasaaf fayyadamu irratti xiyyeeffadha.
        </p>

      </div>

      <div class="card">

        <h3>🎯 Mul'ata Koo</h3>

        <p>
          Dhaloota Qur'aana jaallatu, beekumsa Shari'aa qabu,
          akhlaaqa gaarii horatu fi teknooloojii ammayyaa
          karaa bu'a qabeessa ta'een fayyadamu ijaaruu.
        </p>

        <br>

        <h3>✨ Kaayyoo</h3>

        <p>
          Beekumsa sirrii barsiisuu, nama gaarii ijaaruu,
          dhaloota kakaasuu fi hawaasa keessatti gahee gaarii taphachuu.
        </p>

      </div>

    </div>

  </div>

</section>


<!-- ================= IDENTITY ================= -->

<section>

  <div class="container">

    <div class="section-title">
      <span>My Identity</span>
      <h2>✨ Eenyu Ani?</h2>
    </div>

    <div class="identity-grid">

      <div class="identity-box">
        <div class="identity-icon">🕌</div>
        <h3>Da'ii</h3>
        <p>
          Nama gara kheeyrii, beekumsa fi hojii gaarii waamu.
        </p>
      </div>

      <div class="identity-box">
        <div class="identity-icon">📖</div>
        <h3>Islamic Educator</h3>
        <p>
          Barsiisaa Qur'aanaa fi علوم شرعية.
        </p>
      </div>

      <div class="identity-box">
        <div class="identity-icon">💻</div>
        <h3>Software Engineering</h3>
        <p>
          Barataa Software Engineering fi technology enthusiast.
        </p>
      </div>

    </div>

  </div>

</section>


<!-- ================= DA'WAH ================= -->

<section class="dawah" id="dawah">

  <div class="container">

    <div class="section-title">
      <span>Da'wah & Education</span>
      <h2>🕌 Da'waa fi Barnoota</h2>
    </div>

    <div class="dawah-content">

      <p>
        Da'waan koo Qur'aanaa fi Sunnah irratti hundaa'uun
        nama gara beekumsaa, tawhiidaa, akhlaaqa gaarii fi hojii gaarii
        waamuudha.
      </p>

      <p>
        Dargaggoota fi hawaasa keessatti jaalala Qur'aanaa,
        beekumsa Shari'aa, naamusa gaarii fi itti gaafatamummaa cimsuu
        irratti xiyyeeffadha.
      </p>

      <p>
        Teknooloojii ammayyaa illee akka karaa barnootaa fi da'waa
        babal'isuutti itti fayyadamuun kaayyoo koo keessaa isa tokko.
      </p>

    </div>

  </div>

</section>


<!-- ================= MARKAZA ================= -->

<section id="markaza">

  <div class="container">

    <div class="section-title">
      <span>Islamic Education Center</span>
      <h2>🌿 Markaza Uweysii</h2>
      <p>Iddoo Qur'aanaa, Beekumsa Shari'aa fi Tarbiyaa.</p>
    </div>

    <div class="markaza-box">

      <h2>
        🌿✨ MARKAZA UWEYSII IBNU AAMIR ✨🌿
      </h2>

      <div class="arabic">
        مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ
        <br>
        لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
      </div>

      <p>
        Markazni Uweysii Ibnu Aamir iddoo Qur'aana,
        Tajwiida, Aqiidaa, Fiqhii, Seenaa Nabiyyii ﷺ
        fi Akhlaaqa itti baratan.
      </p>

      <div class="quote">
        نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ
      </div>

    </div>

  </div>

</section>


<!-- ================= PROGRAMS ================= -->

<section id="education">

  <div class="container">

    <div class="section-title">
      <span>Education Programs</span>
      <h2>📚 Sagantaalee Barnootaa</h2>
    </div>

    <div class="program-grid">

      <div class="program">
        <div class="program-icon">🔤</div>
        <h3>Qaacidda Nooraniyyaa</h3>
        <p>
          Sadarkaa jalqabaa fi daa'immaniif.
        </p>
      </div>

      <div class="program">
        <div class="program-icon">📖</div>
        <h3>Tilawaa fi Tajwiid</h3>
        <p>
          Makhaarij, Sifaat fi Ahkaama Tajwiid.
        </p>
        <span class="duration">3 Ji'a</span>
      </div>

      <div class="program">
        <div class="program-icon">☝️</div>
        <h3>Aqiidaa</h3>
        <p>
          Tawhiida fi bu'uura Aqiidaa Islaamaa.
        </p>
        <span class="duration">2 Ji'a</span>
      </div>

      <div class="program">
        <div class="program-icon">⚖️</div>
        <h3>Fiqhii fi Ahkaam</h3>
        <p>
          Ahkaama ibaadaa fi jireenyaa.
        </p>
        <span class="duration">3 Ji'a</span>
      </div>

      <div class="program">
        <div class="program-icon">🌙</div>
        <h3>Seenaa Nabiyyii ﷺ</h3>
        <p>
          Jireenya fi Akhlaaqa Nabiyyii ﷺ.
        </p>
        <span class="duration">2 Ji'a</span>
      </div>

      <div class="program">
        <div class="program-icon">✨</div>
        <h3>Sagantaa Guutuu</h3>
        <p>
          Qur'aana, Tajwiida, Aqiidaa, Fiqhii fi Seeraa.
        </p>
        <span class="duration">3 Ji'a</span>
      </div>

    </div>

  </div>

</section>


<!-- ================= TIME ================= -->

<section>

  <div class="container">

    <div class="section-title">
      <span>Learning Schedule</span>
      <h2>📅 Sagantaa</h2>
    </div>

    <div class="about-grid">

      <div class="card">
        <h3>📅 Guyyaa</h3>
        <p>
          Sanbata hanga Kamisaatti.
        </p>
      </div>

      <div class="card">
        <h3>⏰ Sa'aatii</h3>
        <p>
          2:30 PM — 5:30 PM
        </p>
      </div>

    </div>

  </div>

</section>


<!-- ================= TECHNOLOGY ================= -->

<section id="technology">

  <div class="container">

    <div class="section-title">
      <span>Technology</span>
      <h2>💻 Software Engineering</h2>
      <p>
        Teknooloojii akka meeshaa barnootaa fi tajaajila hawaasaatti.
      </p>
    </div>

    <div class="skills">

      <div class="skill">HTML</div>
      <div class="skill">CSS</div>
      <div class="skill">JavaScript</div>
      <div class="skill">React</div>
      <div class="skill">Java</div>
      <div class="skill">Python</div>
      <div class="skill">Git</div>
      <div class="skill">GitHub</div>

    </div>

  </div>

</section>


<!-- ================= LANGUAGES ================= -->

<section>

  <div class="container">

    <div class="section-title">
      <span>Languages</span>
      <h2>🌍 Afaanota</h2>
    </div>

    <div class="languages">

      <div class="language">
        <strong>Afaan Oromoo</strong>
        <span>Native</span>
      </div>

      <div class="language">
        <strong>العربية</strong>
        <span>Advanced</span>
      </div>

      <div class="language">
        <strong>አማርኛ</strong>
        <span>Advanced</span>
      </div>

      <div class="language">
        <strong>English</strong>
        <span>Intermediate</span>
      </div>

    </div>

  </div>

</section>


<!-- ================= PROJECTS ================= -->

<section id="projects">

  <div class="container">

    <div class="section-title">
      <span>My Work</span>
      <h2>🚀 Projects</h2>
      <p>
        Hojiiwwan fi pirojektoota ani irratti hojjedhu.
      </p>
    </div>

    <div class="projects">

      <div class="project">
        <h3>🌿 Markaza Uweysii Website</h3>
        <p>
          Website Markaza Uweysii Ibnu Aamir,
          barnoota Qur'aanaa fi علوم شرعية beeksisuuf qophaa'e.
        </p>
      </div>

      <div class="project">
        <h3>💻 Ferhan Portfolio</h3>
        <p>
          Website dhuunfaa koo kan Da'waa,
          barnoota fi Software Engineering walitti fidu.
        </p>
      </div>

      <div class="project">
        <h3>📚 Digital Learning</h3>
        <p>
          Yaada platformii barnootaa dijitaalaa
          Qur'aanaa fi beekumsaaf.
        </p>
      </div>

    </div>

  </div>

</section>


<!-- ================= FINAL MESSAGE ================= -->

<section>

  <div class="container">

    <div class="markaza-box">

      <div class="arabic">
        الْقُرْآنُ يَنْتَظِرُكَ! 📖
      </div>

      <h2>
        Beekumsa Baradhu — Dhaloota Ijaari
      </h2>

      <p>
        Qur'aana Baradhu, Diinii Kee Hubadhu,
        Akhlaaqa Kee Miidhagsi.
      </p>

      <br>

      <a href="#contact" class="btn btn-primary">
        🤝 Nu Qunnami
      </a>

    </div>

  </div>

</section>


<!-- ================= CONTACT ================= -->

<section id="contact">

  <div class="container">

    <div class="section-title">
      <span>Contact</span>
      <h2>📞 Na Qunnami</h2>
    </div>

    <div class="contact-box">

      <h2>
        Let's Connect
      </h2>

      <p>
        Da'waa, barnoota, technology ykn hojii waliin hojjechuu
        irratti mari'achuuf na qunnami.
      </p>

      <!-- EMAIL KEE ASITTI GALCHI -->
      <a href="mailto:com.com"
        class="btn btn-primary">
        📧 Email Me
      </a>

    </div>

  </div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

  <div class="container">

    <p>
      © 2026 <strong>Ferhan Shaamil AbdulGafur</strong>.
      All Rights Reserved.
    </p>

    <p>
      🕌 Da'ii • 📖 Islamic Educator • 💻 Software Engineering Student
    </p>

  </div>

</footer>

</body>
</html><!DOCTYPE html>
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
</html>              <div class="markaza-box">
                  <h2>🌿✨ Markaza Uweysii Ibnu Aamir ✨🌿</h2>
                  
                      <div class="arabic">
                            مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ
                                  لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
                                      </div>
                                      
                                          <p>
                                                Iddoo Qur’aana, Tajwiida, Aqiidaa, Fiqhii,
                                                      Seenaa Nabiyyii ﷺ fi Akhlaaqa itti baratan.
                                                          </p>
                                                          
                                                              <div class="markaza-quote">
                                                                    نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ
                                                                        </div>
                                                                          </div>
                                                                          
                                                                            <!-- KAAYYOO -->
                                                                              <div class="section-title">
                                                                                  <span>Kaayyoo Keenya</span>
                                                                                      <h2>🎯 Maalif Hojjenna?</h2>
                                                                                        </div>
                                                                                        
                                                                                          <div class="program-grid">
                                                                                          
                                                                                              <div class="program">
                                                                                                    <div class="program-icon">📖</div>
                                                                                                          <h3>Qur’aana & Tajwiida</h3>
                                                                                                                <p>Qur’aana sirriitti dubbisuu fi Tajwiida barachuu.</p>
                                                                                                                    </div>
                                                                                                                    
                                                                                                                        <div class="program">
                                                                                                                              <div class="program-icon">☝️</div>
                                                                                                                                    <h3>Aqiidaa</h3>
                                                                                                                                          <p>Bu’uura Tawhiidaa fi Aqiidaa Islaamaa barachuu.</p>
                                                                                                                                              </div>
                                                                                                                                              
                                                                                                                                                  <div class="program">
                                                                                                                                                        <div class="program-icon">⚖️</div>
                                                                                                                                                              <h3>Fiqhii</h3>
                                                                                                                                                                    <p>Ahkaama ibaadaa fi jireenyaa barachuu.</p>
                                                                                                                                                                        </div>
                                                                                                                                                                        
                                                                                                                                                                            <div class="program">
                                                                                                                                                                                  <div class="program-icon">🌙</div>
                                                                                                                                                                                        <h3>Seenaa Nabiyyii ﷺ</h3>
                                                                                                                                                                                              <p>Jireenya fi Akhlaaqa Nabiyyii ﷺ irraa barachuu.</p>
                                                                                                                                                                                                  </div>
                                                                                                                                                                                                  
                                                                                                                                                                                                      <div class="program">
                                                                                                                                                                                                            <div class="program-icon">🌱</div>
                                                                                                                                                                                                                  <h3>Tarbiyaa</h3>
                                                                                                                                                                                                                        <p>Akhlaaqa gaarii, obsa fi safuu Islaamaa cimsuu.</p>
                                                                                                                                                                                                                            </div>
                                                                                                                                                                                                                            
                                                                                                                                                                                                                                <div class="program">
                                                                                                                                                                                                                                      <div class="program-icon">💻</div>
                                                                                                                                                                                                                                            <h3>Barnoota Ammayyaa</h3>
                                                                                                                                                                                                                                                  <p>Teknooloojii barnootaaf sirriitti fayyadamu.</p>
                                                                                                                                                                                                                                                      </div>
                                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                        </div>
                                                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                          <!-- SAGANTAA -->
                                                                                                                                                                                                                                                            <div class="section-title">
                                                                                                                                                                                                                                                                <span>Sagantaalee Barnootaa</span>
                                                                                                                                                                                                                                                                    <h2>📚 Barnoota Keenya</h2>
                                                                                                                                                                                                                                                                      </div>
                                                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                        <div class="program-grid">
                                                                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                                            <div class="program">
                                                                                                                                                                                                                                                                                  <h3>🔤 Qaacidda Nooraniyyaa</h3>
                                                                                                                                                                                                                                                                                        <p>Sadarkaa jalqabaa fi daa’immaniif.</p>
                                                                                                                                                                                                                                                                                            </div>
                                                                                                                                                                                                                                                                                            
                                                                                                                                                                                                                                                                                                <div class="program">
                                                                                                                                                                                                                                                                                                      <h3>📖 Tilawaa fi Tajwiid</h3>
                                                                                                                                                                                                                                                                                                            <p>Makhaarij, Sifaat fi Ahkaama Tajwiid.</p>
                                                                                                                                                                                                                                                                                                                  <span class="duration">3 Ji’a</span>
                                                                                                                                                                                                                                                                                                                      </div>
                                                                                                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                                                                          <div class="program">
                                                                                                                                                                                                                                                                                                                                <h3>☝️ Aqiidaa Sirrii</h3>
                                                                                                                                                                                                                                                                                                                                      <p>Tawhiida fi bu’uura Aqiidaa Islaamaa.</p>
                                                                                                                                                                                                                                                                                                                                            <span class="duration">2 Ji’a</span>
                                                                                                                                                                                                                                                                                                                                                </div>
                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                    <div class="program">
                                                                                                                                                                                                                                                                                                                                                          <h3>⚖️ Fiqhii fi Ahkaam</h3>
                                                                                                                                                                                                                                                                                                                                                                <p>Ahkaama ibaadaa fi jireenyaa.</p>
                                                                                                                                                                                                                                                                                                                                                                      <span class="duration">3 Ji’a</span>
                                                                                                                                                                                                                                                                                                                                                                          </div>
                                                                                                                                                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                                                                                              <div class="program">
                                                                                                                                                                                                                                                                                                                                                                                    <h3>🌙 Seenaa Nabiyyii ﷺ</h3>
                                                                                                                                                                                                                                                                                                                                                                                          <p>Jireenya fi Akhlaaqa Nabiyyii ﷺ.</p>
                                                                                                                                                                                                                                                                                                                                                                                                <span class="duration">2 Ji’a</span>
                                                                                                                                                                                                                                                                                                                                                                                                    </div>
                                                                                                                                                                                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                                                                                                                                                        <div class="program">
                                                                                                                                                                                                                                                                                                                                                                                                              <h3>✨ Sagantaa Guutuu</h3>
                                                                                                                                                                                                                                                                                                                                                                                                                    <p>Qur’aana, Tajwiida, Aqiidaa, Fiqhii fi Seeraa.</p>
                                                                                                                                                                                                                                                                                                                                                                                                                          <span class="duration">3 Ji’a</span>
                                                                                                                                                                                                                                                                                                                                                                                                                              </div>
                                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                                                </div>
                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                                                                                                  <!-- BARATTOOTA -->
                                                                                                                                                                                                                                                                                                                                                                                                                                    <div class="section-title">
                                                                                                                                                                                                                                                                                                                                                                                                                                        <span>Barattoota Keenya</span>
                                                                                                                                                                                                                                                                                                                                                                                                                                            <h2>👥 Eenyutu Barachuu Danda’a?</h2>
                                                                                                                                                                                                                                                                                                                                                                                                                                                <p>Daa’imman, shamarran, dargaggoota fi nama barachuu barbaadu hunda.</p>
                                                                                                                                                                                                                                                                                                                                                                                                                                                  </div>
                                                                                                                                                                                                                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                                                                                                                                                    <!-- YEROO -->
                                                                                                                                                                                                                                                                                                                                                                                                                                                      <div class="about-grid">
                                                                                                                                                                                                                                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                                                                                                                                                                                                          <div class="card">
                                                                                                                                                                                                                                                                                                                                                                                                                                                                <h3>📅 Guyyaa</h3>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                      <p>Sanbata hanga Kamisaatti.</p>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                          </div>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                                                                                                                                                                                              <div class="card">
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    <h3>⏰ Sa’aatii</h3>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          <p>2:30 PM — 5:30 PM</p>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              </div>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                </div>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  <!-- GALMEE -->
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    <div class="markaza-box" id="galmee">
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        <div class="arabic">
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              استمارة التسجيل في برامج العلوم الشرعية
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  </div>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      <h2>📝 Amma Galmaa’i</h2>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          <p>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                Sagantaa siif mijatu filadhu; imala barnootaa kee har’a jalqabi.
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    </p>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        <a
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              href="https://forms.google.com"
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    target="_blank"
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          class="btn btn-primary"
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              >
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    📝 Foormii Galmee Guuti
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        </a>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            <a href="#contact" class="btn btn-outline">
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  💬 Nu Qunnami
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      </a>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        </div>
                                                                                                                                                                                                                                                                                                                                <!-- =========================
     MARKAZA UWEYSII
========================== -->

<section class="markaza" id="markaza">

  <div class="section-title">

    <span>Markaza Uweysii Ibnu Aamir</span>

    <h2>🌿 Markaza Uweysii</h2>

    <p>
      Iddoo Qur’aana, Beekumsa Shari’aa, Tarbiyaa Fi
      Akkaataa Jireenyaa Gaarii Itti Baratan.
    </p>

  </div>


  <!-- =========================
       SEENAA MARKAZAA
  ========================== -->

  <div class="markaza-box">

    <h2>
      🌿✨ Markaza Uweysii Ibnu Aamir ✨🌿
    </h2>

    <div class="arabic">
      مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ
      لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
    </div>

    <div class="markaza-subtitle">
      Iddoo Beekumsa Shari’aa Fi Qur’aana Kabajamaa
    </div>

    <p>
      Manara Beekumsa Shari’aa Fi Qur’aana Kabajamaa
    </p>

    <div class="markaza-quote">
      Nu Barsiifna Qur’aana Akkuma Buufametti,
      Dhaloota Qur’aanaa Sirriitti Leenjifna.
    </div>

    <p>
      Markazni Uweysii Ibnu Aamir Iddoo Barattoonni
      Qur’aana, Tajwiida, Aqiidaa, Fiqhii, Seenaa Nabiyyii ﷺ
      Fi Beekumsa Shari’aa Karaa Sirrii Fi Tartiiba Qabuun
      Itti Baratanidha.
    </p>

  </div>


  <!-- =========================
       SEENAA
  ========================== -->

  <div class="markaza-story">

    <div class="section-title">

      <span>Seenaa Keenya</span>

      <h2>📖 Seenaa Markazaa</h2>

      <p>
        Markazni Keenya Yaada Dhaloota Qur’aanaa Ijaaru
        Irraa Ka’e.
      </p>

    </div>


    <div class="about-grid">

      <div class="card">

        <h3>🌱 Jalqaba Keenya</h3>

        <p>
          Markazni Uweysii Ibnu Aamir Yaada Tokko Irraa
          Ka’e: Dhaloota Qur’aana Jaalatu, Qur’aana Sirriitti
          Dubbisu, Diinii Isaa Beeku Fi Akhlaaqa Gaarii Qabu
          Ijaaru.
        </p>

        <br>

        <p>
          Kaayyoon Keenya Barnoota Qur’aanaa Fi Shari’aa
          Tartiiba Qabuun Dhalootaaf Dhiyeessuu Fi Imala
          Beekumsaa Isaanii Cimsuudha.
        </p>

      </div>


      <div class="card">

        <h3>🕌 Maqaa Markazaa</h3>

        <p>
          Maqaan <strong>Uweysii Ibnu Aamir</strong>
          Jireenya Nama Ibaadaa, Ikhlaasa, Obsa Fi Sodaa
          Rabbii Tiin Beekamaa Ture Yaadachiisa.
        </p>

        <br>

        <p>
          Maqaan Kun Barattootaaf Fakkeenya Gaarii Ta’uun,
          Ikhlaasa, Hojii Gaarii Fi Jireenya Rabbii Wajjin
          Walitti Hidhame Yaadachiisa.
        </p>

      </div>

    </div>

  </div>


  <!-- =========================
       KAAYYOO
  ========================== -->

  <div class="markaza-goals">

    <div class="section-title">

      <span>Kaayyoo Keenya</span>

      <h2>🎯 Maalif Hojjenna?</h2>

      <p>
        Beekumsa Qofa Kennuu Osoo Hin Taane,
        Beekumsa Jireenyatti Hiikuu Barbaanna.
      </p>

    </div>


    <div class="program-grid">


      <div class="program">

        <div class="program-icon">📖</div>

        <h3>Qur’aana</h3>

        <p>
          Qur’aana Sirnaan Dubbisuu, Tajwiida Barachuu,
          Qalbii Keessatti Jaalala Qur’aanaa Cimsuu Fi
          Hojiiirra Oolchuu.
        </p>

      </div>


      <div class="program">

        <div class="program-icon">☝️</div>

        <h3>Aqiidaa</h3>

        <p>
          Tawhiida Fi Bu’uura Aqiidaa Islaamaa Sirriitti
          Hubachuun Amantii Jabaa Ijaaru.
        </p>

      </div>


      <div class="program">

        <div class="program-icon">🕌</div>

        <h3>Fiqhii</h3>

        <p>
          Ahkaama Ibaadaa Fi Dhimma Jireenyaa
          Muslimni Guyyaa Guyyaan Itti Fayyadamu Barachuu.
        </p>

      </div>


      <div class="program">

        <div class="program-icon">🌙</div>

        <h3>Seenaa Nabiyyii ﷺ</h3>

        <p>
          Jireenya Nabiyyii ﷺ, Akhlaaqa Isaa,
          Da’waa Isaa Fi Barnoota Jireenya Isaa Irraa Barachuu.
        </p>

      </div>


      <div class="program">

        <div class="program-icon">🌱</div>

        <h3>Tarbiyaa Fi Akhlaaqa</h3>

        <p>
          Amala Gaarii, Obsa, Kabaja, Itti-gaafatamummaa
          Fi Safuu Islaamaa Cimsuu.
        </p>

      </div>


      <div class="program">

        <div class="program-icon">💻</div>

        <h3>Barnoota Ammayyaa</h3>

        <p>
          Teknooloojii Fi Barnoota Ammayyaa Sirriitti
          Fayyadamuun Beekumsa Babal’isuu.
        </p>

      </div>

    </div>

  </div>


  <!-- =========================
       SAGANTAALEE BARNOOTAA
  ========================== -->

  <div class="markaza-programs">

    <div class="section-title">

      <span>Sagantaalee Barnootaa</span>

      <h2>📚 Barnoota Keenya</h2>

      <p>
        Barnoonni Keenya Sadarkaa Barataa Fi Fedhii
        Isaa Irratti Hundaa’uun Qindaa’a.
      </p>

    </div>


    <div class="program-grid">


      <div class="program">

        <div class="program-icon">🔤</div>

        <h3>Qaacidda Nooraniyyaa</h3>

        <p>
          Namoota Qur’aana Dubbisuu Jalqaban,
          Daa’immanii Fi Barattoota Sadarkaa Jalqabaatiif.
        </p>

        <span class="duration">
          Sadarkaa Jalqabaa
        </span>

      </div>


      <div class="program">

        <div class="program-icon">📖</div>

        <h3>Tilawaa Fi Tajwiid</h3>

        <p>
          Makhaarij, Sifaat, Ahkaam Tajwiid, Madd
          Fi Sirna Dubbisa Qur’aanaa Sirreessuu.
        </p>

        <span class="duration">
          3 Ji’a
        </span>

      </div>


      <div class="program">

        <div class="program-icon">☝️</div>

        <h3>Aqiidaa Sirrii</h3>

        <p>
          Tawhiida, Iimaana Fi Bu’uura Aqiidaa Islaamaa
          Hubannoo Sirriin Barachuu.
        </p>

        <span class="duration">
          2 Ji’a
        </span>

      </div>


      <div class="program">

        <div class="program-icon">⚖️</div>

        <h3>Fiqhii Fi Ahkaam</h3>

        <p>
          Ahkaama Ibaadaa Fi Dhimma Jireenyaa
          Karaa Sirrii Ta’een Barachuu.
        </p>

        <span class="duration">
          3 Ji’a
        </span>

      </div>


      <div class="program">

        <div class="program-icon">🌙</div>

        <h3>Seenaa Nabiyyii ﷺ</h3>

        <p>
          Jireenya Nabiyyii ﷺ, Akhlaaqa Isaa Fi
          Barnoota Jireenya Isaa Irraa Argamu Barachuu.
        </p>

        <span class="duration">
          2 Ji’a
        </span>

      </div>


      <div class="program">

        <div class="program-icon">✨</div>

        <h3>Sagantaa Guutuu</h3>

        <p>
          Qur’aana, Tajwiida, Aqiidaa, Fiqhii Fi
          Seenaa Nabiyyii ﷺ Walitti Qabu.
        </p>

        <span class="duration">
          3 Ji’a
        </span>

      </div>

    </div>

  </div>


  <!-- =========================
       BARATTOOTA
  ========================== -->

  <div class="students">

    <div class="section-title">

      <span>Barattoota Keenya</span>

      <h2>👥 Eenyutu Barachuu Danda’a?</h2>

      <p>
        Namni Barachuu Barbaadu Kamiyyuu Sadarkaa
        Isaatti Haala Mijatuun Barachuu Danda’a.
      </p>

    </div>


    <div class="about-grid">


      <div class="card">

        <h3>👦 Daa’imman</h3>

        <p>
          Daa’imman Qur’aana Dubbisuu, Qaacidda Nooraniyyaa,
          Tajwiida Bu’uuraa Fi Akhlaaqa Gaarii Baratu.
        </p>

      </div>


      <div class="card">

        <h3>👩‍🎓 Shamarran Fi Dubartoota</h3>

        <p>
          Qur’aana Fi Beekumsa Shari’aa Barachuun
          Beekumsa Isaanii Cimsachuu Fi Jireenya Isaanii
          Keessatti Hojiiirra Oolchuu Danda’u.
        </p>

      </div>


      <div class="card">

        <h3>👨‍🎓 Dargaggoota</h3>

        <p>
          Dargaggoonni Qur’aana, Aqiidaa, Fiqhii,
          Seenaa Nabiyyii ﷺ Fi Akhlaaqa Irratti
          Beekumsa Horachuu Danda’u.
        </p>

      </div>


      <div class="card">

        <h3>📚 Nama Barachuu Barbaadu Hunda</h3>

        <p>
          Umurii Fi Sadarkaan Kee Maaliyyuu Ta’u,
          Yoo Barachuu Barbaadde, Imala Beekumsaa Kee
          Asirraa Jalqabuu Dandeessa.
        </p>

      </div>

    </div>

  </div>


  <!-- =========================
       IMALA BARATAA
  ========================== -->

  <div class="student-journey">

    <div class="section-title">

      <span>Imala Barataa</span>

      <h2>🚀 Sadarkaa Barnootaa</h2>

      <p>
        Barataan Sadarkaa Tokko Irraa Gara Sadarkaa
        Itti Aanuutti Tartiiba Qabuun Ce’a.
      </p>

    </div>


    <div class="book-grid">

      <div class="book">

        <strong>01 — 🔤 Jalqabaa</strong>

        <span>
          Bu’uura Qur’aanaa Fi Qaacidda Nooraniyyaa.
        </span>

      </div>


      <div class="book">

        <strong>02 — 📖 Giddugaleessaa</strong>

        <span>
          Tilawaa, Tajwiida Fi Barnoota Shari’aa.
        </span>

      </div>


      <div class="book">

        <strong>03 — 📚 Olaanaa</strong>

        <span>
          Aqiidaa, Fiqhii, Hadith Fi Seenaa.
        </span>

      </div>


      <div class="book">

        <strong>04 — 🎓 Xumuraa</strong>

        <span>
          Qormaata Xumuraa Fi Ragaa Xumuraa.
        </span>

      </div>

    </div>

  </div>


  <!-- =========================
       GALMEE
  ========================== -->

  <div class="registration" id="galmee">

    <div class="section-title">

      <span>Galmee Galmaa’uu</span>

      <h2>📝 Amma Galmaa’i</h2>

      <p>
        Sagantaa Siif Mijatu Filadhu; Imala Barnootaa Kee
        Har’a Jalqabi.
      </p>

    </div>


    <div class="markaza-box">

      <div class="arabic">
        استمارة التسجيل في برامج العلوم الشرعية
      </div>

      <p>
        Barnoota Qur’aanaa Fi Ulumu Shari’aa Barachuuf
        Gara Markaza Uweysii Ibnu Aamiritti Nu Wajjin Deemi.
      </p>

      <br>


      <div class="registration-list">

        <div class="book">
          <strong>👤 Maqaa Guutuu</strong>
          <span>
            Maqaa Kee Guutuu Galchi.
          </span>
        </div>


        <div class="book">
          <strong>🎂 Umurii</strong>
          <span>
            Umurii Kee Galchi.
          </span>
        </div>


        <div class="book">
          <strong>📱 Lakkoofsa Bilbila</strong>
          <span>
            Lakkoofsa Si Qunnaman Galchi.
          </span>
        </div>


        <div class="book">
          <strong>💬 WhatsApp</strong>
          <span>
            Lakkoofsa WhatsApp Kee Galchi.
          </span>
        </div>


        <div class="book">
          <strong>📖 Sadarkaa Qur’aanaa</strong>
          <span>
            Sadarkaa Jalqabaa, Giddugaleessaa Ykn Olaanaa.
          </span>
        </div>


        <div class="book">
          <strong>📚 Sagantaa Filadhu</strong>
          <span>
            Nooraniyyaa, Tajwiida, Aqiidaa, Fiqhii,
            Seenaa Ykn Sagantaa Guutuu.
          </span>
        </div>

      </div>


      <div class="buttons">

        <a
          href="https://forms.google.com"
          target="_blank"
          class="btn btn-primary"
        >
          📝 Foormii Galmee Guuti
        </a>

        <a
          href="#contact"
          class="btn btn-outline"
        >
          💬 Nu Qunnami
        </a>

      </div>

    </div>

  </div>


  <!-- =========================
       YEROO BARNOOTAA
  ========================== -->

  <div class="schedule">

    <div class="section-title">

      <span>Yeroo Barnootaa</span>

      <h2>🕐 Sagantaa Yeroo</h2>

      <p>
        Barnoonni Markazaa Yeroo Qindaa’een Gaggeeffama.
      </p>

    </div>


    <div class="about-grid">


      <div class="card">

        <h3>📅 Guyyaa</h3>

        <p>
          Sanbata Irraa Hanga Kamisaatti.
        </p>

      </div>


      <div class="card">

        <h3>⏰ Sa’aatii</h3>

        <p>
          2:30 PM — 5:30 PM
        </p>

      </div>


      <div class="card">

        <h3>📚 Sirna Barnootaa</h3>

        <p>
          Barnoota, Shaakala, Irra-Deebii,
          Qormaata Fi Madaallii Barataa.
        </p>

      </div>


      <div class="card">

        <h3>🎓 Xumura</h3>

        <p>
          Barataan Ulaagaalee Sagantaa Isaa Erga Guutee
          Booda Qormaata Xumuraa Fi Ragaa Xumuraa Argata.
        </p>

      </div>

    </div>

  </div>


  <!-- =========================
       ERGAA XUMURAA
  ========================== -->

  <div class="markaza-box">

    <div class="arabic">
      الْقُرْآنُ يَنْتَظِرُكَ! 📖
    </div>

    <h2>
      Beekumsa Baradhu — Dhaloota Ijaari
    </h2>

    <p>
      Qur’aana Baradhu, Diinii Kee Hubadhu,
      Akhlaaqa Kee Miidhagsi, Jireenya Kee Ifa Godhi.
    </p>

    <br>

    <div class="arabic">
      الرِّحْلَةُ تَبْدَأُ مِنْ هُنَا 🚀
    </div>

    <div class="buttons">

      <a
        href="#galmee"
        class="btn btn-primary"
      >
        🚀 Amma Galmaa’i
      </a>

      <a
        href="#contact"
        class="btn btn-outline"
      >
        💬 Nu Qunnami
      </a>

    </div>

  </div>

</section><!DOCTYPE html>
<html lang="om" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>مركز أُويس بن عامر | لدراسة العلوم الشرعية</title>
  <meta name="description" content="مركز أُويس بن عامر — لدراسة العلوم الشرعية والقرآن الكريم. Ferhan Shaamil, داعية ومُعلّم.">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --bg: #04100c;
      --bg2: #071a13;
      --card: rgba(13, 42, 31, .72);
      --card2: #0b2419;
      --green: #0d5138;
      --green-light: #18704d;
      --gold: #d6b45d;
      --gold-light: #f2d98d;
      --white: #f7f5ed;
      --text: #d8e2dc;
      --muted: #9eaea6;
      --border: rgba(214, 180, 93, .25);
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: radial-gradient(circle at 15% 10%, rgba(214, 180, 93, .08), transparent 25%), radial-gradient(circle at 85% 40%, rgba(24, 112, 77, .12), transparent 30%), var(--bg);
      color: var(--white);
      line-height: 1.7;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1180px, 92%);
      margin: auto;
    }

    /* ===== NAVBAR ===== */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 999;
      background: rgba(4, 16, 12, .88);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid var(--border);
    }

    .nav {
      min-height: 76px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 11px;
    }

    .logo-mark {
      width: 45px;
      height: 45px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      border: 1px solid var(--gold);
      background: rgba(214, 180, 93, .06);
      font-size: 22px;
    }

    .logo-text strong {
      display: block;
      color: var(--gold-light);
      font-size: 14px;
      letter-spacing: .7px;
    }

    .logo-text small {
      display: block;
      color: var(--muted);
      font-size: 9px;
    }

    .nav-links {
      display: flex;
      gap: 20px;
      align-items: center;
      list-style: none;
      font-size: 13px;
    }

    .nav-links a {
      color: var(--text);
      transition: .3s;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .nav-contact {
      border: 1px solid var(--gold);
      padding: 8px 15px;
      border-radius: 25px;
      color: var(--gold-light) !important;
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 100vh;
      padding: 145px 0 80px;
      display: flex;
      align-items: center;
      position: relative;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 50px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      padding: 7px 15px;
      border: 1px solid var(--border);
      background: rgba(214, 180, 93, .06);
      border-radius: 30px;
      color: var(--gold-light);
      font-size: 12px;
      margin-bottom: 20px;
    }

    .hero h1 {
      font-size: clamp(40px, 6vw, 76px);
      line-height: 1.05;
      letter-spacing: -2px;
    }

    .hero h1 span {
      color: var(--gold-light);
    }

    .hero-title {
      color: var(--text);
      font-size: clamp(18px, 3vw, 25px);
      margin: 20px 0 12px;
    }

    .arabic {
      direction: rtl;
      text-align: right;
      font-family: "Times New Roman", serif;
    }

    .hero-arabic {
      color: var(--gold-light);
      font-size: clamp(22px, 3vw, 32px);
      margin: 15px 0;
    }

    .hero-description {
      max-width: 680px;
      color: var(--muted);
      font-size: 15px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 28px;
    }

    .btn {
      display: inline-block;
      padding: 12px 22px;
      border-radius: 30px;
      border: 1px solid var(--gold);
      font-weight: bold;
      font-size: 13px;
      transition: .3s;
    }

    .btn:hover {
      transform: translateY(-4px);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold-light), var(--gold));
      color: #07130e;
      border: none;
    }

    .hero-card {
      border: 1px solid var(--border);
      background: linear-gradient(145deg, rgba(18, 68, 48, .7), rgba(7, 27, 19, .8));
      border-radius: 35px;
      padding: 35px;
      text-align: center;
      box-shadow: 0 30px 70px rgba(0, 0, 0, .25);
    }

    .hero-symbol {
      width: 150px;
      height: 150px;
      margin: auto;
      border-radius: 50%;
      display: grid;
      place-items: center;
      border: 1px solid var(--gold);
      background: radial-gradient(circle, rgba(214, 180, 93, .15), transparent 65%);
      font-size: 70px;
    }

    .hero-card h3 {
      margin-top: 20px;
      color: var(--gold-light);
    }

    .hero-card p {
      color: var(--muted);
      font-size: 13px;
      margin-top: 7px;
    }

    /* ===== SECTIONS ===== */
    section {
      padding: 90px 0;
    }

    .section-head {
      text-align: center;
      max-width: 760px;
      margin: 0 auto 45px;
    }

    .section-mini {
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 3px;
      font-size: 11px;
    }

    .section-head h2 {
      font-size: clamp(29px, 5vw, 45px);
      margin: 7px 0;
    }

    .section-head p {
      color: var(--muted);
      font-size: 14px;
    }

    /* ===== ABOUT ===== */
    .personal {
      background: rgba(7, 26, 19, .55);
    }

    .personal-grid {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 25px;
      align-items: stretch;
    }

    .profile-card,
    .content-card {
      border: 1px solid var(--border);
      background: var(--card);
      border-radius: 27px;
      padding: 32px;
    }

    .profile-icon {
      width: 115px;
      height: 115px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      margin-bottom: 20px;
      border: 1px solid var(--gold);
      background: rgba(214, 180, 93, .07);
      font-size: 50px;
    }

    .profile-card h3 {
      color: var(--gold-light);
      font-size: 23px;
    }

    .profile-card .role {
      color: var(--muted);
      margin: 6px 0 20px;
      font-size: 13px;
    }

    .profile-list {
      list-style: none;
      display: grid;
      gap: 9px;
      color: var(--text);
      font-size: 13px;
    }

    .content-card h3 {
      color: var(--gold-light);
      margin-bottom: 12px;
      font-size: 24px;
    }

    .content-card p {
      color: var(--muted);
      margin-bottom: 14px;
    }

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-top: 20px;
    }

    .skill {
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 6px 12px;
      color: var(--gold-light);
      background: rgba(214, 180, 93, .05);
      font-size: 11px;
    }

    /* ===== MARKAZA ===== */
    .markaza-box {
      position: relative;
      overflow: hidden;
      text-align: center;
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 60px 25px;
      background: radial-gradient(circle at center, rgba(24, 112, 77, .28), transparent 60%), rgba(8, 29, 21, .75);
    }

    .markaza-icon {
      font-size: 50px;
    }

    .markaza-box h2 {
      color: var(--gold-light);
      font-size: clamp(27px, 5vw, 46px);
      margin-top: 10px;
    }

    .markaza-arabic {
      color: #eee4c8;
      font-size: 25px;
      margin: 8px 0 20px;
    }

    .markaza-box p {
      max-width: 780px;
      margin: auto;
      color: var(--muted);
    }

    /* ===== PROGRAMS ===== */
    .program-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .program {
      position: relative;
      border: 1px solid var(--border);
      border-radius: 23px;
      padding: 28px;
      background: var(--card2);
      transition: .35s;
      overflow: hidden;
    }

    .program:hover {
      transform: translateY(-7px);
      border-color: var(--gold);
    }

    .program-icon {
      font-size: 37px;
    }

    .program h3 {
      font-size: 18px;
      margin-top: 8px;
    }

    .program p {
      color: var(--muted);
      font-size: 13px;
      margin: 7px 0 15px;
    }

    .duration {
      display: inline-block;
      padding: 5px 11px;
      border-radius: 20px;
      border: 1px solid var(--border);
      color: var(--gold-light);
      font-size: 10px;
    }

    /* ===== CURRICULUM ===== */
    .curriculum {
      background: rgba(7, 26, 19, .55);
    }

    .book-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
    }

    .book {
      display: flex;
      gap: 16px;
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 22px;
      background: var(--card);
    }

    .book-icon {
      font-size: 31px;
    }

    .book h3 {
      color: var(--gold-light);
      font-size: 16px;
    }

    .book p {
      color: var(--muted);
      font-size: 12px;
      margin-top: 4px;
    }

    /* ===== MESSAGE ===== */
    .message-box {
      max-width: 900px;
      margin: auto;
      text-align: center;
      padding: 45px 25px;
      border-radius: 28px;
      border: 1px solid var(--border);
      background: linear-gradient(135deg, #0d3021, #071c14);
    }

    .message-box .arabic {
      text-align: center;
      color: var(--gold-light);
      font-size: 25px;
      line-height: 1.9;
    }

    .message-box p {
      color: var(--muted);
      margin-top: 18px;
      font-size: 14px;
    }

    /* ===== CONTACT ===== */
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .contact-card {
      text-align: center;
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 28px;
      background: var(--card);
      transition: .3s;
    }

    .contact-card:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
    }

    .contact-icon {
      font-size: 34px;
    }

    .contact-card h3 {
      color: var(--gold-light);
      margin: 8px 0;
    }

    .contact-card p {
      color: var(--muted);
      font-size: 13px;
      word-break: break-word;
    }

    /* ===== CTA ===== */
    .cta {
      text-align: center;
      padding: 95px 20px;
      background: radial-gradient(circle, rgba(24, 112, 77, .3), transparent 60%);
    }

    .cta .arabic {
      text-align: center;
      color: var(--gold-light);
      font-size: 28px;
      margin-bottom: 12px;
    }

    .cta h2 {
      font-size: clamp(32px, 6vw, 55px);
      color: var(--gold-light);
    }

    .cta p {
      color: var(--muted);
      max-width: 650px;
      margin: 10px auto 25px;
    }

    /* ===== FOOTER ===== */
    footer {
      border-top: 1px solid var(--border);
      background: #020a07;
      padding: 40px 0;
      text-align: center;
    }

    footer .footer-logo {
      font-size: 28px;
      margin-bottom: 8px;
    }

    footer strong {
      color: var(--gold-light);
    }

    footer p {
      color: var(--muted);
      font-size: 11px;
      margin-top: 5px;
    }

    /* ===== FLOATING WHATSAPP ===== */
    .floating {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 500;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: #16804f;
      border: 2px solid rgba(255, 255, 255, .2);
      font-size: 25px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, .4);
    }

    /* ===== RESPONSIVE ===== */
    @media(max-width:900px) {
      .nav-links {
        display: none;
      }
      .hero-grid,
      .personal-grid {
        grid-template-columns: 1fr;
      }
      .program-grid {
        grid-template-columns: repeat(2, 1fr);
      }
      .contact-grid {
        grid-template-columns: 1fr;
      }
    }

    @media(max-width:560px) {
      section {
        padding: 65px 0;
      }
      .hero {
        padding-top: 125px;
      }
      .hero h1 {
        font-size: 42px;
      }
      .hero-card {
        padding: 25px;
      }
      .program-grid,
      .book-grid {
        grid-template-columns: 1fr;
      }
      .profile-card,
      .content-card {
        padding: 24px;
      }
      .markaza-box {
        padding: 42px 18px;
      }
    }
  </style>
</head>

<body>

  <!-- ===== NAVIGATION ===== -->
  <nav>
    <div class="container nav">
      <a href="#home" class="logo">
        <div class="logo-mark">🌿</div>
        <div class="logo-text">
          <strong>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</strong>
          <small>لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</small>
        </div>
      </a>
      <ul class="nav-links">
        <li><a href="#home">الرئيسية</a></li>
        <li><a href="#about">عنِّي</a></li>
        <li><a href="#markaza">المركز</a></li>
        <li><a href="#programs">البرامج</a></li>
        <li><a href="#curriculum">المنهج</a></li>
        <li><a href="#contact" class="nav-contact">اتصل بنا</a></li>
      </ul>
    </div>
  </nav>

  <!-- ===== HERO ===== -->
  <section class="hero" id="home">
    <div class="container hero-grid">
      <div>
        <div class="badge">🌿✨ الْمَوْقِعُ الرَّسْمِيُّ • الْقُرْآنُ • الْعِلْمُ • التِّقْنِيَةُ</div>
        <h1>مَرْكَزُ<br><span>أُوَيْسِ بْنِ عَامِرٍ</span></h1>
        <div class="hero-title">لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ وَالْقُرْآنِ الْكَرِيمِ</div>
        <div class="arabic hero-arabic">مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</div>
        <p class="hero-description">
          مَرْكَزٌ عِلْمِيٌّ يَهْدِفُ إِلَى تَعْلِيمِ الْقُرْآنِ الْكَرِيمِ،
          وَالْعُلُومِ الشَّرْعِيَّةِ، وَتَرْبِيَةِ النَّشْءِ عَلَى الْأَخْلَاقِ الْفَاضِلَةِ،
          مَعَ تَسْخِيرِ التِّقْنِيَةِ الْحَدِيثَةِ فِي سَبِيلِ الدَّعْوَةِ وَالتَّعْلِيمِ.
        </p>
        <div class="hero-buttons">
          <a href="#markaza" class="btn btn-primary">🕌 تَعَرَّفْ عَلَى الْمَرْكَزِ</a>
          <a href="#programs" class="btn">📚 اِسْتَعْرِضِ الْبَرَامِجَ</a>
        </div>
      </div>
      <div class="hero-card">
        <div class="hero-symbol">🕌</div>
        <h3>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</h3>
        <p>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</p>
        <p style="margin-top:18px;">📖 الْقُرْآنُ<br>🕌 الْعُلُومُ الشَّرْعِيَّةُ<br>🌱 التَّرْبِيَةُ<br>💻 التِّقْنِيَةُ</p>
      </div>
    </div>
  </section>

  <!-- ===== ABOUT ===== -->
  <section class="personal" id="about">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">عَنِ الْمُدَرِّسِ</div>
        <h2>👤 فَرْحَانُ شَامِلُ عَبْدِ الْغَفُورِ</h2>
        <p>مُدَرِّسُ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ فِي الْمَرْكَزِ</p>
      </div>
      <div class="personal-grid">
        <div class="profile-card">
          <div class="profile-icon">👤</div>
          <h3>فَرْحَانُ شَامِلٌ</h3>
          <div class="role">دَاعِيَةٌ • مُعَلِّمٌ • طَالِبُ هَنْدَسَةِ الْبَرْمَجِيَّاتِ</div>
          <ul class="profile-list">
            <li>🕌 مُعَلِّمٌ فِي مَرْكَزِ أُوَيْسِ بْنِ عَامِرٍ</li>
            <li>📖 تَعْلِيمُ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ</li>
            <li>🌱 تَرْبِيَةُ النَّشْءِ وَبِنَاؤُهُمْ</li>
            <li>💻 هَنْدَسَةُ الْبَرْمَجِيَّاتِ</li>
            <li>🚀 التَّعْلِيمُ الرَّقْمِيُّ</li>
          </ul>
        </div>
        <div class="content-card">
          <h3>🌿 رِسَالَةُ الْمُدَرِّسِ</h3>
          <p>
            أَنَا فَرْحَانُ شَامِلٌ، أَسْعَى إِلَى تَعْلِيمِ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ بِطَرِيقَةٍ عَصْرِيَّةٍ،
            وَبِنَاءِ جِيلٍ يَجْمَعُ بَيْنَ الْعِلْمِ الشَّرْعِيِّ وَالْمَهَارَاتِ الرَّقْمِيَّةِ،
            لِيَكُونَ نَافِعًا لِنَفْسِهِ وَمُجْتَمَعِهِ.
          </p>
          <p>
            كَمَا أَسْخَرُ التِّقْنِيَةَ فِي تَوْسِيعِ نِطَاقِ التَّعْلِيمِ وَالدَّعْوَةِ،
            مِنْ خِلَالِ الْمَوَاقِعِ الْإِلِكْتِرُونِيَّةِ، وَالْمُحْتَوَى الرَّقْمِيِّ،
            وَخِدْمَةِ الْمُجْتَمَعِ.
          </p>
          <div class="skills">
            <span class="skill">📖 الْقُرْآنُ</span>
            <span class="skill">🕌 الدَّعْوَةُ</span>
            <span class="skill">📚 الدِّرَاسَاتُ الْإِسْلَامِيَّةُ</span>
            <span class="skill">💻 هَنْدَسَةُ الْبَرْمَجِيَّاتِ</span>
            <span class="skill">🌐 تَطْوِيرُ الْوَيْبِ</span>
            <span class="skill">🎨 التَّصْمِيمُ الرَّقْمِيُّ</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== MARKAZA ===== -->
  <section id="markaza">
    <div class="container">
      <div class="markaza-box">
        <div class="markaza-icon">🌿✨🕌📖</div>
        <h2>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</h2>
        <div class="arabic markaza-arabic">
          مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ<br>لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
        </div>
        <p>
          <strong>“مَنَارَةٌ لِتَعَلُّمِ الْعُلُومِ الشَّرْعِيَّةِ وَالْقُرْآنِ الْكَرِيمِ”</strong>
          <br><br>
          نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ، وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ.
        </p>
      </div>
    </div>
  </section>

  <!-- ===== PROGRAMS ===== -->
  <section id="programs">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">الْبَرَامِجُ التَّعْلِيمِيَّةُ</div>
        <h2>📚 بَرَامِجُنَا</h2>
        <p>بَرَامِجُ مُنَظَّمَةٌ لِبِنَاءِ الْمُسْلِمِ عِلْمِيًّا وَأَخْلَاقِيًّا</p>
      </div>
      <div class="program-grid">
        <div class="program">
          <div class="program-icon">🔤</div>
          <h3>الْقَاعِدَةُ النُّورَانِيَّةُ</h3>
          <p>اَلْمُسْتَوَى التَّمْهِيدِيُّ لِتَعْلِيمِ الْقِرَاءَةِ الصَّحِيحَةِ لِلْحُرُوفِ وَالْكَلِمَاتِ، مُخَصَّصٌ لِلصِّغَارِ وَالْمُبْتَدِئِينَ.</p>
          <span class="duration">🌱 لِلْمُبْتَدِئِينَ</span>
        </div>
        <div class="program">
          <div class="program-icon">📖</div>
          <h3>التِّلَاوَةُ وَالتَّجْوِيدُ</h3>
          <p>تَعَلُّمُ مَخَارِجِ الْحُرُوفِ، وَالصِّفَاتِ، وَأَحْكَامِ التَّجْوِيدِ (النُّونِ السَّاكِنَةِ، الْمُدُودِ، وَغَيْرِهَا).</p>
          <span class="duration">⏳ 3 أَشْهُرٍ</span>
        </div>
        <div class="program">
          <div class="program-icon">🌙</div>
          <h3>السِّيرَةُ النَّبَوِيَّةُ</h3>
          <p>دِرَاسَةُ حَيَاةِ النَّبِيِّ ﷺ، وَأَخْلَاقِهِ، وَغَزَوَاتِهِ، وَمَوَاقِفِهِ التَّرْبَوِيَّةِ.</p>
          <span class="duration">⏳ شَهْرَانِ</span>
        </div>
        <div class="program">
          <div class="program-icon">🕌</div>
          <h3>الْفِقْهُ وَالْأَحْكَامُ</h3>
          <p>أَحْكَامُ الطَّهَارَةِ، وَالصَّلَاةِ، وَالزَّكَاةِ، وَالصِّيَامِ، وَالْحَجِّ، وَالْمُعَامِلَاتِ.</p>
          <span class="duration">⏳ 3 أَشْهُرٍ</span>
        </div>
        <div class="program">
          <div class="program-icon">☝️</div>
          <h3>الْعَقِيدَةُ الصَّحِيحَةُ</h3>
          <p>دِرَاسَةُ التَّوْحِيدِ، وَأُصُولِ الْإِيمَانِ، وَأَسْمَاءِ اللَّهِ وَصِفَاتِهِ، وَمَا يُضَادُّ ذَلِكَ مِنَ الشِّرْكِ.</p>
          <span class="duration">⏳ شَهْرَانِ</span>
        </div>
        <div class="program">
          <div class="program-icon">✨</div>
          <h3>الْبَرْنَامَجُ الشَّامِلُ</h3>
          <p>مَنْهَجٌ مُتَكَامِلٌ يَضُمُّ الْقُرْآنَ، وَالتَّجْوِيدَ، وَالْعَقِيدَةَ، وَالْفِقْهَ، وَالسِّيرَةَ فِي فَتْرَةٍ زَمَنِيَّةٍ مُحَدَّدَةٍ.</p>
          <span class="duration">⏳ 3 أَشْهُرٍ</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== CURRICULUM ===== -->
  <section class="curriculum" id="curriculum">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">الْمَنْهَجُ</div>
        <h2>📚 الْكُتُبُ وَالْمُقَرَّرَاتُ</h2>
        <p>اَلْكُتُبُ وَالْمَوَادُّ التَّعْلِيمِيَّةُ الْمُعْتَمَدَةُ</p>
      </div>
      <div class="book-grid">
        <div class="book">
          <div class="book-icon">🔤</div>
          <div>
            <h3>الْقَاعِدَةُ النُّورَانِيَّةُ</h3>
            <p>أَسَاسُ قِرَاءَةِ الْقُرْآنِ وَاللُّغَةِ الْعَرَبِيَّةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">📖</div>
          <div>
            <h3>التِّلَاوَةُ وَالتَّجْوِيدُ</h3>
            <p>مَخَارِجُ الْحُرُوفِ، الصِّفَاتُ، وَأَحْكَامُ التَّجْوِيدِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">☝️</div>
          <div>
            <h3>اَلْأُصُولُ الثَّلَاثَةُ</h3>
            <p>أُصُولُ الْعَقِيدَةِ وَالتَّوْحِيدِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">🕌</div>
          <div>
            <h3>كِتَابُ التَّوْحِيدِ وَالْعَقِيدَةُ الْوَاسِطِيَّةُ</h3>
            <p>شُرُوحٌ مُيَسَّرَةٌ لِلْعَقِيدَةِ الصَّحِيحَةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">📕</div>
          <div>
            <h3>خُذْ عَقِيدَتَكَ</h3>
            <p>مُقَدِّمَةٌ مُبَسَّطَةٌ لِلْعَقِيدَةِ الْإِسْلَامِيَّةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">📚</div>
          <div>
            <h3>اَلْأَرْبَعُونَ النَّوَوِيَّةُ وَبُلُوغُ الْمَرَامِ</h3>
            <p>مَجْمُوعَاتٌ حَدِيثِيَّةٌ مَعَ شُرُوحٍ مُخْتَصَرَةٍ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">⚖️</div>
          <div>
            <h3>اَلْأَحْكَامُ الْفِقْهِيَّةُ</h3>
            <p>أَحْكَامُ الْعِبَادَاتِ وَالْمُعَامَلَاتِ الْيَوْمِيَّةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">🌙</div>
          <div>
            <h3>السِّيرَةُ النَّبَوِيَّةُ</h3>
            <p>دُرُوسٌ وَعِبَرٌ مِنْ حَيَاةِ النَّبِيِّ ﷺ.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== MESSAGE ===== -->
  <section>
    <div class="container">
      <div class="section-head">
        <div class="section-mini">رِسَالَتُنَا</div>
        <h2>🌿 رِسَالَتُنَا</h2>
      </div>
      <div class="message-box">
        <div class="arabic">
          نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،<br>
          وَنُعَرِّفُكَ بِنَبِيِّكَ ﷺ،<br>
          وَنُفَهِّمُكَ دِينَكَ،<br>
          وَنُصَحِّحُ لَكَ عَقِيدَتَكَ.
        </div>
        <p>
          لِتَكُونَ قَارِئًا مُتْقِنًا لِلْقُرْآنِ، مُسْلِمًا صَحِيحَ الْعَقِيدَةِ،
          فَهِمًا لِدِينِكَ، مُتَّبِعًا لِنَبِيِّكَ ﷺ.
        </p>
      </div>
    </div>
  </section>

  <!-- ===== CONTACT ===== -->
  <section id="contact">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">اِتَّصِلْ بِنَا</div>
        <h2>📞 اِتَّصِلْ بِنَا</h2>
        <p>لِلِاسْتِفْسَارِ عَنِ الدَّعْوَةِ، أَوِ التَّعْلِيمِ، أَوِ التَّعَاوُنِ التِّقْنِيِّ</p>
      </div>
      <div class="contact-grid">
        <a href="tel:0915455051" class="contact-card">
          <div class="contact-icon">📞</div>
          <h3>اَلْهَاتِفُ</h3>
          <p>0915455051</p>
        </a>
        <a href="https://wa.me/251915455051" target="_blank" class="contact-card">
          <div class="contact-icon">💬</div>
          <h3>وَاتْسَابْ</h3>
          <p>0915455051</p>
        </a>
        <a href="mailto:Ferhanshaamil@gmail.com" class="contact-card">
          <div class="contact-icon">📧</div>
          <h3>اَلْبَرِيدُ الْإِلِكْتِرُونِيُّ</h3>
          <p>Ferhanshaamil@gmail.com</p>
        </a>
      </div>
    </div>
  </section>

  <!-- ===== CTA ===== -->
  <section class="cta">
    <div class="container">
      <div class="arabic">خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ</div>
      <h2>اَلْقُرْآنُ يَنْتَظِرُكَ! 📖</h2>
      <p>
        اَلْمَكَانُ هُنَا. 🕌<br>
        اَلْفُرْصَةُ الْآنَ. ⏰<br>
        الرِّحْلَةُ تَبْدَأُ الْيَوْمَ. 🚀
      </p>
      <a href="#contact" class="btn btn-primary">📝 تَوَاصَلْ مَعَنَا</a>
    </div>
  </section>

  <!-- ===== FOOTER ===== -->
  <footer>
    <div class="container">
      <div class="footer-logo">🌿✨🕌📖</div>
      <p><strong>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</strong></p>
      <p>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</p>
      <p>مُدَرِّسُ الْمَرْكَزِ: فَرْحَانُ شَامِلٌ</p>
      <p>© 2026 مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ. جَمِيعُ الْحُقُوقِ مَحْفُوظَةٌ.</p>
    </div>
  </footer>

  <!-- ===== FLOATING WHATSAPP ===== -->
  <a href="https://wa.me/251915455051" target="_blank" class="floating" title="WhatsApp">💬</a>

</body>
</html><!DOCTYPE html>
<html lang="om" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ferhan Shaamil | Markaza Uweysii Ibnu Aamir</title>
  <meta name="description" content="Ferhan Shaamil AbdulGafur - Da'ii, Barsiisaa Qur'aanaa fi Beekumsa Shari'aa, Software Engineering Student">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --bg: #040d09;
      --bg2: #0a1f15;
      --card: rgba(11, 44, 30, 0.75);
      --gold: #d6b45d;
      --gold-light: #f2d98d;
      --white: #f7f5ed;
      --text: #d1ddd6;
      --muted: #98aea4;
      --border: rgba(214, 180, 93, 0.25);
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: radial-gradient(circle at 10% 20%, rgba(214, 180, 93, 0.08), transparent 30%),
                  radial-gradient(circle at 90% 70%, rgba(13, 158, 110, 0.10), transparent 35%),
                  var(--bg);
      color: var(--white);
      line-height: 1.9;
      min-height: 100vh;
    }

    .container {
      width: min(1180px, 92%);
      margin: 0 auto;
    }

    /* ===== NAVBAR ===== */
    nav {
      position: fixed;
      top: 0;
      right: 0;
      left: 0;
      z-index: 999;
      background: rgba(4, 13, 9, 0.92);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid var(--border);
      padding: 0 5%;
    }

    .nav-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      min-height: 75px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-icon {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      border: 1px solid var(--gold);
      display: grid;
      place-items: center;
      font-size: 22px;
      color: var(--gold-light);
    }

    .logo-text strong {
      display: block;
      color: var(--gold-light);
      font-size: 15px;
      letter-spacing: 0.5px;
    }

    .logo-text small {
      display: block;
      color: var(--muted);
      font-size: 9px;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      list-style: none;
      font-size: 14px;
    }

    .nav-links a {
      color: var(--text);
      transition: 0.3s;
      font-weight: 600;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 150px 0 80px;
      position: relative;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 50px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      border: 1px solid var(--border);
      background: rgba(214, 180, 93, 0.08);
      padding: 8px 18px;
      border-radius: 40px;
      color: var(--gold-light);
      font-size: 13px;
      margin-bottom: 20px;
      font-weight: 700;
    }

    .hero h1 {
      font-size: clamp(38px, 6vw, 70px);
      line-height: 1.1;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .hero h1 span {
      color: var(--gold-light);
    }

    .hero-sub {
      font-size: clamp(20px, 3vw, 30px);
      color: var(--gold);
      margin: 15px 0 10px;
      font-weight: 700;
    }

    .hero-desc {
      color: var(--muted);
      font-size: 16px;
      max-width: 650px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 30px;
    }

    .btn {
      padding: 13px 28px;
      border-radius: 35px;
      font-weight: 700;
      font-size: 14px;
      transition: 0.3s;
      display: inline-block;
      border: 1px solid var(--gold);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold-light), var(--gold));
      color: #07130d;
      border: none;
    }

    .btn-primary:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 30px rgba(214, 180, 93, 0.3);
    }

    .btn-outline {
      background: transparent;
      color: var(--white);
    }
    .btn-outline:hover {
      background: rgba(214, 180, 93, 0.1);
      border-color: var(--gold-light);
    }

    .hero-card {
      border: 1px solid var(--border);
      background: var(--card);
      backdrop-filter: blur(10px);
      border-radius: 35px;
      padding: 35px 25px;
      text-align: center;
      box-shadow: 0 30px 70px rgba(0, 0, 0, 0.4);
    }

    .hero-symbol {
      width: 130px;
      height: 130px;
      margin: 0 auto 20px;
      border-radius: 50%;
      border: 1px solid var(--gold);
      display: grid;
      place-items: center;
      font-size: 60px;
      background: radial-gradient(circle, rgba(214, 180, 93, 0.15), transparent 65%);
    }

    .hero-card h3 {
      color: var(--gold-light);
      font-size: 22px;
      margin-bottom: 5px;
    }

    .hero-card p {
      color: var(--muted);
      font-size: 13px;
    }

    /* ===== SECTIONS ===== */
    section {
      padding: 100px 0;
    }

    .section-head {
      text-align: center;
      max-width: 800px;
      margin: 0 auto 55px;
    }

    .section-mini {
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 4px;
      font-size: 12px;
      font-weight: 700;
    }

    .section-head h2 {
      font-size: clamp(30px, 5vw, 48px);
      margin: 10px 0;
    }

    .section-head p {
      color: var(--muted);
      font-size: 15px;
    }

    /* ===== ABOUT ===== */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
    }

    .card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 32px 28px;
      backdrop-filter: blur(6px);
      transition: 0.4s;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
    }

    .card h3 {
      color: var(--gold-light);
      font-size: 22px;
      margin-bottom: 15px;
    }

    .card p {
      color: var(--muted);
      font-size: 14px;
      margin-bottom: 12px;
    }

    .card .highlight {
      color: var(--gold-light);
      font-weight: 700;
    }

    /* ===== WORK / SERVICES ===== */
    .work-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .work-item {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 28px 20px;
      text-align: center;
      transition: 0.4s;
    }

    .work-item:hover {
      transform: translateY(-7px);
      border-color: var(--gold);
    }

    .work-item .icon {
      font-size: 40px;
      margin-bottom: 12px;
    }

    .work-item h4 {
      color: var(--gold-light);
      font-size: 18px;
      margin-bottom: 8px;
    }

    .work-item p {
      color: var(--muted);
      font-size: 13px;
    }

    /* ===== VISION ===== */
    .vision-box {
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 50px 30px;
      background: radial-gradient(circle at center, rgba(13, 158, 110, 0.12), transparent 60%), rgba(8, 25, 18, 0.8);
      text-align: center;
    }

    .vision-box h3 {
      color: var(--gold-light);
      font-size: 28px;
      margin-bottom: 15px;
    }

    .vision-box p {
      color: var(--muted);
      max-width: 800px;
      margin: 0 auto;
      font-size: 16px;
    }

    /* ===== MESSAGE / QUOTE ===== */
    .message-box {
      border: 1px solid var(--border);
      border-radius: 28px;
      padding: 45px 30px;
      background: var(--card);
      text-align: center;
    }

    .message-box blockquote {
      font-size: clamp(24px, 4vw, 38px);
      color: var(--gold-light);
      font-weight: 700;
      line-height: 1.6;
      margin-bottom: 20px;
    }

    .message-box p {
      color: var(--muted);
      font-size: 16px;
      max-width: 750px;
      margin: 0 auto;
    }

    /* ===== SOCIAL MEDIA ===== */
    .social-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      max-width: 900px;
      margin: 0 auto;
    }

    .social-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 28px 20px;
      text-align: center;
      transition: 0.4s;
    }

    .social-card:hover {
      transform: translateY(-6px);
      border-color: var(--gold);
    }

    .social-card .s-icon {
      font-size: 36px;
      margin-bottom: 10px;
    }

    .social-card h4 {
      color: var(--gold-light);
      font-size: 17px;
      margin-bottom: 5px;
    }

    .social-card a {
      display: inline-block;
      color: var(--muted);
      font-size: 13px;
      word-break: break-word;
      transition: 0.3s;
    }

    .social-card a:hover {
      color: var(--white);
    }

    /* ===== CTA ===== */
    .cta {
      text-align: center;
      padding: 90px 20px;
      background: radial-gradient(circle, rgba(214, 180, 93, 0.08), transparent 55%);
    }

    .cta h2 {
      font-size: clamp(32px, 5vw, 52px);
      color: var(--gold-light);
      margin: 15px 0;
    }

    .cta p {
      color: var(--muted);
      max-width: 600px;
      margin: 0 auto 25px;
      font-size: 16px;
    }

    /* ===== FOOTER ===== */
    footer {
      border-top: 1px solid var(--border);
      background: #020906;
      padding: 45px 0;
      text-align: center;
    }

    footer strong {
      color: var(--gold-light);
    }

    footer p {
      color: var(--muted);
      font-size: 13px;
      margin: 4px 0;
    }

    .footer-socials {
      margin-top: 15px;
      display: flex;
      justify-content: center;
      gap: 18px;
      flex-wrap: wrap;
    }

    .footer-socials a {
      color: var(--muted);
      font-size: 24px;
      transition: 0.3s;
    }

    .footer-socials a:hover {
      color: var(--gold-light);
      transform: scale(1.1);
    }

    /* ===== WHATSAPP ===== */
    .wa {
      position: fixed;
      bottom: 20px;
      left: 20px;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      background: #25d366;
      display: grid;
      place-items: center;
      font-size: 28px;
      z-index: 500;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 900px) {
      .nav-links {
        display: none;
      }
      .hero-grid {
        grid-template-columns: 1fr;
        text-align: center;
      }
      .hero-desc {
        margin: 0 auto;
      }
      .hero-buttons {
        justify-content: center;
      }
      .about-grid {
        grid-template-columns: 1fr;
      }
      .work-grid {
        grid-template-columns: 1fr 1fr;
      }
      .social-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 550px) {
      .work-grid,
      .social-grid {
        grid-template-columns: 1fr;
      }
      .hero {
        padding-top: 120px;
      }
      section {
        padding: 70px 0;
      }
      .vision-box {
        padding: 35px 20px;
      }
      .message-box {
        padding: 30px 18px;
      }
    }
  </style>
</head>

<body>

  <!-- ===== NAVBAR ===== -->
  <nav>
    <div class="container nav-inner">
      <a href="#home" class="logo">
        <div class="logo-icon">🌿</div>
        <div class="logo-text">
          <strong>FERHAN SHAAMIL</strong>
          <small>Markaza Uweysii Ibnu Aamir</small>
        </div>
      </a>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#work">Work</a></li>
        <li><a href="#vision">Vision</a></li>
        <li><a href="#social">Social</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
  </nav>

  <!-- ===== HERO ===== -->
  <section class="hero" id="home">
    <div class="container hero-grid">
      <div>
        <div class="badge">🌿✨ OFFICIAL WEBSITE</div>
        <h1>FERHAN<br><span>SHAAMIL</span></h1>
        <div class="hero-sub">Da'ii • Barsiisaa Qur'aanaa Fi Beekumsa Shari'aa • Barataa Software Engineering</div>
        <p class="hero-desc">
          Ani Ferhan Shaamil AbdulGafur, Barsiisaa Markaza Uweysii Ibnu Aamir, Da'ii Fi Nama Dhaloota Qur'aanaa, Beekumsa Shari'aa Fi Akkaataa Jireenyaa Gaarii Irratti Kakaasuudha.
        </p>
        <p class="hero-desc" style="margin-top:10px;">
          Kaayyoon Koo Beekumsa Qofa Dabarsuu Osoo Hin Taane, Beekumsa Sana Jireenya Keessatti Hojiiirra Oolchuuf Dhaloota Qopheessuudha.
        </p>
        <p class="hero-desc" style="margin-top:10px;">
          Qur'aana Jaalachuu, Diinii Hubachuu, Akhlaaqa Gaarii Horachuu Fi Teknooloojii Sirriitti Fayyadamuun Dhaloota Boruu Ijaaruuf Nan Hojjedha.
        </p>
        <div class="hero-buttons">
          <a href="#about" class="btn btn-primary">👤 Waa'ee Kiyya</a>
          <a href="#social" class="btn btn-outline">📱 Nu Hordofaa</a>
        </div>
      </div>
      <div class="hero-card">
        <div class="hero-symbol">🌿</div>
        <h3>Ferhan Shaamil</h3>
        <p>Da'ii • Barsiisaa • Software Engineering Student</p>
        <p style="margin-top:15px;">📖 Qur'aana<br>🕌 Da'waa<br>💻 Technology</p>
      </div>
    </div>
  </section>

  <!-- ===== ABOUT ===== -->
  <section id="about">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">About Me</div>
        <h2>🌿 Waa'ee Kiyya</h2>
        <p>Ferhan Shaamil AbdulGafur — Da'ii, Barsiisaa Qur'aanaa Fi Beekumsa Shari'aa, Akkasumas Barataa Software Engineering Ti.</p>
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
        </div>
      </div>
    </div>
  </section>

  <!-- ===== WORK / SERVICES ===== -->
  <section id="work" style="background: rgba(7, 22, 15, 0.4);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">What I Do</div>
        <h2>💡 Waan Ani Irratti Hojjedhu</h2>
      </div>
      <div class="work-grid">
        <div class="work-item">
          <div class="icon">📖</div>
          <h4>Qur'aana</h4>
          <p>Qur'aana Barachuu, Barsiisuu Fi Jaalala Qur'aanaa Dhaloota Keessatti Cimsuu.</p>
        </div>
        <div class="work-item">
          <div class="icon">🕌</div>
          <h4>Da'waa</h4>
          <p>Nama Gara Kheeyrii, Beekumsaa, Tawhiidaa Fi Hojii Gaarii Waamuu.</p>
        </div>
        <div class="work-item">
          <div class="icon">📚</div>
          <h4>Beekumsa Shari'aa</h4>
          <p>Aqiidaa, Fiqhii, Seenaa Nabiyyii ﷺ Fi Barnoota Islaamaa Babal'isuu.</p>
        </div>
        <div class="work-item">
          <div class="icon">🌱</div>
          <h4>Tarbiyaa Fi Akhlaaqa</h4>
          <p>Dhaloota Akhlaaqa Gaarii, Naamusa, Obsa Fi Itti Gaafatamummaa Qabu Ijaaruu.</p>
        </div>
        <div class="work-item">
          <div class="icon">💻</div>
          <h4>Software Engineering</h4>
          <p>Teknooloojii Hubachuu Fi Furmaata Dijitaalaa Bu'a Qabeessa Uumuu.</p>
        </div>
        <div class="work-item">
          <div class="icon">🌐</div>
          <h4>Web Development</h4>
          <p>Websitewwan Ammayyaa, Saffisaa Fi Fayyadamtootaaf Mijataa Ta'an Ijaaruu.</p>
        </div>
        <div class="work-item">
          <div class="icon">🎨</div>
          <h4>Digital Design</h4>
          <p>Design Dijitaalaa Bareedaa, Qulqulluu Fi Ergaa Qabu Uumuu.</p>
        </div>
        <div class="work-item">
          <div class="icon">🚀</div>
          <h4>Teknooloojii Fi Barnoota Ammayyaa</h4>
          <p>Teknooloojii Akka Meeshaa Barnootaa, Da'waa Fi Tajaajila Hawaasaatti Fayyadamu.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== VISION ===== -->
  <section id="vision">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">My Vision</div>
        <h2>🌟 Mul'ata Kiyya</h2>
      </div>
      <div class="vision-box">
        <p>Dhaloota Qur'aana Jaalatu, Diinii Isaa Hubatu, Akhlaaqa Gaarii Horatu, Beekumsa Barbaadu Fi Teknooloojii Karaa Gaarii Ta'een Fayyadamu Ijaaruu.</p>
      </div>
    </div>
  </section>

  <!-- ===== MESSAGE ===== -->
  <section style="background: rgba(7, 22, 15, 0.3);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">My Message</div>
        <h2>✨ Ergaa Kiyya</h2>
      </div>
      <div class="message-box">
        <blockquote>"Beekumsa Baradhu, Dhaloota Ijaari, Jireenya Kee Ifa Godhi."</blockquote>
        <p>Jireenyi Nama Tokkoo Yeroo Inni Ofii Isaatiif Qofa Jiraatu Caalaa, Yeroo Inni Nama Biraa Fayyadu Hiika Guddaa Qaba.</p>
      </div>
    </div>
  </section>

  <!-- ===== SOCIAL MEDIA ===== -->
  <section id="social" style="background: rgba(7, 22, 15, 0.5);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">Follow Me</div>
        <h2>📱 Nu Hordofaa</h2>
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
          <div class="s-icon">🐙</div>
          <h4>GitHub</h4>
          <a href="https://github.com/HamzaAbdulhakim" target="_blank">github.com/HamzaAbdulhakim</a>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== CONTACT / CTA ===== -->
  <section class="cta" id="contact">
    <div class="container">
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
      <p><strong>FERHAN SHAAMIL ABDULGAFUR</strong></p>
      <p>🕌 Da'ii • 📖 Barsiisaa Qur'aanaa fi Beekumsa Shari'aa • 💻 Software Engineering Student</p>
      <div class="footer-socials">
        <a href="https://www.facebook.com/share/1D9P96HFwe/" target="_blank" title="Facebook">📘</a>
        <a href="https://www.tiktok.com/@mirkanihararge" target="_blank" title="TikTok">🎵</a>
        <a href="https://youtube.com/@ferhanshaamil" target="_blank" title="YouTube">▶️</a>
        <a href="https://t.me/Ferhan_Shaamil" target="_blank" title="Telegram">✈️</a>
        <a href="https://wa.me/251915455051" target="_blank" title="WhatsApp">💬</a>
        <a href="https://github.com/HamzaAbdulhakim" target="_blank" title="GitHub">🐙</a>
        <a href="mailto:Ferhanshaamil@gmail.com" title="Email">📧</a>
      </div>
      <p style="margin-top:15px;">© 2026 Ferhan Shaamil AbdulGafur. All Rights Reserved.</p>
    </div>
  </footer>

  <!-- ===== WHATSAPP FLOATING ===== -->
  <a href="https://wa.me/251915455051" target="_blank" class="wa" title="WhatsApp">💬</a>

</body>
</html><!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ - لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</title>
  <meta name="description" content="مركز أويس بن عامر - منارة العلوم الشرعية والقرآن الكريم، مزود بتقنيات التعليم الرقمي والذكاء الاصطناعي.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;600;700;800;900&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --bg: #040d09;
      --bg2: #0a1f15;
      --card: rgba(11, 44, 30, 0.75);
      --gold: #d6b45d;
      --gold-light: #f2d98d;
      --green: #0d9e6e;
      --white: #f7f5ed;
      --text: #d1ddd6;
      --muted: #98aea4;
      --border: rgba(214, 180, 93, 0.25);
    }

    body {
      font-family: 'Cairo', 'Amiri', sans-serif;
      background: radial-gradient(circle at 10% 20%, rgba(214, 180, 93, 0.08), transparent 30%),
        radial-gradient(circle at 90% 70%, rgba(13, 158, 110, 0.15), transparent 35%),
        var(--bg);
      color: var(--white);
      line-height: 1.9;
      min-height: 100vh;
    }

    .container {
      width: min(1180px, 92%);
      margin: 0 auto;
    }

    /* ===== NAVBAR ===== */
    nav {
      position: fixed;
      top: 0;
      right: 0;
      left: 0;
      z-index: 999;
      background: rgba(4, 13, 9, 0.92);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid var(--border);
      padding: 0 5%;
    }

    .nav-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      min-height: 75px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-icon {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      border: 1px solid var(--gold);
      display: grid;
      place-items: center;
      font-size: 22px;
      color: var(--gold-light);
    }

    .logo-text strong {
      display: block;
      color: var(--gold-light);
      font-size: 15px;
      letter-spacing: 0.5px;
    }

    .logo-text small {
      display: block;
      color: var(--muted);
      font-size: 9px;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      list-style: none;
      font-size: 14px;
    }

    .nav-links a {
      color: var(--text);
      transition: 0.3s;
      font-weight: 600;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .nav-cta {
      border: 1px solid var(--gold);
      padding: 8px 18px;
      border-radius: 30px;
      color: var(--gold-light) !important;
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 150px 0 80px;
      position: relative;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 50px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      border: 1px solid var(--border);
      background: rgba(214, 180, 93, 0.08);
      padding: 8px 18px;
      border-radius: 40px;
      color: var(--gold-light);
      font-size: 13px;
      margin-bottom: 20px;
      font-weight: 700;
    }

    .hero h1 {
      font-size: clamp(38px, 6vw, 70px);
      line-height: 1.1;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .hero h1 span {
      color: var(--gold-light);
    }

    .hero-sub {
      font-size: clamp(20px, 3vw, 30px);
      color: var(--gold);
      margin: 15px 0 10px;
      font-weight: 700;
    }

    .hero-motto {
      font-family: 'Amiri', serif;
      font-size: clamp(22px, 3.5vw, 38px);
      color: #f5eace;
      margin: 15px 0 20px;
      line-height: 1.7;
      border-right: 4px solid var(--gold);
      padding-right: 20px;
    }

    .hero-desc {
      color: var(--muted);
      font-size: 16px;
      max-width: 650px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 30px;
    }

    .btn {
      padding: 13px 28px;
      border-radius: 35px;
      font-weight: 700;
      font-size: 14px;
      transition: 0.3s;
      display: inline-block;
      border: 1px solid var(--gold);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold-light), var(--gold));
      color: #07130d;
      border: none;
    }

    .btn-primary:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 30px rgba(214, 180, 93, 0.3);
    }

    .btn-outline {
      background: transparent;
      color: var(--white);
    }
    .btn-outline:hover {
      background: rgba(214, 180, 93, 0.1);
      border-color: var(--gold-light);
    }

    .hero-card {
      border: 1px solid var(--border);
      background: var(--card);
      backdrop-filter: blur(10px);
      border-radius: 35px;
      padding: 35px 25px;
      text-align: center;
      box-shadow: 0 30px 70px rgba(0, 0, 0, 0.4);
    }

    .hero-symbol {
      width: 130px;
      height: 130px;
      margin: 0 auto 20px;
      border-radius: 50%;
      border: 1px solid var(--gold);
      display: grid;
      place-items: center;
      font-size: 60px;
      background: radial-gradient(circle, rgba(214, 180, 93, 0.15), transparent 65%);
    }

    .hero-card h3 {
      color: var(--gold-light);
      font-size: 22px;
      margin-bottom: 5px;
    }

    .hero-card p {
      color: var(--muted);
      font-size: 13px;
    }
    .hero-card .arabic-tag {
      font-family: 'Amiri', serif;
      font-size: 18px;
      color: #eee4c8;
      margin-top: 12px;
    }

    /* ===== SECTIONS ===== */
    section {
      padding: 100px 0;
    }

    .section-head {
      text-align: center;
      max-width: 800px;
      margin: 0 auto 55px;
    }

    .section-mini {
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 4px;
      font-size: 12px;
      font-weight: 700;
    }

    .section-head h2 {
      font-size: clamp(30px, 5vw, 48px);
      margin: 10px 0;
    }

    .section-head .arabic-sub {
      font-family: 'Amiri', serif;
      color: var(--gold-light);
      font-size: 22px;
      margin-top: 5px;
    }

    .section-head p {
      color: var(--muted);
      font-size: 15px;
    }

    /* ===== FEATURES GRID ===== */
    .features-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .feature {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 32px 25px;
      text-align: center;
      transition: 0.4s;
      backdrop-filter: blur(6px);
    }

    .feature:hover {
      transform: translateY(-10px);
      border-color: var(--gold);
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
    }

    .feature .icon {
      font-size: 45px;
      margin-bottom: 15px;
    }

    .feature h3 {
      color: var(--gold-light);
      font-size: 19px;
      margin-bottom: 10px;
    }

    .feature p {
      color: var(--muted);
      font-size: 13px;
    }

    .feature .ar-desc {
      font-family: 'Amiri', serif;
      font-size: 14px;
      color: #c7d4cd;
      margin-top: 8px;
    }

    /* ===== MISSION / VISION ===== */
    .mission-box {
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 60px 30px;
      background: radial-gradient(circle at center, rgba(13, 158, 110, 0.15), transparent 60%), rgba(8, 25, 18, 0.8);
      text-align: center;
    }

    .mission-box .big-arabic {
      font-family: 'Amiri', serif;
      font-size: clamp(28px, 4vw, 45px);
      color: var(--gold-light);
      line-height: 2;
    }

    .mission-box p {
      color: var(--muted);
      max-width: 800px;
      margin: 20px auto 0;
      font-size: 16px;
    }

    /* ===== MODERN TOOLS ===== */
    .tools-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .tool {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 25px 15px;
      text-align: center;
    }

    .tool .icon {
      font-size: 32px;
    }

    .tool h4 {
      color: var(--gold-light);
      font-size: 15px;
      margin-top: 8px;
    }

    .tool span {
      display: block;
      color: var(--muted);
      font-size: 11px;
    }

    /* ===== CURRICULUM ===== */
    .curr-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
    }

    .curr-item {
      display: flex;
      gap: 18px;
      align-items: center;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 20px;
    }

    .curr-item .lvl {
      font-size: 28px;
    }

    .curr-item h4 {
      color: var(--gold-light);
      font-size: 16px;
    }

    .curr-item p {
      color: var(--muted);
      font-size: 12px;
    }

    /* ===== SOCIAL MEDIA GRID (NEW) ===== */
    .social-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      max-width: 900px;
      margin: 0 auto;
    }

    .social-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 30px 20px;
      text-align: center;
      transition: 0.4s;
      backdrop-filter: blur(6px);
    }

    .social-card:hover {
      transform: translateY(-8px);
      border-color: var(--gold);
      box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
    }

    .social-card .s-icon {
      font-size: 40px;
      margin-bottom: 12px;
    }

    .social-card h4 {
      color: var(--gold-light);
      font-size: 18px;
      margin-bottom: 5px;
    }

    .social-card a {
      display: inline-block;
      color: var(--muted);
      font-size: 13px;
      word-break: break-word;
      transition: 0.3s;
      border-bottom: 1px solid transparent;
    }

    .social-card a:hover {
      color: var(--white);
      border-bottom-color: var(--gold);
    }

    /* ===== CTA ===== */
    .cta {
      text-align: center;
      padding: 100px 20px;
      background: radial-gradient(circle, rgba(214, 180, 93, 0.1), transparent 55%);
    }

    .cta .arabic {
      font-family: 'Amiri', serif;
      font-size: 35px;
      color: var(--gold-light);
    }

    .cta h2 {
      font-size: clamp(32px, 5vw, 52px);
      color: var(--white);
      margin: 15px 0;
    }

    .cta p {
      color: var(--muted);
      max-width: 600px;
      margin: 0 auto 30px;
    }

    /* ===== FOOTER ===== */
    footer {
      border-top: 1px solid var(--border);
      background: #020906;
      padding: 45px 0;
      text-align: center;
    }

    footer strong {
      color: var(--gold-light);
    }

    footer .ar {
      font-family: 'Amiri', serif;
      color: #d4cbaa;
      font-size: 20px;
      margin: 5px 0;
    }

    footer p {
      color: var(--muted);
      font-size: 12px;
    }
    
    footer .footer-socials {
      margin-top: 15px;
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }
    
    footer .footer-socials a {
      color: var(--muted);
      font-size: 22px;
      transition: 0.3s;
    }
    footer .footer-socials a:hover {
      color: var(--gold-light);
      transform: scale(1.1);
    }

    /* ===== WHATSAPP ===== */
    .wa {
      position: fixed;
      bottom: 20px;
      left: 20px;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      background: #25d366;
      display: grid;
      place-items: center;
      font-size: 28px;
      z-index: 500;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 900px) {
      .nav-links {
        display: none;
      }
      .hero-grid {
        grid-template-columns: 1fr;
        text-align: center;
      }
      .hero-motto {
        border-right: none;
        padding-right: 0;
        text-align: center;
      }
      .hero-desc {
        margin: 0 auto;
      }
      .hero-buttons {
        justify-content: center;
      }
      .features-grid {
        grid-template-columns: 1fr 1fr;
      }
      .tools-grid {
        grid-template-columns: 1fr 1fr;
      }
      .curr-grid {
        grid-template-columns: 1fr;
      }
      .social-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 550px) {
      .features-grid,
      .tools-grid,
      .social-grid {
        grid-template-columns: 1fr;
      }
      .hero {
        padding-top: 120px;
      }
      section {
        padding: 70px 0;
      }
      .mission-box {
        padding: 40px 20px;
      }
    }
  </style>
</head>

<body>

  <!-- ===== NAVBAR ===== -->
  <nav>
    <div class="container nav-inner">
      <a href="#home" class="logo">
        <div class="logo-icon">🌿</div>
        <div class="logo-text">
          <strong>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</strong>
          <small>لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</small>
        </div>
      </a>
      <ul class="nav-links">
        <li><a href="#home">الرئيسية</a></li>
        <li><a href="#vision">الرؤية</a></li>
        <li><a href="#tools">التقنيات</a></li>
        <li><a href="#curriculum">المنهج</a></li>
        <li><a href="#social">التواصل</a></li>
        <li><a href="#contact" class="nav-cta">اتصل بنا</a></li>
      </ul>
    </div>
  </nav>

  <!-- ===== HERO ===== -->
  <section class="hero" id="home">
    <div class="container hero-grid">
      <div>
        <div class="badge">🌿✨ الْمَوْقِعُ الرَّسْمِيُّ الْجَدِيدُ</div>
        <h1>مَرْكَزُ <span>أُوَيْسِ بْنِ عَامِرٍ</span></h1>
        <div class="hero-sub">لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</div>
        <div class="hero-motto">
          مِنَ الْكِتَابِ إِلَى التِّقْنِيَةِ،<br>
          وَمِنَ التَّعَلُّمِ إِلَى التَّمَيُّزِ.
        </div>
        <p class="hero-desc">
          مَرْكَزٌ عِلْمِيٌّ رَائِدٌ يَجْمَعُ بَيْنَ أَصَالَةِ الْعُلُومِ الشَّرْعِيَّةِ وَرُوحِ الْعَصْرِ،
          مُسَخِّرًا الذَّكَاءَ الاصْطِنَاعِيَّ وَالتَّعْلِيمَ الرَّقْمِيَّ لِبِنَاءِ جِيلٍ قُرْآنِيٍّ مُتْقَنٍ.
        </p>
        <div class="hero-buttons">
          <a href="#vision" class="btn btn-primary">اِكْتَشِفِ الرُّؤْيَةَ</a>
          <a href="#social" class="btn btn-outline">تَابِعْنَا عَلَى الْمَوَاقِعِ</a>
        </div>
      </div>
      <div class="hero-card">
        <div class="hero-symbol">🕌</div>
        <h3>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</h3>
        <p class="arabic-tag">مَنَارَةُ الْعِلْمِ الشَّرْعِيِّ</p>
        <p style="margin-top:15px;">
          📖 الْقُرْآنُ • 🕌 الْفِقْهُ • ☝️ الْعَقِيدَةُ<br>
          🌙 السِّيرَةُ • 💻 الذَّكَاءُ الْاصْطِنَاعِيُّ
        </p>
      </div>
    </div>
  </section>

  <!-- ===== VISION / MISSION ===== -->
  <section id="vision">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">رُؤْيَتُنَا</div>
        <h2>نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ</h2>
        <div class="arabic-sub">وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ</div>
      </div>
      <div class="mission-box">
        <div class="big-arabic">
          نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،<br>
          وَنُعَرِّفُكَ بِنَبِيِّكَ ﷺ،<br>
          وَنُفَهِّمُكَ دِينَكَ،<br>
          وَنُصَحِّحُ لَكَ عَقِيدَتَكَ.
        </div>
        <p>
          نَطْمَحُ إِلَى أَنْ نَكُونَ صَرْحًا تَعْلِيمِيًّا عَصْرِيًّا يُوَازِنُ بَيْنَ الْعُلُومِ الشَّرْعِيَّةِ وَالتِّقْنِيَةِ،
          لِنُخَرِّجَ جِيلًا يَقْرَأُ الْقُرْآنَ إِتْقَانًا، وَيَفْهَمُ دِينَهُ فَهْمًا، وَيَسْتَخْدِمُ التِّقْنِيَةَ فِي الْخَيْرِ.
        </p>
        <p style="margin-top:15px; font-family:'Amiri',serif; color:var(--gold-light); font-size:20px;">
          "مِنَ الْكِتَابِ إِلَى التِّقْنِيَةِ، وَمِنَ التَّعَلُّمِ إِلَى التَّمَيُّزِ"
        </p>
      </div>
    </div>
  </section>

  <!-- ===== MODERN FEATURES ===== -->
  <section>
    <div class="container">
      <div class="section-head">
        <div class="section-mini">مَا نُقَدِّمُهُ</div>
        <h2>مِيْزَاتُنَا التَّقْنِيَّةُ</h2>
        <p>نَمْزِجُ بَيْنَ الْعِلْمِ الشَّرْعِيِّ وَأَحْدَثِ أَدَوَاتِ الْعَصْرِ الرَّقْمِيَّةِ</p>
      </div>
      <div class="features-grid">

        <div class="feature">
          <div class="icon">📱</div>
          <h3>التَّعْلِيمُ الرَّقْمِيُّ</h3>
          <p>دُرُوسٌ، مَقَاطِعُ فِيدْيُو، وَمُلَخَّصَاتٌ عَبْرَ التِّلِغْرَامِ وَالْوَاتْسَابِ.</p>
          <div class="ar-desc">تَعَلُّمٌ مَرِنٌ فِي أَيِّ وَقْتٍ</div>
        </div>

        <div class="feature">
          <div class="icon">🤖</div>
          <h3>الذَّكَاءُ الْاصْطِنَاعِيُّ</h3>
          <p>تَحْلِيلُ الْأَدَاءِ، تَصْحِيحُ الْأَخْطَاءِ، وَإِنْشَاءُ الِاخْتِبَارَاتِ الذَّكِيَّةِ.</p>
          <div class="ar-desc">تَقْنِيَةٌ لِلتَّفَوُّقِ</div>
        </div>

        <div class="feature">
          <div class="icon">📝</div>
          <h3>الِاخْتِبَارَاتُ الْإِلِكْتِرُونِيَّةُ</h3>
          <p>اِخْتِبَارَاتٌ أُسْبُوعِيَّةٌ، شَهْرِيَّةٌ، وَخِتَامِيَّةٌ بِتَصْحِيحٍ آليٍّ.</p>
          <div class="ar-desc">تَقْيِيمٌ مُسْتَمِرٌّ</div>
        </div>

        <div class="feature">
          <div class="icon">🎓</div>
          <h3>إِدَارَةُ الطُّلَّابِ</h3>
          <p>مُتَابَعَةُ الْحُضُورِ، الدُّرُوسِ، وَتَقَارِيرُ التَّقَدُّمِ الْفَرْدِيَّةِ.</p>
          <div class="ar-desc">نِظَامٌ إِدَارِيٌّ مُتَكَامِلٌ</div>
        </div>

        <div class="feature">
          <div class="icon">📚</div>
          <h3>مَنْهَجٌ مُتَدَرِّجٌ</h3>
          <p>مُبْتَدِئ → مُتَوَسِّط → مُتَقَدِّم → دِبْلُومٌ فِي الْعُلُومِ الشَّرْعِيَّةِ.</p>
          <div class="ar-desc">مَسَارٌ عِلْمِيٌّ وَاضِحٌ</div>
        </div>

        <div class="feature">
          <div class="icon">🏆</div>
          <h3>الشَّهَادَاتُ الْمُعْتَمَدَةُ</h3>
          <p>شَهَادَاتٌ رَقْمِيَّةٌ وَوَرَقِيَّةٌ مُعْتَمَدَةٌ بَعْدَ إِتْمَامِ الْبَرَامِجِ.</p>
          <div class="ar-desc">تَوْثِيقٌ رَسْمِيٌّ لِلْجُهُودِ</div>
        </div>

      </div>
    </div>
  </section>

  <!-- ===== MODERN TOOLS ===== -->
  <section id="tools" style="background: rgba(7, 22, 15, 0.6);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">أَدَوَاتُنَا</div>
        <h2>أَحْدَثُ تَقْنِيَاتِ التَّعْلِيمِ</h2>
        <p>نَسْتَخْدِمُ مَا يَجْعَلُ التَّعَلُّمَ سَهْلًا وَمُمْتِعًا</p>
      </div>
      <div class="tools-grid">
        <div class="tool"><div class="icon">📹</div><h4>الدُّرُوسُ الْفِيدْيُو</h4><span>مَحْتَوَى بَصَرِيٌّ غَنِيٌّ</span></div>
        <div class="tool"><div class="icon">🎙️</div><h4>التِّلَاوَةُ الصَّوْتِيَّةُ</h4><span>تَصْحِيحُ التَّجْوِيدِ</span></div>
        <div class="tool"><div class="icon">📊</div><h4>التَّحْلِيلُ الْآلِيُّ</h4><span>إِحْصَاءُ التَّقَدُّمِ</span></div>
        <div class="tool"><div class="icon">💬</div><h4>التَّفَاعُلُ الْمُبَاشِرُ</h4><span>مَجْمُوعَاتُ الْمُنَاقَشَةِ</span></div>
        <div class="tool"><div class="icon">🖥️</div><h4>الْفَصْلُ الذَّكِيُّ</h4><span>سَبُورَةٌ رَقْمِيَّةٌ</span></div>
        <div class="tool"><div class="icon">🤖</div><h4>مُسَاعِدُ الذَّكَاءِ</h4><span>إِجَابَةُ الْأَسْئِلَةِ</span></div>
        <div class="tool"><div class="icon">📝</div><h4>النَّمَاذِجُ الْإِلِكْتِرُونِيَّةُ</h4><span>جُوجِلُ فُورْمْ</span></div>
        <div class="tool"><div class="icon">🔐</div><h4>سِجِلَّاتٌ آمِنَةٌ</h4><span>حِفْظُ الْبَيَانَاتِ</span></div>
      </div>
    </div>
  </section>

  <!-- ===== CURRICULUM ===== -->
  <section id="curriculum">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">الْمَنْهَجُ الدِّرَاسِيُّ</div>
        <h2>بَرَامِجُنَا الْمُتَمَيِّزَةُ</h2>
        <p>مَسَارٌ عِلْمِيٌّ مُنَظَّمٌ مِنَ الْقَاعِدَةِ إِلَى التَّخَصُّصِ</p>
      </div>
      <div class="curr-grid">
        <div class="curr-item"><div class="lvl">🔤</div><div><h4>الْقَاعِدَةُ النُّورَانِيَّةُ</h4><p>أَسَاسُ قِرَاءَةِ الْحُرُوفِ وَالْكَلِمَاتِ</p></div></div>
        <div class="curr-item"><div class="lvl">📖</div><div><h4>التِّلَاوَةُ وَالتَّجْوِيدُ</h4><p>مَخَارِجُ الْحُرُوفِ وَأَحْكَامُ النُّونِ وَالْمِيمِ</p></div></div>
        <div class="curr-item"><div class="lvl">☝️</div><div><h4>الْعَقِيدَةُ الصَّحِيحَةُ</h4><p>التَّوْحِيدُ وَأَسْمَاءُ اللَّهِ وَصِفَاتُهُ</p></div></div>
        <div class="curr-item"><div class="lvl">🕌</div><div><h4>الْفِقْهُ وَالْأَحْكَامُ</h4><p>الطَّهَارَةُ، الصَّلَاةُ، الزَّكَاةُ، الصِّيَامُ، الْحَجُّ</p></div></div>
        <div class="curr-item"><div class="lvl">🌙</div><div><h4>السِّيرَةُ النَّبَوِيَّةُ</h4><p>دُرُوسٌ وَعِبَرٌ مِنْ حَيَاةِ النَّبِيِّ ﷺ</p></div></div>
        <div class="curr-item"><div class="lvl">✨</div><div><h4>الْبَرْنَامَجُ الشَّامِلُ</h4><p>جَمْعُ الْفُرُوعِ كُلِّهَا فِي مَنْهَجٍ مُتَكَامِلٍ</p></div></div>
      </div>
    </div>
  </section>

  <!-- ===== SOCIAL MEDIA LINKS (NEW SECTION) ===== -->
  <section id="social" style="background: rgba(7, 22, 15, 0.4);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">تَابِعُونَا</div>
        <h2>وَسَائِلُ التَّوَاصُلِ الِاجْتِمَاعِيِّ</h2>
        <p>اِنْضَمَّ إِلَيْنَا عَلَى مَنَصَّاتِنَا الرَّقْمِيَّةِ لِتُوَاصِلَ التَّعَلُّمَ وَالدَّعْوَةَ</p>
      </div>
      <div class="social-grid">

        <!-- Facebook -->
        <div class="social-card">
          <div class="s-icon">📘</div>
          <h4>فَيْسْبُوك</h4>
          <a href="https://www.facebook.com/share/1D9P96HFwe/" target="_blank">facebook.com/share/1D9P96HFwe</a>
        </div>

        <!-- TikTok -->
        <div class="social-card">
          <div class="s-icon">🎵</div>
          <h4>تِيكْ توك</h4>
          <a href="https://www.tiktok.com/@mirkanihararge" target="_blank">@mirkanihararge</a>
        </div>

        <!-- YouTube -->
        <div class="social-card">
          <div class="s-icon">▶️</div>
          <h4>يُوتْيُوب</h4>
          <a href="https://youtube.com/@ferhanshaamil" target="_blank">@ferhanshaamil</a>
        </div>

        <!-- Telegram -->
        <div class="social-card">
          <div class="s-icon">✈️</div>
          <h4>تِلِغْرَام</h4>
          <a href="https://t.me/Ferhan_Shaamil" target="_blank">t.me/Ferhan_Shaamil</a>
        </div>

        <!-- WhatsApp -->
        <div class="social-card">
          <div class="s-icon">💬</div>
          <h4>وَاتْسَاب</h4>
          <a href="https://wa.me/251915455051" target="_blank">+251 915 455 051</a>
        </div>

        <!-- GitHub -->
        <div class="social-card">
          <div class="s-icon">🐙</div>
          <h4>جِيتْ هَب</h4>
          <a href="https://github.com/HamzaAbdulhakim" target="_blank">github.com/HamzaAbdulhakim</a>
        </div>

      </div>
    </div>
  </section>

  <!-- ===== FINAL CTA ===== -->
  <section class="cta" id="contact">
    <div class="container">
      <div class="arabic">خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ</div>
      <h2>اَلْقُرْآنُ يَنْتَظِرُكَ! 📖</h2>
      <p>
        اَلْمَكَانُ هُنَا. 🕌<br>
        اَلْفُرْصَةُ الْآنَ. ⏰<br>
        الرِّحْلَةُ تَبْدَأُ الْيَوْمَ. 🚀<br><br>
        <strong>لِلِاسْتِفْسَارِ:</strong> Ferhanshaamil@gmail.com<br>
        <strong>لِلِاتِّصَالِ:</strong> +251 915 455 051
      </p>
      <a href="https://wa.me/251915455051" target="_blank" class="btn btn-primary">📱 تَوَاصَلْ مَعَنَا عَلَى الْوَاتْسَابِ</a>
    </div>
  </section>

  <!-- ===== FOOTER ===== -->
  <footer>
    <div class="container">
      <div class="ar">مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</div>
      <p><strong>فَرْحَانُ شَامِلُ عَبْدِ الْغَفُورِ</strong> — مُدَرِّسُ الْمَرْكَزِ</p>
      <p style="font-size:13px; color:var(--gold-light);">
        دَاعِيَةٌ • مُعَلِّمُ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ • طَالِبُ هَنْدَسَةِ الْبَرْمَجِيَّاتِ
      </p>
      
      <div class="footer-socials">
        <a href="https://www.facebook.com/share/1D9P96HFwe/" target="_blank" title="Facebook">📘</a>
        <a href="https://www.tiktok.com/@mirkanihararge" target="_blank" title="TikTok">🎵</a>
        <a href="https://youtube.com/@ferhanshaamil" target="_blank" title="YouTube">▶️</a>
        <a href="https://t.me/Ferhan_Shaamil" target="_blank" title="Telegram">✈️</a>
        <a href="https://wa.me/251915455051" target="_blank" title="WhatsApp">💬</a>
        <a href="https://github.com/HamzaAbdulhakim" target="_blank" title="GitHub">🐙</a>
        <a href="mailto:Ferhanshaamil@gmail.com" title="Email">📧</a>
      </div>
      
      <p style="margin-top:15px;">© 2026 جَمِيعُ الْحُقُوقِ مَحْفُوظَةٌ</p>
    </div>
  </footer>

  <!-- ===== WHATSAPP FLOATING ===== -->
  <a href="https://wa.me/251915455051" target="_blank" class="wa" title="واتساب">💬</a>

</body>
</html><!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ - لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</title>
  <meta name="description" content="مركز أويس بن عامر - منارة العلوم الشرعية والقرآن الكريم، مزود بتقنيات التعليم الرقمي والذكاء الاصطناعي.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;600;700;800;900&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --bg: #040d09;
      --bg2: #0a1f15;
      --card: rgba(11, 44, 30, 0.75);
      --gold: #d6b45d;
      --gold-light: #f2d98d;
      --green: #0d9e6e;
      --white: #f7f5ed;
      --text: #d1ddd6;
      --muted: #98aea4;
      --border: rgba(214, 180, 93, 0.25);
    }

    body {
      font-family: 'Cairo', 'Amiri', sans-serif;
      background: radial-gradient(circle at 10% 20%, rgba(214, 180, 93, 0.08), transparent 30%),
        radial-gradient(circle at 90% 70%, rgba(13, 158, 110, 0.15), transparent 35%),
        var(--bg);
      color: var(--white);
      line-height: 1.9;
      min-height: 100vh;
    }

    .container {
      width: min(1180px, 92%);
      margin: 0 auto;
    }

    /* ===== NAVBAR ===== */
    nav {
      position: fixed;
      top: 0;
      right: 0;
      left: 0;
      z-index: 999;
      background: rgba(4, 13, 9, 0.92);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid var(--border);
      padding: 0 5%;
    }

    .nav-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      min-height: 75px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-icon {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      border: 1px solid var(--gold);
      display: grid;
      place-items: center;
      font-size: 22px;
      color: var(--gold-light);
    }

    .logo-text strong {
      display: block;
      color: var(--gold-light);
      font-size: 15px;
      letter-spacing: 0.5px;
    }

    .logo-text small {
      display: block;
      color: var(--muted);
      font-size: 9px;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      list-style: none;
      font-size: 14px;
    }

    .nav-links a {
      color: var(--text);
      transition: 0.3s;
      font-weight: 600;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .nav-cta {
      border: 1px solid var(--gold);
      padding: 8px 18px;
      border-radius: 30px;
      color: var(--gold-light) !important;
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 150px 0 80px;
      position: relative;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 50px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      border: 1px solid var(--border);
      background: rgba(214, 180, 93, 0.08);
      padding: 8px 18px;
      border-radius: 40px;
      color: var(--gold-light);
      font-size: 13px;
      margin-bottom: 20px;
      font-weight: 700;
    }

    .hero h1 {
      font-size: clamp(38px, 6vw, 70px);
      line-height: 1.1;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .hero h1 span {
      color: var(--gold-light);
    }

    .hero-sub {
      font-size: clamp(20px, 3vw, 30px);
      color: var(--gold);
      margin: 15px 0 10px;
      font-weight: 700;
    }

    .hero-motto {
      font-family: 'Amiri', serif;
      font-size: clamp(22px, 3.5vw, 38px);
      color: #f5eace;
      margin: 15px 0 20px;
      line-height: 1.7;
      border-right: 4px solid var(--gold);
      padding-right: 20px;
    }

    .hero-desc {
      color: var(--muted);
      font-size: 16px;
      max-width: 650px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 30px;
    }

    .btn {
      padding: 13px 28px;
      border-radius: 35px;
      font-weight: 700;
      font-size: 14px;
      transition: 0.3s;
      display: inline-block;
      border: 1px solid var(--gold);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold-light), var(--gold));
      color: #07130d;
      border: none;
    }

    .btn-primary:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 30px rgba(214, 180, 93, 0.3);
    }

    .btn-outline {
      background: transparent;
      color: var(--white);
    }
    .btn-outline:hover {
      background: rgba(214, 180, 93, 0.1);
      border-color: var(--gold-light);
    }

    .hero-card {
      border: 1px solid var(--border);
      background: var(--card);
      backdrop-filter: blur(10px);
      border-radius: 35px;
      padding: 35px 25px;
      text-align: center;
      box-shadow: 0 30px 70px rgba(0, 0, 0, 0.4);
    }

    .hero-symbol {
      width: 130px;
      height: 130px;
      margin: 0 auto 20px;
      border-radius: 50%;
      border: 1px solid var(--gold);
      display: grid;
      place-items: center;
      font-size: 60px;
      background: radial-gradient(circle, rgba(214, 180, 93, 0.15), transparent 65%);
    }

    .hero-card h3 {
      color: var(--gold-light);
      font-size: 22px;
      margin-bottom: 5px;
    }

    .hero-card p {
      color: var(--muted);
      font-size: 13px;
    }
    .hero-card .arabic-tag {
      font-family: 'Amiri', serif;
      font-size: 18px;
      color: #eee4c8;
      margin-top: 12px;
    }

    /* ===== SECTIONS ===== */
    section {
      padding: 100px 0;
    }

    .section-head {
      text-align: center;
      max-width: 800px;
      margin: 0 auto 55px;
    }

    .section-mini {
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 4px;
      font-size: 12px;
      font-weight: 700;
    }

    .section-head h2 {
      font-size: clamp(30px, 5vw, 48px);
      margin: 10px 0;
    }

    .section-head .arabic-sub {
      font-family: 'Amiri', serif;
      color: var(--gold-light);
      font-size: 22px;
      margin-top: 5px;
    }

    .section-head p {
      color: var(--muted);
      font-size: 15px;
    }

    /* ===== FEATURES GRID ===== */
    .features-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .feature {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 32px 25px;
      text-align: center;
      transition: 0.4s;
      backdrop-filter: blur(6px);
    }

    .feature:hover {
      transform: translateY(-10px);
      border-color: var(--gold);
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
    }

    .feature .icon {
      font-size: 45px;
      margin-bottom: 15px;
    }

    .feature h3 {
      color: var(--gold-light);
      font-size: 19px;
      margin-bottom: 10px;
    }

    .feature p {
      color: var(--muted);
      font-size: 13px;
    }

    .feature .ar-desc {
      font-family: 'Amiri', serif;
      font-size: 14px;
      color: #c7d4cd;
      margin-top: 8px;
    }

    /* ===== MISSION / VISION ===== */
    .mission-box {
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 60px 30px;
      background: radial-gradient(circle at center, rgba(13, 158, 110, 0.15), transparent 60%), rgba(8, 25, 18, 0.8);
      text-align: center;
    }

    .mission-box .big-arabic {
      font-family: 'Amiri', serif;
      font-size: clamp(28px, 4vw, 45px);
      color: var(--gold-light);
      line-height: 2;
    }

    .mission-box p {
      color: var(--muted);
      max-width: 800px;
      margin: 20px auto 0;
      font-size: 16px;
    }

    /* ===== MODERN TOOLS ===== */
    .tools-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .tool {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 25px 15px;
      text-align: center;
    }

    .tool .icon {
      font-size: 32px;
    }

    .tool h4 {
      color: var(--gold-light);
      font-size: 15px;
      margin-top: 8px;
    }

    .tool span {
      display: block;
      color: var(--muted);
      font-size: 11px;
    }

    /* ===== CURRICULUM ===== */
    .curr-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
    }

    .curr-item {
      display: flex;
      gap: 18px;
      align-items: center;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 20px;
    }

    .curr-item .lvl {
      font-size: 28px;
    }

    .curr-item h4 {
      color: var(--gold-light);
      font-size: 16px;
    }

    .curr-item p {
      color: var(--muted);
      font-size: 12px;
    }

    /* ===== CTA ===== */
    .cta {
      text-align: center;
      padding: 100px 20px;
      background: radial-gradient(circle, rgba(214, 180, 93, 0.1), transparent 55%);
    }

    .cta .arabic {
      font-family: 'Amiri', serif;
      font-size: 35px;
      color: var(--gold-light);
    }

    .cta h2 {
      font-size: clamp(32px, 5vw, 52px);
      color: var(--white);
      margin: 15px 0;
    }

    .cta p {
      color: var(--muted);
      max-width: 600px;
      margin: 0 auto 30px;
    }

    /* ===== FOOTER ===== */
    footer {
      border-top: 1px solid var(--border);
      background: #020906;
      padding: 45px 0;
      text-align: center;
    }

    footer strong {
      color: var(--gold-light);
    }

    footer .ar {
      font-family: 'Amiri', serif;
      color: #d4cbaa;
      font-size: 20px;
      margin: 5px 0;
    }

    footer p {
      color: var(--muted);
      font-size: 12px;
    }

    /* ===== WHATSAPP ===== */
    .wa {
      position: fixed;
      bottom: 20px;
      left: 20px;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      background: #25d366;
      display: grid;
      place-items: center;
      font-size: 28px;
      z-index: 500;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 900px) {
      .nav-links {
        display: none;
      }
      .hero-grid {
        grid-template-columns: 1fr;
        text-align: center;
      }
      .hero-motto {
        border-right: none;
        padding-right: 0;
        text-align: center;
      }
      .hero-desc {
        margin: 0 auto;
      }
      .hero-buttons {
        justify-content: center;
      }
      .features-grid {
        grid-template-columns: 1fr 1fr;
      }
      .tools-grid {
        grid-template-columns: 1fr 1fr;
      }
      .curr-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 550px) {
      .features-grid,
      .tools-grid {
        grid-template-columns: 1fr;
      }
      .hero {
        padding-top: 120px;
      }
      section {
        padding: 70px 0;
      }
      .mission-box {
        padding: 40px 20px;
      }
    }
  </style>
</head>

<body>

  <!-- ===== NAVBAR ===== -->
  <nav>
    <div class="container nav-inner">
      <a href="#home" class="logo">
        <div class="logo-icon">🌿</div>
        <div class="logo-text">
          <strong>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</strong>
          <small>لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</small>
        </div>
      </a>
      <ul class="nav-links">
        <li><a href="#home">الرئيسية</a></li>
        <li><a href="#vision">الرؤية</a></li>
        <li><a href="#tools">التقنيات</a></li>
        <li><a href="#curriculum">المنهج</a></li>
        <li><a href="#contact" class="nav-cta">اتصل بنا</a></li>
      </ul>
    </div>
  </nav>

  <!-- ===== HERO ===== -->
  <section class="hero" id="home">
    <div class="container hero-grid">
      <div>
        <div class="badge">🌿✨ الْمَوْقِعُ الرَّسْمِيُّ الْجَدِيدُ</div>
        <h1>مَرْكَزُ <span>أُوَيْسِ بْنِ عَامِرٍ</span></h1>
        <div class="hero-sub">لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</div>
        <div class="hero-motto">
          مِنَ الْكِتَابِ إِلَى التِّقْنِيَةِ،<br>
          وَمِنَ التَّعَلُّمِ إِلَى التَّمَيُّزِ.
        </div>
        <p class="hero-desc">
          مَرْكَزٌ عِلْمِيٌّ رَائِدٌ يَجْمَعُ بَيْنَ أَصَالَةِ الْعُلُومِ الشَّرْعِيَّةِ وَرُوحِ الْعَصْرِ،
          مُسَخِّرًا الذَّكَاءَ الاصْطِنَاعِيَّ وَالتَّعْلِيمَ الرَّقْمِيَّ لِبِنَاءِ جِيلٍ قُرْآنِيٍّ مُتْقَنٍ.
        </p>
        <div class="hero-buttons">
          <a href="#vision" class="btn btn-primary">اِكْتَشِفِ الرُّؤْيَةَ</a>
          <a href="#tools" class="btn btn-outline">اَلتَّقْنِيَاتُ الْحَدِيثَةُ</a>
        </div>
      </div>
      <div class="hero-card">
        <div class="hero-symbol">🕌</div>
        <h3>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</h3>
        <p class="arabic-tag">مَنَارَةُ الْعِلْمِ الشَّرْعِيِّ</p>
        <p style="margin-top:15px;">
          📖 الْقُرْآنُ • 🕌 الْفِقْهُ • ☝️ الْعَقِيدَةُ<br>
          🌙 السِّيرَةُ • 💻 الذَّكَاءُ الْاصْطِنَاعِيُّ
        </p>
      </div>
    </div>
  </section>

  <!-- ===== VISION / MISSION ===== -->
  <section id="vision">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">رُؤْيَتُنَا</div>
        <h2>نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ</h2>
        <div class="arabic-sub">وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ</div>
      </div>
      <div class="mission-box">
        <div class="big-arabic">
          نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،<br>
          وَنُعَرِّفُكَ بِنَبِيِّكَ ﷺ،<br>
          وَنُفَهِّمُكَ دِينَكَ،<br>
          وَنُصَحِّحُ لَكَ عَقِيدَتَكَ.
        </div>
        <p>
          نَطْمَحُ إِلَى أَنْ نَكُونَ صَرْحًا تَعْلِيمِيًّا عَصْرِيًّا يُوَازِنُ بَيْنَ الْعُلُومِ الشَّرْعِيَّةِ وَالتِّقْنِيَةِ،
          لِنُخَرِّجَ جِيلًا يَقْرَأُ الْقُرْآنَ إِتْقَانًا، وَيَفْهَمُ دِينَهُ فَهْمًا، وَيَسْتَخْدِمُ التِّقْنِيَةَ فِي الْخَيْرِ.
        </p>
        <p style="margin-top:15px; font-family:'Amiri',serif; color:var(--gold-light); font-size:20px;">
          "مِنَ الْكِتَابِ إِلَى التِّقْنِيَةِ، وَمِنَ التَّعَلُّمِ إِلَى التَّمَيُّزِ"
        </p>
      </div>
    </div>
  </section>

  <!-- ===== MODERN FEATURES ===== -->
  <section>
    <div class="container">
      <div class="section-head">
        <div class="section-mini">مَا نُقَدِّمُهُ</div>
        <h2>مِيْزَاتُنَا التَّقْنِيَّةُ</h2>
        <p>نَمْزِجُ بَيْنَ الْعِلْمِ الشَّرْعِيِّ وَأَحْدَثِ أَدَوَاتِ الْعَصْرِ الرَّقْمِيَّةِ</p>
      </div>
      <div class="features-grid">

        <div class="feature">
          <div class="icon">📱</div>
          <h3>التَّعْلِيمُ الرَّقْمِيُّ</h3>
          <p>دُرُوسٌ، مَقَاطِعُ فِيدْيُو، وَمُلَخَّصَاتٌ عَبْرَ التِّلِغْرَامِ وَالْوَاتْسَابِ.</p>
          <div class="ar-desc">تَعَلُّمٌ مَرِنٌ فِي أَيِّ وَقْتٍ</div>
        </div>

        <div class="feature">
          <div class="icon">🤖</div>
          <h3>الذَّكَاءُ الْاصْطِنَاعِيُّ</h3>
          <p>تَحْلِيلُ الْأَدَاءِ، تَصْحِيحُ الْأَخْطَاءِ، وَإِنْشَاءُ الِاخْتِبَارَاتِ الذَّكِيَّةِ.</p>
          <div class="ar-desc">تَقْنِيَةٌ لِلتَّفَوُّقِ</div>
        </div>

        <div class="feature">
          <div class="icon">📝</div>
          <h3>الِاخْتِبَارَاتُ الْإِلِكْتِرُونِيَّةُ</h3>
          <p>اِخْتِبَارَاتٌ أُسْبُوعِيَّةٌ، شَهْرِيَّةٌ، وَخِتَامِيَّةٌ بِتَصْحِيحٍ آليٍّ.</p>
          <div class="ar-desc">تَقْيِيمٌ مُسْتَمِرٌّ</div>
        </div>

        <div class="feature">
          <div class="icon">🎓</div>
          <h3>إِدَارَةُ الطُّلَّابِ</h3>
          <p>مُتَابَعَةُ الْحُضُورِ، الدُّرُوسِ، وَتَقَارِيرُ التَّقَدُّمِ الْفَرْدِيَّةِ.</p>
          <div class="ar-desc">نِظَامٌ إِدَارِيٌّ مُتَكَامِلٌ</div>
        </div>

        <div class="feature">
          <div class="icon">📚</div>
          <h3>مَنْهَجٌ مُتَدَرِّجٌ</h3>
          <p>مُبْتَدِئ → مُتَوَسِّط → مُتَقَدِّم → دِبْلُومٌ فِي الْعُلُومِ الشَّرْعِيَّةِ.</p>
          <div class="ar-desc">مَسَارٌ عِلْمِيٌّ وَاضِحٌ</div>
        </div>

        <div class="feature">
          <div class="icon">🏆</div>
          <h3>الشَّهَادَاتُ الْمُعْتَمَدَةُ</h3>
          <p>شَهَادَاتٌ رَقْمِيَّةٌ وَوَرَقِيَّةٌ مُعْتَمَدَةٌ بَعْدَ إِتْمَامِ الْبَرَامِجِ.</p>
          <div class="ar-desc">تَوْثِيقٌ رَسْمِيٌّ لِلْجُهُودِ</div>
        </div>

      </div>
    </div>
  </section>

  <!-- ===== MODERN TOOLS ===== -->
  <section id="tools" style="background: rgba(7, 22, 15, 0.6);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">أَدَوَاتُنَا</div>
        <h2>أَحْدَثُ تَقْنِيَاتِ التَّعْلِيمِ</h2>
        <p>نَسْتَخْدِمُ مَا يَجْعَلُ التَّعَلُّمَ سَهْلًا وَمُمْتِعًا</p>
      </div>
      <div class="tools-grid">
        <div class="tool"><div class="icon">📹</div><h4>الدُّرُوسُ الْفِيدْيُو</h4><span>مَحْتَوَى بَصَرِيٌّ غَنِيٌّ</span></div>
        <div class="tool"><div class="icon">🎙️</div><h4>التِّلَاوَةُ الصَّوْتِيَّةُ</h4><span>تَصْحِيحُ التَّجْوِيدِ</span></div>
        <div class="tool"><div class="icon">📊</div><h4>التَّحْلِيلُ الْآلِيُّ</h4><span>إِحْصَاءُ التَّقَدُّمِ</span></div>
        <div class="tool"><div class="icon">💬</div><h4>التَّفَاعُلُ الْمُبَاشِرُ</h4><span>مَجْمُوعَاتُ الْمُنَاقَشَةِ</span></div>
        <div class="tool"><div class="icon">🖥️</div><h4>الْفَصْلُ الذَّكِيُّ</h4><span>سَبُورَةٌ رَقْمِيَّةٌ</span></div>
        <div class="tool"><div class="icon">🤖</div><h4>مُسَاعِدُ الذَّكَاءِ</h4><span>إِجَابَةُ الْأَسْئِلَةِ</span></div>
        <div class="tool"><div class="icon">📝</div><h4>النَّمَاذِجُ الْإِلِكْتِرُونِيَّةُ</h4><span>جُوجِلُ فُورْمْ</span></div>
        <div class="tool"><div class="icon">🔐</div><h4>سِجِلَّاتٌ آمِنَةٌ</h4><span>حِفْظُ الْبَيَانَاتِ</span></div>
      </div>
    </div>
  </section>

  <!-- ===== CURRICULUM ===== -->
  <section id="curriculum">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">الْمَنْهَجُ الدِّرَاسِيُّ</div>
        <h2>بَرَامِجُنَا الْمُتَمَيِّزَةُ</h2>
        <p>مَسَارٌ عِلْمِيٌّ مُنَظَّمٌ مِنَ الْقَاعِدَةِ إِلَى التَّخَصُّصِ</p>
      </div>
      <div class="curr-grid">
        <div class="curr-item"><div class="lvl">🔤</div><div><h4>الْقَاعِدَةُ النُّورَانِيَّةُ</h4><p>أَسَاسُ قِرَاءَةِ الْحُرُوفِ وَالْكَلِمَاتِ</p></div></div>
        <div class="curr-item"><div class="lvl">📖</div><div><h4>التِّلَاوَةُ وَالتَّجْوِيدُ</h4><p>مَخَارِجُ الْحُرُوفِ وَأَحْكَامُ النُّونِ وَالْمِيمِ</p></div></div>
        <div class="curr-item"><div class="lvl">☝️</div><div><h4>الْعَقِيدَةُ الصَّحِيحَةُ</h4><p>التَّوْحِيدُ وَأَسْمَاءُ اللَّهِ وَصِفَاتُهُ</p></div></div>
        <div class="curr-item"><div class="lvl">🕌</div><div><h4>الْفِقْهُ وَالْأَحْكَامُ</h4><p>الطَّهَارَةُ، الصَّلَاةُ، الزَّكَاةُ، الصِّيَامُ، الْحَجُّ</p></div></div>
        <div class="curr-item"><div class="lvl">🌙</div><div><h4>السِّيرَةُ النَّبَوِيَّةُ</h4><p>دُرُوسٌ وَعِبَرٌ مِنْ حَيَاةِ النَّبِيِّ ﷺ</p></div></div>
        <div class="curr-item"><div class="lvl">✨</div><div><h4>الْبَرْنَامَجُ الشَّامِلُ</h4><p>جَمْعُ الْفُرُوعِ كُلِّهَا فِي مَنْهَجٍ مُتَكَامِلٍ</p></div></div>
      </div>
    </div>
  </section>

  <!-- ===== FINAL CTA ===== -->
  <section class="cta" id="contact">
    <div class="container">
      <div class="arabic">خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ</div>
      <h2>اَلْقُرْآنُ يَنْتَظِرُكَ! 📖</h2>
      <p>
        اَلْمَكَانُ هُنَا. 🕌<br>
        اَلْفُرْصَةُ الْآنَ. ⏰<br>
        الرِّحْلَةُ تَبْدَأُ الْيَوْمَ. 🚀
      </p>
      <a href="https://wa.me/251915455051" target="_blank" class="btn btn-primary">📱 تَوَاصَلْ مَعَنَا عَلَى الْوَاتْسَابِ</a>
    </div>
  </section>

  <!-- ===== FOOTER ===== -->
  <footer>
    <div class="container">
      <div class="ar">مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</div>
      <p><strong>فَرْحَانُ شَامِلُ عَبْدِ الْغَفُورِ</strong> — مُدَرِّسُ الْمَرْكَزِ</p>
      <p style="font-size:13px; color:var(--gold-light);">
        دَاعِيَةٌ • مُعَلِّمُ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ • طَالِبُ هَنْدَسَةِ الْبَرْمَجِيَّاتِ
      </p>
      <p>© 2026 جَمِيعُ الْحُقُوقِ مَحْفُوظَةٌ</p>
    </div>
  </footer>

  <!-- ===== WHATSAPP FLOATING ===== -->
  <a href="https://wa.me/251915455051" target="_blank" class="wa" title="واتساب">💬</a>

</body>
</html><!DOCTYPE html>
<html lang="om" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>فرحان شامل | مركز أُويس بن عامر</title>
  <meta name="description" content="فرحان شامل — داعية ومُعلِّم القرآن والعلوم الشرعية. مركز أُويس بن عامر لدراسة العلوم الشرعية.">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --bg: #04100c;
      --bg2: #071a13;
      --card: rgba(13, 42, 31, .72);
      --card2: #0b2419;
      --green: #0d5138;
      --green-light: #18704d;
      --gold: #d6b45d;
      --gold-light: #f2d98d;
      --white: #f7f5ed;
      --text: #d8e2dc;
      --muted: #9eaea6;
      --border: rgba(214, 180, 93, .25);
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: radial-gradient(circle at 15% 10%, rgba(214, 180, 93, .08), transparent 25%), radial-gradient(circle at 85% 40%, rgba(24, 112, 77, .12), transparent 30%), var(--bg);
      color: var(--white);
      line-height: 1.7;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1180px, 92%);
      margin: auto;
    }

    /* ===== NAVBAR ===== */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 999;
      background: rgba(4, 16, 12, .88);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid var(--border);
    }

    .nav {
      min-height: 76px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 11px;
    }

    .logo-mark {
      width: 45px;
      height: 45px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      border: 1px solid var(--gold);
      background: rgba(214, 180, 93, .06);
      font-size: 22px;
    }

    .logo-text strong {
      display: block;
      color: var(--gold-light);
      font-size: 14px;
      letter-spacing: .7px;
    }

    .logo-text small {
      display: block;
      color: var(--muted);
      font-size: 9px;
    }

    .nav-links {
      display: flex;
      gap: 20px;
      align-items: center;
      list-style: none;
      font-size: 13px;
    }

    .nav-links a {
      color: var(--text);
      transition: .3s;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .nav-contact {
      border: 1px solid var(--gold);
      padding: 8px 15px;
      border-radius: 25px;
      color: var(--gold-light) !important;
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 100vh;
      padding: 145px 0 80px;
      display: flex;
      align-items: center;
      position: relative;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 50px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      padding: 7px 15px;
      border: 1px solid var(--border);
      background: rgba(214, 180, 93, .06);
      border-radius: 30px;
      color: var(--gold-light);
      font-size: 12px;
      margin-bottom: 20px;
    }

    .hero h1 {
      font-size: clamp(40px, 6vw, 76px);
      line-height: 1.05;
      letter-spacing: -2px;
    }

    .hero h1 span {
      color: var(--gold-light);
    }

    .hero-title {
      color: var(--text);
      font-size: clamp(18px, 3vw, 25px);
      margin: 20px 0 12px;
    }

    .arabic {
      direction: rtl;
      text-align: right;
      font-family: "Times New Roman", serif;
    }

    .hero-arabic {
      color: var(--gold-light);
      font-size: clamp(22px, 3vw, 32px);
      margin: 15px 0;
    }

    .hero-description {
      max-width: 680px;
      color: var(--muted);
      font-size: 15px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 28px;
    }

    .btn {
      display: inline-block;
      padding: 12px 22px;
      border-radius: 30px;
      border: 1px solid var(--gold);
      font-weight: bold;
      font-size: 13px;
      transition: .3s;
    }

    .btn:hover {
      transform: translateY(-4px);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold-light), var(--gold));
      color: #07130e;
      border: none;
    }

    .hero-card {
      border: 1px solid var(--border);
      background: linear-gradient(145deg, rgba(18, 68, 48, .7), rgba(7, 27, 19, .8));
      border-radius: 35px;
      padding: 35px;
      text-align: center;
      box-shadow: 0 30px 70px rgba(0, 0, 0, .25);
    }

    .hero-symbol {
      width: 150px;
      height: 150px;
      margin: auto;
      border-radius: 50%;
      display: grid;
      place-items: center;
      border: 1px solid var(--gold);
      background: radial-gradient(circle, rgba(214, 180, 93, .15), transparent 65%);
      font-size: 70px;
    }

    .hero-card h3 {
      margin-top: 20px;
      color: var(--gold-light);
    }

    .hero-card p {
      color: var(--muted);
      font-size: 13px;
      margin-top: 7px;
    }

    /* ===== SECTIONS ===== */
    section {
      padding: 90px 0;
    }

    .section-head {
      text-align: center;
      max-width: 760px;
      margin: 0 auto 45px;
    }

    .section-mini {
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 3px;
      font-size: 11px;
    }

    .section-head h2 {
      font-size: clamp(29px, 5vw, 45px);
      margin: 7px 0;
    }

    .section-head p {
      color: var(--muted);
      font-size: 14px;
    }

    /* ===== ABOUT ===== */
    .personal {
      background: rgba(7, 26, 19, .55);
    }

    .personal-grid {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 25px;
      align-items: stretch;
    }

    .profile-card,
    .content-card {
      border: 1px solid var(--border);
      background: var(--card);
      border-radius: 27px;
      padding: 32px;
    }

    .profile-icon {
      width: 115px;
      height: 115px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      margin-bottom: 20px;
      border: 1px solid var(--gold);
      background: rgba(214, 180, 93, .07);
      font-size: 50px;
    }

    .profile-card h3 {
      color: var(--gold-light);
      font-size: 23px;
    }

    .profile-card .role {
      color: var(--muted);
      margin: 6px 0 20px;
      font-size: 13px;
    }

    .profile-list {
      list-style: none;
      display: grid;
      gap: 9px;
      color: var(--text);
      font-size: 13px;
    }

    .content-card h3 {
      color: var(--gold-light);
      margin-bottom: 12px;
      font-size: 24px;
    }

    .content-card p {
      color: var(--muted);
      margin-bottom: 14px;
    }

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-top: 20px;
    }

    .skill {
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 6px 12px;
      color: var(--gold-light);
      background: rgba(214, 180, 93, .05);
      font-size: 11px;
    }

    /* ===== MARKAZA ===== */
    .markaza-box {
      position: relative;
      overflow: hidden;
      text-align: center;
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 60px 25px;
      background: radial-gradient(circle at center, rgba(24, 112, 77, .28), transparent 60%), rgba(8, 29, 21, .75);
    }

    .markaza-icon {
      font-size: 50px;
    }

    .markaza-box h2 {
      color: var(--gold-light);
      font-size: clamp(27px, 5vw, 46px);
      margin-top: 10px;
    }

    .markaza-arabic {
      color: #eee4c8;
      font-size: 25px;
      margin: 8px 0 20px;
    }

    .markaza-box p {
      max-width: 780px;
      margin: auto;
      color: var(--muted);
    }

    /* ===== PROGRAMS ===== */
    .program-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .program {
      position: relative;
      border: 1px solid var(--border);
      border-radius: 23px;
      padding: 28px;
      background: var(--card2);
      transition: .35s;
      overflow: hidden;
    }

    .program:hover {
      transform: translateY(-7px);
      border-color: var(--gold);
    }

    .program-icon {
      font-size: 37px;
    }

    .program h3 {
      font-size: 18px;
      margin-top: 8px;
    }

    .program p {
      color: var(--muted);
      font-size: 13px;
      margin: 7px 0 15px;
    }

    .duration {
      display: inline-block;
      padding: 5px 11px;
      border-radius: 20px;
      border: 1px solid var(--border);
      color: var(--gold-light);
      font-size: 10px;
    }

    /* ===== CURRICULUM ===== */
    .curriculum {
      background: rgba(7, 26, 19, .55);
    }

    .book-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
    }

    .book {
      display: flex;
      gap: 16px;
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 22px;
      background: var(--card);
    }

    .book-icon {
      font-size: 31px;
    }

    .book h3 {
      color: var(--gold-light);
      font-size: 16px;
    }

    .book p {
      color: var(--muted);
      font-size: 12px;
      margin-top: 4px;
    }

    /* ===== MESSAGE ===== */
    .message-box {
      max-width: 900px;
      margin: auto;
      text-align: center;
      padding: 45px 25px;
      border-radius: 28px;
      border: 1px solid var(--border);
      background: linear-gradient(135deg, #0d3021, #071c14);
    }

    .message-box .arabic {
      text-align: center;
      color: var(--gold-light);
      font-size: 25px;
      line-height: 1.9;
    }

    .message-box p {
      color: var(--muted);
      margin-top: 18px;
      font-size: 14px;
    }

    /* ===== CONTACT ===== */
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .contact-card {
      text-align: center;
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 28px;
      background: var(--card);
      transition: .3s;
    }

    .contact-card:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
    }

    .contact-icon {
      font-size: 34px;
    }

    .contact-card h3 {
      color: var(--gold-light);
      margin: 8px 0;
    }

    .contact-card p {
      color: var(--muted);
      font-size: 13px;
      word-break: break-word;
    }

    /* ===== CTA ===== */
    .cta {
      text-align: center;
      padding: 95px 20px;
      background: radial-gradient(circle, rgba(24, 112, 77, .3), transparent 60%);
    }

    .cta .arabic {
      text-align: center;
      color: var(--gold-light);
      font-size: 28px;
      margin-bottom: 12px;
    }

    .cta h2 {
      font-size: clamp(32px, 6vw, 55px);
      color: var(--gold-light);
    }

    .cta p {
      color: var(--muted);
      max-width: 650px;
      margin: 10px auto 25px;
    }

    /* ===== FOOTER ===== */
    footer {
      border-top: 1px solid var(--border);
      background: #020a07;
      padding: 40px 0;
      text-align: center;
    }

    footer .footer-logo {
      font-size: 28px;
      margin-bottom: 8px;
    }

    footer strong {
      color: var(--gold-light);
    }

    footer p {
      color: var(--muted);
      font-size: 11px;
      margin-top: 5px;
    }

    /* ===== FLOATING WHATSAPP ===== */
    .floating {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 500;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: #16804f;
      border: 2px solid rgba(255, 255, 255, .2);
      font-size: 25px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, .4);
    }

    /* ===== RESPONSIVE ===== */
    @media(max-width:900px) {
      .nav-links {
        display: none;
      }
      .hero-grid,
      .personal-grid {
        grid-template-columns: 1fr;
      }
      .program-grid {
        grid-template-columns: repeat(2, 1fr);
      }
      .contact-grid {
        grid-template-columns: 1fr;
      }
    }

    @media(max-width:560px) {
      section {
        padding: 65px 0;
      }
      .hero {
        padding-top: 125px;
      }
      .hero h1 {
        font-size: 42px;
      }
      .hero-card {
        padding: 25px;
      }
      .program-grid,
      .book-grid {
        grid-template-columns: 1fr;
      }
      .profile-card,
      .content-card {
        padding: 24px;
      }
      .markaza-box {
        padding: 42px 18px;
      }
    }
  </style>
</head>

<body>

  <!-- ===== NAVIGATION ===== -->
  <nav>
    <div class="container nav">
      <a href="#home" class="logo">
        <div class="logo-mark">🌿</div>
        <div class="logo-text">
          <strong>فَرْحَان شَامِل</strong>
          <small>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</small>
        </div>
      </a>
      <ul class="nav-links">
        <li><a href="#home">الصفحة الرئيسية</a></li>
        <li><a href="#about">عنِّي</a></li>
        <li><a href="#markaza">المركز</a></li>
        <li><a href="#programs">البرامج</a></li>
        <li><a href="#curriculum">المنهج</a></li>
        <li><a href="#contact" class="nav-contact">اتصل بنا</a></li>
      </ul>
    </div>
  </nav>

  <!-- ===== HERO ===== -->
  <section class="hero" id="home">
    <div class="container hero-grid">
      <div>
        <div class="badge">🌿✨ الْمَوْقِعُ الرَّسْمِيُّ • الْقُرْآنُ • الْعِلْمُ • التِّقْنِيَةُ</div>
        <h1>فَرْحَان<br><span>شَامِل</span></h1>
        <div class="hero-title">دَاعِيَةٌ • مُعَلِّمٌ • طَالِبُ هَنْدَسَةِ الْبَرْمَجِيَّاتِ</div>
        <div class="arabic hero-arabic">فَرْحَانُ شَامِلُ عَبْدِ الْغَفُورِ</div>
        <p class="hero-description">
          أَنَا فَرْحَانُ شَامِلُ عَبْدِ الْغَفُورِ، مُعَلِّمٌ فِي مَرْكَزِ أُوَيْسِ بْنِ عَامِرٍ،
          دَاعِيَةٌ وَطَالِبُ هَنْدَسَةِ الْبَرْمَجِيَّاتِ. هَدَفِي تَعْلِيمُ الْقُرْآنِ
          وَالْعُلُومِ الشَّرْعِيَّةِ، وَبِنَاءُ جِيلٍ وَاعٍ بِدِينِهِ وَأَخْلَاقِهِ،
          مَعَ تَسْخِيرِ التِّقْنِيَةِ الْحَدِيثَةِ فِي سَبِيلِ الدَّعْوَةِ وَالتَّعْلِيمِ.
        </p>
        <div class="hero-buttons">
          <a href="#markaza" class="btn btn-primary">🕌 تَعَرَّفْ عَلَى الْمَرْكَزِ</a>
          <a href="#programs" class="btn">📚 اِسْتَعْرِضِ الْبَرَامِجَ</a>
        </div>
      </div>
      <div class="hero-card">
        <div class="hero-symbol">🕌</div>
        <h3>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</h3>
        <p>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</p>
        <p style="margin-top:18px;">📖 الْقُرْآنُ<br>🕌 الْعُلُومُ الشَّرْعِيَّةُ<br>🌱 التَّرْبِيَةُ<br>💻 التِّقْنِيَةُ</p>
      </div>
    </div>
  </section>

  <!-- ===== ABOUT ===== -->
  <section class="personal" id="about">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">عَنِّي</div>
        <h2>👤 عَنِّي</h2>
        <p>اَلْجَمْعُ بَيْنَ الْعِلْمِ الشَّرْعِيِّ وَالتِّقْنِيَةِ الْحَدِيثَةِ</p>
      </div>
      <div class="personal-grid">
        <div class="profile-card">
          <div class="profile-icon">👤</div>
          <h3>فَرْحَانُ شَامِلُ عَبْدِ الْغَفُورِ</h3>
          <div class="role">دَاعِيَةٌ • مُعَلِّمٌ • طَالِبُ هَنْدَسَةِ الْبَرْمَجِيَّاتِ</div>
          <ul class="profile-list">
            <li>🕌 مُعَلِّمٌ فِي مَرْكَزِ أُوَيْسِ بْنِ عَامِرٍ</li>
            <li>📖 تَعْلِيمُ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ</li>
            <li>🌱 تَرْبِيَةُ النَّشْءِ وَبِنَاؤُهُمْ</li>
            <li>💻 هَنْدَسَةُ الْبَرْمَجِيَّاتِ</li>
            <li>🚀 التَّعْلِيمُ الرَّقْمِيُّ</li>
          </ul>
        </div>
        <div class="content-card">
          <h3>🌿 هَدَفِي</h3>
          <p>
            أَسْعَى إِلَى تَعْلِيمِ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ بِطَرِيقَةٍ عَصْرِيَّةٍ،
            وَبِنَاءِ جِيلٍ يَجْمَعُ بَيْنَ الْعِلْمِ الشَّرْعِيِّ وَالْمَهَارَاتِ الرَّقْمِيَّةِ،
            لِيَكُونَ نَافِعًا لِنَفْسِهِ وَمُجْتَمَعِهِ.
          </p>
          <p>
            كَمَا أَسْخَرُ التِّقْنِيَةَ فِي تَوْسِيعِ نِطَاقِ التَّعْلِيمِ وَالدَّعْوَةِ،
            مِنْ خِلَالِ الْمَوَاقِعِ الْإِلِكْتِرُونِيَّةِ، وَالْمُحْتَوَى الرَّقْمِيِّ،
            وَخِدْمَةِ الْمُجْتَمَعِ.
          </p>
          <div class="skills">
            <span class="skill">📖 الْقُرْآنُ</span>
            <span class="skill">🕌 الدَّعْوَةُ</span>
            <span class="skill">📚 الدِّرَاسَاتُ الْإِسْلَامِيَّةُ</span>
            <span class="skill">💻 هَنْدَسَةُ الْبَرْمَجِيَّاتِ</span>
            <span class="skill">🌐 تَطْوِيرُ الْوَيْبِ</span>
            <span class="skill">🎨 التَّصْمِيمُ الرَّقْمِيُّ</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== MARKAZA ===== -->
  <section id="markaza">
    <div class="container">
      <div class="markaza-box">
        <div class="markaza-icon">🌿✨🕌📖</div>
        <h2>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</h2>
        <div class="arabic markaza-arabic">
          مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ<br>لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
        </div>
        <p>
          <strong>“مَنَارَةٌ لِتَعَلُّمِ الْعُلُومِ الشَّرْعِيَّةِ وَالْقُرْآنِ الْكَرِيمِ”</strong>
          <br><br>
          نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ، وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ.
        </p>
      </div>
    </div>
  </section>

  <!-- ===== PROGRAMS ===== -->
  <section id="programs">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">الْبَرَامِجُ التَّعْلِيمِيَّةُ</div>
        <h2>📚 بَرَامِجُنَا</h2>
        <p>بَرَامِجُ مُنَظَّمَةٌ لِبِنَاءِ الْمُسْلِمِ عِلْمِيًّا وَأَخْلَاقِيًّا</p>
      </div>
      <div class="program-grid">
        <div class="program">
          <div class="program-icon">🔤</div>
          <h3>الْقَاعِدَةُ النُّورَانِيَّةُ</h3>
          <p>اَلْمُسْتَوَى التَّمْهِيدِيُّ لِتَعْلِيمِ الْقِرَاءَةِ الصَّحِيحَةِ لِلْحُرُوفِ وَالْكَلِمَاتِ، مُخَصَّصٌ لِلصِّغَارِ وَالْمُبْتَدِئِينَ.</p>
          <span class="duration">🌱 لِلْمُبْتَدِئِينَ</span>
        </div>
        <div class="program">
          <div class="program-icon">📖</div>
          <h3>التِّلَاوَةُ وَالتَّجْوِيدُ</h3>
          <p>تَعَلُّمُ مَخَارِجِ الْحُرُوفِ، وَالصِّفَاتِ، وَأَحْكَامِ التَّجْوِيدِ (النُّونِ السَّاكِنَةِ، الْمُدُودِ، وَغَيْرِهَا).</p>
          <span class="duration">⏳ 3 أَشْهُرٍ</span>
        </div>
        <div class="program">
          <div class="program-icon">🌙</div>
          <h3>السِّيرَةُ النَّبَوِيَّةُ</h3>
          <p>دِرَاسَةُ حَيَاةِ النَّبِيِّ ﷺ، وَأَخْلَاقِهِ، وَغَزَوَاتِهِ، وَمَوَاقِفِهِ التَّرْبَوِيَّةِ.</p>
          <span class="duration">⏳ شَهْرَانِ</span>
        </div>
        <div class="program">
          <div class="program-icon">🕌</div>
          <h3>الْفِقْهُ وَالْأَحْكَامُ</h3>
          <p>أَحْكَامُ الطَّهَارَةِ، وَالصَّلَاةِ، وَالزَّكَاةِ، وَالصِّيَامِ، وَالْحَجِّ، وَالْمُعَامِلَاتِ.</p>
          <span class="duration">⏳ 3 أَشْهُرٍ</span>
        </div>
        <div class="program">
          <div class="program-icon">☝️</div>
          <h3>الْعَقِيدَةُ الصَّحِيحَةُ</h3>
          <p>دِرَاسَةُ التَّوْحِيدِ، وَأُصُولِ الْإِيمَانِ، وَأَسْمَاءِ اللَّهِ وَصِفَاتِهِ، وَمَا يُضَادُّ ذَلِكَ مِنَ الشِّرْكِ.</p>
          <span class="duration">⏳ شَهْرَانِ</span>
        </div>
        <div class="program">
          <div class="program-icon">✨</div>
          <h3>الْبَرْنَامَجُ الشَّامِلُ</h3>
          <p>مَنْهَجٌ مُتَكَامِلٌ يَضُمُّ الْقُرْآنَ، وَالتَّجْوِيدَ، وَالْعَقِيدَةَ، وَالْفِقْهَ، وَالسِّيرَةَ فِي فَتْرَةٍ زَمَنِيَّةٍ مُحَدَّدَةٍ.</p>
          <span class="duration">⏳ 3 أَشْهُرٍ</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== CURRICULUM ===== -->
  <section class="curriculum" id="curriculum">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">الْمَنْهَجُ</div>
        <h2>📚 الْكُتُبُ وَالْمُقَرَّرَاتُ</h2>
        <p>اَلْكُتُبُ وَالْمَوَادُّ التَّعْلِيمِيَّةُ الْمُعْتَمَدَةُ</p>
      </div>
      <div class="book-grid">
        <div class="book">
          <div class="book-icon">🔤</div>
          <div>
            <h3>الْقَاعِدَةُ النُّورَانِيَّةُ</h3>
            <p>أَسَاسُ قِرَاءَةِ الْقُرْآنِ وَاللُّغَةِ الْعَرَبِيَّةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">📖</div>
          <div>
            <h3>التِّلَاوَةُ وَالتَّجْوِيدُ</h3>
            <p>مَخَارِجُ الْحُرُوفِ، الصِّفَاتُ، وَأَحْكَامُ التَّجْوِيدِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">☝️</div>
          <div>
            <h3>اَلْأُصُولُ الثَّلَاثَةُ</h3>
            <p>أُصُولُ الْعَقِيدَةِ وَالتَّوْحِيدِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">🕌</div>
          <div>
            <h3>كِتَابُ التَّوْحِيدِ وَالْعَقِيدَةُ الْوَاسِطِيَّةُ</h3>
            <p>شُرُوحٌ مُيَسَّرَةٌ لِلْعَقِيدَةِ الصَّحِيحَةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">📕</div>
          <div>
            <h3>خُذْ عَقِيدَتَكَ</h3>
            <p>مُقَدِّمَةٌ مُبَسَّطَةٌ لِلْعَقِيدَةِ الْإِسْلَامِيَّةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">📚</div>
          <div>
            <h3>اَلْأَرْبَعُونَ النَّوَوِيَّةُ وَبُلُوغُ الْمَرَامِ</h3>
            <p>مَجْمُوعَاتٌ حَدِيثِيَّةٌ مَعَ شُرُوحٍ مُخْتَصَرَةٍ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">⚖️</div>
          <div>
            <h3>اَلْأَحْكَامُ الْفِقْهِيَّةُ</h3>
            <p>أَحْكَامُ الْعِبَادَاتِ وَالْمُعَامَلَاتِ الْيَوْمِيَّةِ.</p>
          </div>
        </div>
        <div class="book">
          <div class="book-icon">🌙</div>
          <div>
            <h3>السِّيرَةُ النَّبَوِيَّةُ</h3>
            <p>دُرُوسٌ وَعِبَرٌ مِنْ حَيَاةِ النَّبِيِّ ﷺ.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== MESSAGE ===== -->
  <section>
    <div class="container">
      <div class="section-head">
        <div class="section-mini">رِسَالَتُنَا</div>
        <h2>🌿 رِسَالَتُنَا</h2>
      </div>
      <div class="message-box">
        <div class="arabic">
          نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،<br>
          وَنُعَرِّفُكَ بِنَبِيِّكَ ﷺ،<br>
          وَنُفَهِّمُكَ دِينَكَ،<br>
          وَنُصَحِّحُ لَكَ عَقِيدَتَكَ.
        </div>
        <p>
          لِتَكُونَ قَارِئًا مُتْقِنًا لِلْقُرْآنِ، مُسْلِمًا صَحِيحَ الْعَقِيدَةِ،
          فَهِمًا لِدِينِكَ، مُتَّبِعًا لِنَبِيِّكَ ﷺ.
        </p>
      </div>
    </div>
  </section>

  <!-- ===== CONTACT ===== -->
  <section id="contact">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">اِتَّصِلْ بِنَا</div>
        <h2>📞 اِتَّصِلْ بِنَا</h2>
        <p>لِلِاسْتِفْسَارِ عَنِ الدَّعْوَةِ، أَوِ التَّعْلِيمِ، أَوِ التَّعَاوُنِ التِّقْنِيِّ</p>
      </div>
      <div class="contact-grid">
        <a href="tel:0915455051" class="contact-card">
          <div class="contact-icon">📞</div>
          <h3>اَلْهَاتِفُ</h3>
          <p>0915455051</p>
        </a>
        <a href="https://wa.me/251915455051" target="_blank" class="contact-card">
          <div class="contact-icon">💬</div>
          <h3>وَاتْسَابْ</h3>
          <p>0915455051</p>
        </a>
        <a href="mailto:Ferhanshaamil@gmail.com" class="contact-card">
          <div class="contact-icon">📧</div>
          <h3>اَلْبَرِيدُ الْإِلِكْتِرُونِيُّ</h3>
          <p>Ferhanshaamil@gmail.com</p>
        </a>
      </div>
    </div>
  </section>

  <!-- ===== CTA ===== -->
  <section class="cta">
    <div class="container">
      <div class="arabic">خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ</div>
      <h2>اَلْقُرْآنُ يَنْتَظِرُكَ! 📖</h2>
      <p>
        اَلْمَكَانُ هُنَا. 🕌<br>
        اَلْفُرْصَةُ الْآنَ. ⏰<br>
        الرِّحْلَةُ تَبْدَأُ الْيَوْمَ. 🚀
      </p>
      <a href="#contact" class="btn btn-primary">📝 تَوَاصَلْ مَعَنَا</a>
    </div>
  </section>

  <!-- ===== FOOTER ===== -->
  <footer>
    <div class="container">
      <div class="footer-logo">🌿✨🕌📖</div>
      <p><strong>فَرْحَانُ شَامِلُ عَبْدِ الْغَفُورِ</strong></p>
      <p>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</p>
      <p>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</p>
      <p>© 2026 فَرْحَانُ شَامِلٌ. جَمِيعُ الْحُقُوقِ مَحْفُوظَةٌ.</p>
    </div>
  </footer>

  <!-- ===== FLOATING WHATSAPP ===== -->
  <a href="https://wa.me/251915455051" target="_blank" class="floating" title="WhatsApp">💬</a>

</body>
</html><!DOCTYPE html>
<html lang="om">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">

<title>Ferhan Shaamil | Markaza Uweysii</title>

<meta name="description"
content="Ferhan Shaamil — Da'ii, Barsiisaa fi Software Engineering Student. Markaza Uweysii Ibnu Aamir.">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  scroll-behavior:smooth
}

:root{
  --bg:#04110c;
  --card:#0a2118;
  --green:#126044;
  --gold:#d9b85c;
  --light:#f5efd9;
  --text:#d4ddd7;
  --muted:#91a29a;
  --border:rgba(217,184,92,.25)
}

body{
  font-family:Arial,sans-serif;
  background:
  radial-gradient(circle at top right,rgba(18,96,68,.25),transparent 35%),
  radial-gradient(circle at bottom left,rgba(217,184,92,.08),transparent 30%),
  var(--bg);
  color:var(--light);
  line-height:1.7
}

a{
  text-decoration:none;
  color:inherit
}

.container{
  width:min(1100px,92%);
  margin:auto
}

/* NAV */

nav{
  position:fixed;
  top:0;
  width:100%;
  z-index:10;
  background:rgba(4,17,12,.88);
  backdrop-filter:blur(15px);
  border-bottom:1px solid var(--border)
}

.nav{
  height:70px;
  display:flex;
  justify-content:space-between;
  align-items:center
}

.logo{
  display:flex;
  align-items:center;
  gap:10px
}

.logo-icon{
  width:42px;
  height:42px;
  display:grid;
  place-items:center;
  border:1px solid var(--gold);
  border-radius:50%
}

.logo strong{
  color:var(--gold);
  font-size:14px
}

.logo small{
  display:block;
  color:var(--muted);
  font-size:9px
}

.links{
  display:flex;
  gap:22px;
  list-style:none;
  font-size:13px
}

.links a:hover{
  color:var(--gold)
}

/* HERO */

.hero{
  min-height:100vh;
  display:flex;
  align-items:center;
  padding:120px 0 70px
}

.hero-grid{
  display:grid;
  grid-template-columns:1.2fr .8fr;
  gap:45px;
  align-items:center
}

.badge{
  display:inline-block;
  padding:6px 13px;
  border:1px solid var(--border);
  border-radius:30px;
  color:var(--gold);
  font-size:11px;
  margin-bottom:18px
}

h1{
  font-size:clamp(45px,8vw,78px);
  line-height:1;
  letter-spacing:-3px
}

h1 span{
  color:var(--gold)
}

.role{
  margin:18px 0 8px;
  font-size:20px;
  color:var(--text)
}

.arabic{
  direction:rtl;
  font-family:"Times New Roman",serif
}

.hero-arabic{
  color:var(--gold);
  font-size:27px;
  margin:12px 0
}

.description{
  color:var(--muted);
  max-width:650px;
  font-size:14px
}

.buttons{
  display:flex;
  gap:12px;
  flex-wrap:wrap;
  margin-top:25px
}

.btn{
  display:inline-block;
  padding:11px 20px;
  border:1px solid var(--gold);
  border-radius:30px;
  font-size:13px;
  font-weight:bold
}

.primary{
  background:linear-gradient(135deg,#f0d989,var(--gold));
  color:#07130d;
  border:none
}

/* CARD */

.hero-card{
  padding:35px;
  text-align:center;
  border:1px solid var(--border);
  border-radius:30px;
  background:linear-gradient(145deg,#103c2b,#071810);
  box-shadow:0 25px 70px rgba(0,0,0,.3)
}

.icon{
  width:130px;
  height:130px;
  margin:auto;
  display:grid;
  place-items:center;
  border:1px solid var(--gold);
  border-radius:50%;
  font-size:60px
}

.hero-card h3{
  color:var(--gold);
  margin:18px 0 5px
}

.hero-card p{
  color:var(--muted);
  font-size:12px
}

/* SECTIONS */

section{
  padding:80px 0
}

.section-title{
  text-align:center;
  margin-bottom:40px
}

.section-title small{
  color:var(--gold);
  letter-spacing:3px;
  font-size:10px
}

.section-title h2{
  font-size:clamp(28px,5vw,42px);
  margin:5px 0
}

.section-title p{
  color:var(--muted);
  font-size:13px
}

/* ABOUT */

.about{
  background:rgba(7,26,18,.55)
}

.about-grid{
  display:grid;
  grid-template-columns:.7fr 1.3fr;
  gap:20px
}

.card{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:25px;
  padding:28px
}

.card h3{
  color:var(--gold);
  margin-bottom:10px
}

.card p{
  color:var(--muted);
  font-size:13px;
  margin-bottom:12px
}

.skills{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  margin-top:18px
}

.skill{
  padding:5px 10px;
  border:1px solid var(--border);
  border-radius:20px;
  color:var(--gold);
  font-size:10px
}

/* MARKAZA */

.markaza{
  text-align:center;
  border:1px solid var(--gold);
  border-radius:30px;
  padding:45px 20px;
  background:
  radial-gradient(circle,rgba(18,96,68,.35),transparent 65%),
  #071b13
}

.markaza .big{
  font-size:45px
}

.markaza h2{
  color:var(--gold);
  font-size:clamp(25px,5vw,43px)
}

.markaza .arabic{
  font-size:23px;
  margin:8px 0 18px
}

.markaza p{
  color:var(--muted);
  max-width:700px;
  margin:auto;
  font-size:13px
}

/* PROGRAMS */

.programs{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:16px
}

.program{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:20px;
  padding:24px;
  transition:.3s
}

.program:hover{
  transform:translateY(-5px);
  border-color:var(--gold)
}

.program .emoji{
  font-size:30px
}

.program h3{
  margin:7px 0;
  font-size:17px
}

.program p{
  color:var(--muted);
  font-size:12px
}

.duration{
  display:inline-block;
  margin-top:12px;
  color:var(--gold);
  font-size:10px;
  border:1px solid var(--border);
  padding:4px 9px;
  border-radius:20px
}

/* MISSION */

.mission{
  text-align:center;
  background:rgba(7,26,18,.55)
}

.quote{
  max-width:850px;
  margin:auto;
  padding:40px 25px;
  border:1px solid var(--border);
  border-radius:25px;
  background:var(--card)
}

.quote .arabic{
  color:var(--gold);
  font-size:24px;
  line-height:1.9
}

.quote p{
  color:var(--muted);
  font-size:13px;
  margin-top:15px
}

/* CONTACT */

.contact{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:16px
}

.contact a{
  text-align:center;
  padding:25px;
  border:1px solid var(--border);
  border-radius:20px;
  background:var(--card)
}

.contact .emoji{
  font-size:30px
}

.contact h3{
  color:var(--gold);
  margin:5px 0
}

.contact p{
  color:var(--muted);
  font-size:12px
}

/* CTA */

.cta{
  text-align:center;
  padding:90px 20px
}

.cta .arabic{
  color:var(--gold);
  font-size:25px
}

.cta h2{
  font-size:clamp(30px,6vw,50px);
  color:var(--gold);
  margin:8px 0
}

.cta p{
  color:var(--muted);
  margin-bottom:20px
}

/* FOOTER */

footer{
  padding:35px 20px;
  text-align:center;
  border-top:1px solid var(--border);
  background:#020906
}

footer strong{
  color:var(--gold)
}

footer p{
  color:var(--muted);
  font-size:10px
}

/* WHATSAPP */

.whatsapp{
  position:fixed;
  right:18px;
  bottom:18px;
  width:53px;
  height:53px;
  display:grid;
  place-items:center;
  border-radius:50%;
  background:#16804f;
  font-size:24px;
  z-index:20
}

/* MOBILE */

@media(max-width:800px){

  .links{
    display:none
  }

  .hero-grid,
  .about-grid{
    grid-template-columns:1fr
  }

  .programs{
    grid-template-columns:repeat(2,1fr)
  }

  .contact{
    grid-template-columns:1fr
  }
}

@media(max-width:520px){

  section{
    padding:60px 0
  }

  .hero{
    padding-top:110px
  }

  .programs{
    grid-template-columns:1fr
  }

  .hero-card{
    padding:25px
  }

  .card{
    padding:23px
  }
}
</style>
</head>

<body>

<!-- NAV -->
<nav>
<div class="container nav">

<a href="#home" class="logo">
<div class="logo-icon">🌿</div>
<div>
<strong>FERHAN SHAAMIL</strong>
<small>مركز أويس بن عامر</small>
</div>
</a>

<ul class="links">
<li><a href="#home">Home</a></li>
<li><a href="#about">About</a></li>
<li><a href="#markaza">Markaza</a></li>
<li><a href="#programs">Programs</a></li>
<li><a href="#contact">Contact</a></li>
</ul>

</div>
</nav>


<!-- HERO -->
<section class="hero" id="home">
<div class="container hero-grid">

<div>

<span class="badge">🌿 OFFICIAL WEBSITE • QUR'AN • EDUCATION</span>

<h1>
FERHAN<br>
<span>SHAAMIL</span>
</h1>

<div class="role">
Da'ii • Barsiisaa • Software Engineering Student
</div>

<div class="arabic hero-arabic">
فرحان شامل عبدالغفور
</div>

<p class="description">
Barsiisaa Markaza Uweysii Ibnu Aamiri,
Da'ii fi barataa Software Engineering.
Kaayyoon koo Qur'aanaa, beekumsa Shari'aa,
tarbiyaa fi teknooloojii walitti fiduudha.
</p>

<div class="buttons">
<a href="#markaza" class="btn primary">🕌 Markazaa Ilaali</a>
<a href="#programs" class="btn">📚 Barnoota</a>
</div>

</div>


<div class="hero-card">

<div class="icon">🕌</div>

<h3>MARKAZA UWEYSII IBNU AAMIR</h3>

<p class="arabic">
مركز أويس بن عامر لدراسة العلوم الشرعية
</p>

<p style="margin-top:15px">
📖 Qur'aana<br>
🕌 علوم شرعية<br>
🌱 Tarbiyaa<br>
💻 Teknooloojii
</p>

</div>

</div>
</section>


<!-- ABOUT -->
<section class="about" id="about">

<div class="container">

<div class="section-title">
<small>ABOUT ME</small>
<h2>👤 Waa'ee Koo</h2>
<p>Barnoota, Da'awaa, Qur'aana fi Teknooloojii.</p>
</div>

<div class="about-grid">

<div class="card">

<h3>Ferhan Shaamil</h3>

<p>
Da'ii • Barsiisaa • Software Engineering Student
</p>

<p>🕌 Barsiisaa Markaza Uweysii Ibnu Aamir</p>
<p>📖 Qur'aanaa fi علوم شرعية</p>
<p>🌱 Tarbiyaa dhalootaa</p>
<p>💻 Software Engineering</p>

</div>

<div class="card">

<h3>🌿 Kaayyoo Koo</h3>

<p>
Qur'aanaa fi beekumsa Shari'aa karaa ammayyaa ta'een
dhalootaaf dabarsuu, akkasumas teknooloojii fayyadamuun
barnoota fi tajaajila hawaasaa babal'isuudha.
</p>

<div class="skills">
<span class="skill">📖 Qur'an</span>
<span class="skill">🕌 Da'wah</span>
<span class="skill">📚 Islamic Studies</span>
<span class="skill">💻 Software Engineering</span>
<span class="skill">🌐 Web Development</span>
</div>

</div>

</div>
</div>
</section>


<!-- MARKAZA -->
<section id="markaza">

<div class="container">

<div class="markaza">

<div class="big">🌿✨🕌📖</div>

<h2>MARKAZA UWEYSII IBNU AAMIR</h2>

<div class="arabic">
مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ
لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
</div>

<p>
<strong>
“Iddoo Beekumsa Shar'iyyaa fi Qur'aana Kabajamaa.”
</strong>
<br><br>
منارة لتعلم العلوم الشرعية والقرآن الكريم
<br><br>
نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،
وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ.
</p>

</div>

</div>
</section>


<!-- PROGRAMS -->
<section id="programs">

<div class="container">

<div class="section-title">
<small>EDUCATION</small>
<h2>📚 Sagantaalee Barnootaa</h2>
<p>Qur'aanaa fi علوم شرعية.</p>
</div>

<div class="programs">

<div class="program">
<div class="emoji">🔤</div>
<h3>Qaacidda Nooraniyyaa</h3>
<p>Bu'uura dubbisa Qur'aanaa fi qubee.</p>
<span class="duration">🌱 Jalqabdootaaf</span>
</div>

<div class="program">
<div class="emoji">📖</div>
<h3>Tilawaa fi Tajwiid</h3>
<p>Qara'a Qur'aanaa fi seera Tajwiidaa.</p>
<span class="duration">⏳ Ji'a 3</span>
</div>

<div class="program">
<div class="emoji">🌙</div>
<h3>Seenaa Nabiyyii ﷺ</h3>
<p>Jireenya Nabiyyii ﷺ fi barnoota isaa.</p>
<span class="duration">⏳ Ji'a 2</span>
</div>

<div class="program">
<div class="emoji">🕌</div>
<h3>Fiqhii fi Ahkaam</h3>
<p>Ahkaama jireenya Muslimaa.</p>
<span class="duration">⏳ Ji'a 3</span>
</div>

<div class="program">
<div class="emoji">☝️</div>
<h3>Aqeedaa Sirrii</h3>
<p>Tawhiida fi bu'uura Aqeedaa.</p>
<span class="duration">⏳ Ji'a 2</span>
</div>

<div class="program">
<div class="emoji">✨</div>
<h3>Sagantaa Guutuu</h3>
<p>Tilawaa, Tajwiid, Aqeedaa, Fiqhii fi Seenaa.</p>
<span class="duration">⏳ Ji'a 3</span>
</div>

</div>
</div>
</section>


<!-- MISSION -->
<section class="mission">

<div class="container">

<div class="section-title">
<small>OUR MISSION</small>
<h2>🌿 Ergaa Keenya</h2>
</div>

<div class="quote">

<div class="arabic">
نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،
وَنُعَرِّفُكَ بِنَبِيِّكَ ﷺ،
وَنُفَهِّمُكَ دِينَكَ،
وَنُصَحِّحُ لَكَ عَقِيدَتَكَ.
</div>

<p>
Akka ati Qur'aana sirriitti qaraatu,
Diinii kee hubattu, Aqeedaa sirrii qabaattu
fi Nabiyyii kee ﷺ hordoftuuf si qopheessina.
</p>

</div>

</div>
</section>


<!-- CONTACT -->
<section id="contact">

<div class="container">

<div class="section-title">
<small>CONTACT</small>
<h2>📞 Nu Qunnami</h2>
<p>Odeeffannoo dabalataaf nu qunnami.</p>
</div>

<div class="contact">

<a href="tel:0915455051">
<div class="emoji">📞</div>
<h3>Bilbila</h3>
<p>0915455051</p>
</a>

<a href="https://wa.me/251915455051" target="_blank">
<div class="emoji">💬</div>
<h3>WhatsApp</h3>
<p>0915455051</p>
</a>

<a href="mailto:Ferhanshaamil@gmail.com">
<div class="emoji">📧</div>
<h3>Email</h3>
<p>Ferhanshaamil@gmail.com</p>
</a>

</div>

</div>
</section>


<!-- CTA -->
<section class="cta">

<div class="container">

<div class="arabic">
خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ
</div>

<h2>Qur'aanni Si Eeggata! 📖</h2>

<p>
Bakki as jira. 🕌 Carraan amma jira. ⏰
Imalli barnootaa har'a jalqaba. 🚀
</p>

<a href="#contact" class="btn primary">
📝 Nu Qunnami
</a>

</div>
</section>


<!-- FOOTER -->
<footer>

<strong>FERHAN SHAAMIL ABDULGAFUR</strong>

<p>Markaza Uweysii Ibnu Aamir</p>

<p class="arabic">
مركز أويس بن عامر لدراسة العلوم الشرعية
</p>

<p>© 2026 Ferhan Shaamil. All Rights Reserved.</p>

</footer>


<!-- WHATSAPP -->
<a
href="https://wa.me/251915455051"
target="_blank"
class="whatsapp"
title="WhatsApp">
💬
</a>

</body>
</html><!DOCTYPE html>
<html lang="om" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ferhan Shaamil | Markaza Uweysii Ibnu Aamir</title>

  <meta name="description"
    content="Ferhan Shaamil — Da'ii, Barsiisaa Qur'aanaa fi Barnoota Shari'aa. Markaza Uweysii Ibnu Aamir.">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --green: #063d2c;
      --green2: #0b5d42;
      --dark: #031f17;
      --gold: #d6ad4b;
      --gold2: #f1d477;
      --cream: #fffaf0;
      --white: #ffffff;
      --text: #eaf5ef;
      --muted: #b9d0c5;
      --card: rgba(255,255,255,.075);
      --border: rgba(214,173,75,.28);
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background:
        radial-gradient(circle at 10% 10%, rgba(214,173,75,.15), transparent 25%),
        radial-gradient(circle at 90% 30%, rgba(11,93,66,.35), transparent 30%),
        linear-gradient(135deg, #021a13, #063d2c 45%, #021a13);
      color: var(--text);
      line-height: 1.8;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1150px, 92%);
      margin: auto;
    }

    /* NAVBAR */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      background: rgba(2,26,19,.9);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid var(--border);
    }

    .nav-inner {
      min-height: 72px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
    }

    .logo {
      color: var(--gold2);
      font-weight: 900;
      font-size: 20px;
      letter-spacing: .5px;
    }

    .nav-links {
      display: flex;
      gap: 22px;
      list-style: none;
      font-size: 14px;
    }

    .nav-links a:hover {
      color: var(--gold2);
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 120px 0 70px;
      position: relative;
    }

    .hero::before {
      content: "☪";
      position: absolute;
      font-size: 360px;
      opacity: .025;
      right: -70px;
      top: 100px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.25fr .75fr;
      gap: 45px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      border: 1px solid var(--border);
      background: rgba(214,173,75,.08);
      color: var(--gold2);
      padding: 7px 15px;
      border-radius: 100px;
      margin-bottom: 20px;
      font-size: 13px;
    }

    h1 {
      font-size: clamp(48px, 8vw, 90px);
      line-height: 1;
      color: var(--white);
      margin-bottom: 18px;
      letter-spacing: -3px;
    }

    .hero h2 {
      color: var(--gold2);
      font-size: clamp(22px, 4vw, 35px);
      margin-bottom: 15px;
    }

    .arabic {
      direction: rtl;
      font-family: "Times New Roman", serif;
      font-size: 25px;
      color: #f4df9b;
      margin: 15px 0;
    }

    .hero p {
      max-width: 720px;
      color: var(--muted);
      font-size: 18px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      margin-top: 28px;
    }

    .btn {
      padding: 13px 22px;
      border-radius: 12px;
      border: 1px solid var(--border);
      font-weight: bold;
      transition: .3s;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold), var(--gold2));
      color: #06271c;
    }

    .btn-outline {
      background: rgba(255,255,255,.05);
    }

    .btn:hover {
      transform: translateY(-3px);
    }

    .hero-card {
      background: linear-gradient(145deg, rgba(214,173,75,.16), rgba(255,255,255,.05));
      border: 1px solid var(--border);
      padding: 35px;
      border-radius: 28px;
      text-align: center;
      box-shadow: 0 25px 70px rgba(0,0,0,.25);
    }

    .hero-card .icon {
      font-size: 70px;
      margin-bottom: 15px;
    }

    .hero-card h3 {
      color: var(--gold2);
      font-size: 23px;
    }

    /* SECTIONS */

    section {
      padding: 90px 0;
    }

    .section-title {
      text-align: center;
      margin-bottom: 50px;
    }

    .section-title span {
      color: var(--gold2);
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 3px;
    }

    .section-title h2 {
      font-size: clamp(30px, 5vw, 48px);
      color: var(--white);
      margin-top: 7px;
    }

    .section-title p {
      color: var(--muted);
      max-width: 700px;
      margin: 10px auto;
    }

    /* CARDS */

    .grid {
      display: grid;
      grid-template-columns: repeat(3,1fr);
      gap: 20px;
    }

    .card {
      background: var(--card);
      border: 1px solid rgba(255,255,255,.09);
      border-radius: 20px;
      padding: 25px;
      transition: .3s;
    }

    .card:hover {
      transform: translateY(-7px);
      border-color: var(--gold);
      background: rgba(255,255,255,.1);
    }

    .card-icon {
      font-size: 35px;
      margin-bottom: 10px;
    }

    .card h3 {
      color: var(--gold2);
      margin-bottom: 8px;
    }

    .card p {
      color: var(--muted);
    }

    /* ABOUT */

    .about {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 30px;
      align-items: stretch;
    }

    .profile-box {
      background: linear-gradient(145deg, #0a6044, #03251b);
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 40px;
      text-align: center;
    }

    .profile-circle {
      width: 130px;
      height: 130px;
      border-radius: 50%;
      margin: auto auto 20px;
      display: grid;
      place-items: center;
      background: linear-gradient(145deg, var(--gold), var(--gold2));
      color: #073b2b;
      font-size: 42px;
      font-weight: 900;
    }

    .profile-box h3 {
      font-size: 28px;
      color: var(--white);
    }

    .profile-box p {
      color: var(--gold2);
    }

    /* MARKAZA */

    .markaza-box {
      background:
        linear-gradient(rgba(3,31,23,.9), rgba(3,31,23,.96)),
        radial-gradient(circle, #0c684a, #031f17);
      border: 1px solid var(--border);
      border-radius: 30px;
      padding: 50px 30px;
      text-align: center;
    }

    .markaza-logo {
      font-size: 65px;
    }

    .markaza-box h2 {
      color: var(--gold2);
      font-size: clamp(28px,5vw,48px);
      margin: 10px 0;
    }

    .markaza-box .arabic {
      font-size: 28px;
    }

    .quote {
      margin: 25px auto;
      padding: 22px;
      max-width: 850px;
      border-left: 4px solid var(--gold);
      border-right: 4px solid var(--gold);
      background: rgba(214,173,75,.06);
      border-radius: 15px;
      color: var(--cream);
      font-size: 18px;
    }

    /* PROGRAMS */

    .program {
      position: relative;
      overflow: hidden;
    }

    .program:nth-child(1) { border-top: 4px solid #8ed8ff; }
    .program:nth-child(2) { border-top: 4px solid #75c9ff; }
    .program:nth-child(3) { border-top: 4px solid #c8a2ff; }
    .program:nth-child(4) { border-top: 4px solid #f2cc65; }
    .program:nth-child(5) { border-top: 4px solid #7be495; }
    .program:nth-child(6) { border-top: 4px solid #ffad70; }

    .duration {
      display: inline-block;
      margin-top: 14px;
      background: rgba(255,255,255,.08);
      padding: 5px 11px;
      border-radius: 100px;
      font-size: 13px;
      color: var(--gold2);
    }

    /* TABLE */

    .table-wrap {
      overflow-x: auto;
      border-radius: 18px;
      border: 1px solid var(--border);
    }

    table {
      width: 100%;
      border-collapse: collapse;
      min-width: 650px;
      background: rgba(255,255,255,.04);
    }

    th, td {
      padding: 15px;
      text-align: right;
      border-bottom: 1px solid rgba(255,255,255,.08);
    }

    th {
      background: rgba(214,173,75,.12);
      color: var(--gold2);
    }

    td {
      color: var(--muted);
    }

    /* FORM */

    .form-box {
      max-width: 850px;
      margin: auto;
      background: var(--card);
      padding: 30px;
      border-radius: 25px;
      border: 1px solid var(--border);
    }

    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 15px;
    }

    input, select, textarea {
      width: 100%;
      padding: 14px;
      border-radius: 12px;
      border: 1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.2);
      color: white;
      outline: none;
    }

    textarea {
      min-height: 130px;
      resize: vertical;
    }

    input:focus, select:focus, textarea:focus {
      border-color: var(--gold);
    }

    .full {
      grid-column: 1 / -1;
    }

    /* SOCIAL */

    .social-card {
      border-left: 4px solid var(--gold);
    }

    .social-card h3 {
      color: var(--gold2);
    }

    /* CONTACT */

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(3,1fr);
      gap: 20px;
    }

    .contact-card {
      text-align: center;
    }

    .contact-card a {
      color: var(--gold2);
      word-break: break-word;
    }

    /* CTA */

    .cta {
      text-align: center;
      background:
        linear-gradient(rgba(4,50,36,.95), rgba(4,50,36,.95)),
        radial-gradient(circle, #11694c, #031f17);
      border: 1px solid var(--border);
      border-radius: 30px;
      padding: 60px 25px;
    }

    .cta h2 {
      color: var(--gold2);
      font-size: clamp(30px,5vw,55px);
    }

    .cta .big {
      font-size: 24px;
      margin: 15px 0;
    }

    /* FOOTER */

    footer {
      border-top: 1px solid var(--border);
      padding: 45px 0;
      text-align: center;
      color: var(--muted);
    }

    footer strong {
      color: var(--gold2);
    }

    /* WHATSAPP */

    .whatsapp {
      position: fixed;
      bottom: 20px;
      right: 20px;
      width: 58px;
      height: 58px;
      border-radius: 50%;
      background: #25d366;
      display: grid;
      place-items: center;
      font-size: 28px;
      z-index: 999;
      box-shadow: 0 10px 30px rgba(0,0,0,.4);
    }

    /* MOBILE */

    @media(max-width: 850px) {
      .nav-links {
        display: none;
      }

      .hero-grid,
      .about {
        grid-template-columns: 1fr;
      }

      .grid {
        grid-template-columns: 1fr 1fr;
      }

      .contact-grid {
        grid-template-columns: 1fr;
      }
    }

    @media(max-width: 600px) {
      section {
        padding: 65px 0;
      }

      .grid {
        grid-template-columns: 1fr;
      }

      .form-grid {
        grid-template-columns: 1fr;
      }

      h1 {
        font-size: 50px;
      }

      .hero p {
        font-size: 16px;
      }

      .hero-card {
        padding: 25px;
      }

      .profile-box {
        padding: 30px 20px;
      }
    }
  </style>
</head>

<body>

<!-- ================= NAVBAR ================= -->

<nav>
  <div class="container nav-inner">
    <a href="#home" class="logo">🌿 Ferhan Shaamil</a>

    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#markaza">Markaza</a></li>
      <li><a href="#programs">Programs</a></li>
      <li><a href="#curriculum">Curriculum</a></li>
      <li><a href="#register">Galmee</a></li>
      <li><a href="#contact">Quunnamtii</a></li>
    </ul>
  </div>
</nav>


<!-- ================= HERO ================= -->

<header class="hero" id="home">
  <div class="container hero-grid">

    <div>
      <span class="badge">🌿✨ Qur'aana • Barnoota • Teknooloojii</span>

      <h1>FERHAN<br>SHAAMIL</h1>

      <h2>داعية ومعلّم للقرآن والعلوم الشرعية</h2>

      <div class="arabic">
        فرحان شامل عبدالغفور
      </div>

      <p>
        Barsiisaa Markaza Uweysii Ibnu Aamir,
        Da'ii fi nama dhaloota Qur'aanaa fi beekumsa
        Shari'aa irratti kakaasu.
      </p>

      <div class="buttons">
        <a class="btn btn-primary" href="#about">👤 About Me</a>
        <a class="btn btn-outline" href="#markaza">🕌 Markaza Uweysii</a>
      </div>
    </div>

    <div class="hero-card">
      <div class="icon">🕌📖🌿</div>

      <h3>Markaza Uweysii Ibnu Aamir</h3>

      <div class="arabic">
        مركز أُوَيْس بن عامر لدراسة العلوم الشرعية
      </div>

      <p>
        Iddoo Beekumsa Shar'iyyaa Fi Qur'aana Kabajamaa
      </p>

      <p>
        منارة لتعلم العلوم الشرعية والقرآن الكريم
      </p>
    </div>

  </div>
</header>


<!-- ================= ABOUT ================= -->

<section id="about">
  <div class="container">

    <div class="section-title">
      <span>About Me</span>
      <h2>Waa'ee Kiyya</h2>
      <p>
        Daandii Qur'aanaa, Barnoota Shari'aa Fi Teknooloojii Walitti Qabu.
      </p>
    </div>

    <div class="about">

      <div class="profile-box">
        <div class="profile-circle">FS</div>

        <h3>Ferhan Shaamil</h3>

        <p>داعية ومعلّم للقرآن والعلوم الشرعية</p>

        <div class="arabic">
          فرحان شامل عبدالغفور
        </div>

        <p>
          Barsiisaa • Da'ii • Software Engineering Student
        </p>
      </div>

      <div class="card">
        <h3>🌿 Ani Eenyu?</h3>

        <p>
          Ani Ferhan Shaamil, Barsiisaa Markaza Uweysii Ibnu Aamir,
          Da'ii fi barataa Software Engineering ti.
        </p>

        <br>

        <p>
          Kaayyoon Kiyya Qur'aana, Barnoota Shari'aa,
          Tarbiyaa Fi Teknooloojii Ammayyaa Walitti Fiduun
          Dhaloota Beekumsa Qabu Ijaaruudha.
        </p>

        <br>

        <h3>💎 Dandeettiilee</h3>

        <p>
          📖 Qur'aana • 🕌 Da'waa • 📚 Barnoota Islaamaa •
          💻 Software Engineering • 🌐 Web Development •
          🎨 Digital Design
        </p>
      </div>

    </div>
  </div>
</section>


<!-- ================= MARKAZA ================= -->

<section id="markaza">
  <div class="container">

    <div class="markaza-box">

      <div class="markaza-logo">🌿✨🕌📖</div>

      <h2>Markaza Uweysii Ibnu Aamir</h2>

      <div class="arabic">
        مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
      </div>

      <p>
        Iddoo Beekumsa Shar'iyyaa Fi Qur'aana Kabajamaa
      </p>

      <div class="arabic">
        منارة لتعلم العلوم الشرعية والقرآن الكريم
      </div>

      <div class="quote">
        "نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،
        وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ"
      </div>

      <p>
        Nuti Qur'aana Akkuma Bu'etti Si Barsiinna,
        Nabiyyii Kee Si Beeksisna, Diinii Kee Si Hubachiifna,
        Aqiidaa Keessan Sirreessina.
      </p>

    </div>

  </div>
</section>


<!-- ================= PROGRAMS ================= -->

<section id="programs">
  <div class="container">

    <div class="section-title">
      <span>Barnoota Fi Sagantaalee</span>
      <h2>📚 Sagantaalee Kennaman</h2>
      <p>
        Barnoota Bu'uuraa Irraa Kaasee Hanga Sadarkaa Ol'aanaatti.
      </p>
    </div>

    <div class="grid">

      <div class="card program">
        <div class="card-icon">🔤</div>
        <h3>Qaacidda Nooraniyyaa</h3>
        <p>
          Jalqabdoota Fi Ijoollee Qur'aana Sirriitti Dubbisuuf
          Bu'uura Barnootaa.
        </p>
        <span class="duration">🌱 Jalqabaaf</span>
      </div>

      <div class="card program">
        <div class="card-icon">📖</div>
        <h3>Tilawaa Fi Tajwiid</h3>
        <p>
          Qur'aana Sirriitti Qara'uu, Seera Tajwiidaa Hubachuu
          Fi Sagalee Bareedaan Tilaa'uu.
        </p>
        <span class="duration">⏳ Ji'a 3</span>
      </div>

      <div class="card program">
        <div class="card-icon">🌙</div>
        <h3>Seenaa Nabiyyii ﷺ</h3>
        <p>
          Seenaa Nabiyyii ﷺ, Akhlaaqa Isaa Fi Tarbiyaa
          Isarraa Barachuu.
        </p>
        <span class="duration">⏳ Ji'a 2</span>
      </div>

      <div class="card program">
        <div class="card-icon">🕌</div>
        <h3>Fiqhii Fi Ahkaam</h3>
        <p>
          Ahkaama Diinii Fi Fiqhii Bu'uuraa Haala Salphaa
          Ta'een Barachuu.
        </p>
        <span class="duration">⏳ Ji'a 3</span>
      </div>

      <div class="card program">
        <div class="card-icon">☝️</div>
        <h3>Aqiidaa Sirrii</h3>
        <p>
          Tawhiida, Aqiidaa Sirrii Fi Bu'uura Amantii Islaamaa
          Barachuu.
        </p>
        <span class="duration">⏳ Ji'a 2</span>
      </div>

      <div class="card program">
        <div class="card-icon">✨</div>
        <h3>Sagantaa Guutuu</h3>
        <p>
          Tilawaa, Tajwiid, Aqiidaa, Fiqhii Fi Seenaa Nabiyyii
          Walitti Qabu.
        </p>
        <span class="duration">⏳ Ji'a 3</span>
      </div>

    </div>
  </div>
</section>


<!-- ================= CURRICULUM ================= -->

<section id="curriculum">
  <div class="container">

    <div class="section-title">
      <span>Books & Lessons</span>
      <h2>📚 Kitaabota Fi Barnoota</h2>
    </div>

    <div class="grid">

      <div class="card">
        <h3>📖 Qur'aana Fi Bu'uuraa</h3>
        <p>✨ Al-Qaida An-Nooraniyya — القاعدة النورانية</p>
        <p>✨ Tajwiid Fi Tilawaa — التجويد والتلاوة</p>
      </div>

      <div class="card">
        <h3>☝️ Aqiidaa Fi Hadiisa</h3>
        <p>✨ Al-Usulu Salaasa — الأصول الثلاثة</p>
        <p>✨ Kitabu Tawhiid — كتاب التوحيد</p>
        <p>✨ Aqiidaa Wasixiyyaa — العقيدة الواسطية</p>
        <p>✨ Khuz Aqeedaa Taka — خذ عقيدتك</p>
        <p>✨ Arba'een Fi Bulughul Maraam</p>
      </div>

      <div class="card">
        <h3>🌿 Fiqhii Fi Seenaa</h3>
        <p>✨ Ahkaama Fiqhii — الأحكام الفقهية</p>
        <p>✨ Seenaa Nabiyyii ﷺ — السيرة النبوية</p>
        <p>✨ Seenaa Fi Tarbiyaa Nabiyyii ﷺ</p>
      </div>

    </div>

  </div>
</section>


<!-- ================= DURATIONS ================= -->

<section>
  <div class="container">

    <div class="section-title">
      <span>⏳ Sagantaalee</span>
      <h2>⏳ Yeroo Barnootaa</h2>
    </div>

    <div class="table-wrap">

      <table>
        <thead>
          <tr>
            <th>📚 Sagantaa</th>
            <th>⏳ Yeroo</th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td>📖 Tilawaa Fi Tajwiid</td>
            <td>Ji'a 3</td>
          </tr>

          <tr>
            <td>🌙 Seenaa Nabiyyii ﷺ</td>
            <td>Ji'a 2</td>
          </tr>

          <tr>
            <td>🕌 Fiqhii</td>
            <td>Ji'a 3</td>
          </tr>

          <tr>
            <td>☝️ Aqiidaa</td>
            <td>Ji'a 2</td>
          </tr>

          <tr>
            <td>✨ Sagantaa Guutuu</td>
            <td>Ji'a 3</td>
          </tr>
        </tbody>
      </table>

    </div>

  </div>
</section>


<!-- ================= MONTHLY PLAN ================= -->

<section>
  <div class="container">

    <div class="section-title">
      <span>Monthly Intensive Program</span>
      <h2>📅 Karoora Barnootaa Ji'aa</h2>
      <p>
        Karoora Barnootaa Bu'uuraa, Tajwiidaa, Aqiidaa Fi Qorannoo.
      </p>
    </div>

    <div class="grid">

      <div class="card">
        <h3>🟢 Torban 1 — Bu'uura</h3>
        <p>🔤 Qaacidda Nooraniyyaa — Qubee</p>
        <p>🔤 Fatha, Kasra, Dhamma</p>
        <p>🔤 Tanwiin Fi Sukuun</p>
        <p>🔤 Shaddaa Fi Liin</p>
      </div>

      <div class="card">
        <h3>🔵 Torban 2 — Tajwiid</h3>
        <p>📖 Nuun Saakina Fi Tanwiin</p>
        <p>📖 Izhaar Fi Idghaam</p>
        <p>📖 Iqlaab Fi Ikhfaa</p>
        <p>📖 Ahkaama Miim Saakina</p>
        <p>📖 Ghunnah</p>
      </div>

      <div class="card">
        <h3>🟣 Torban 3 — Madd Fi Aqiidaa</h3>
        <p>📖 Madd Tabi'ii</p>
        <p>📖 Madd Muttasil</p>
        <p>📖 Madd Munfasil</p>
        <p>☝️ Tawhiida Allah</p>
        <p>📖 Suuraa Al-Ikhlaas Fi Al-Faatiha</p>
      </div>

      <div class="card">
        <h3>🟡 Torban 4 — Qorannoo</h3>
        <p>🔤 Irra Deebii Nooraniyyaa</p>
        <p>📖 Irra Deebii Nuun Fi Miim</p>
        <p>☝️ Irra Deebii Madd Fi Aqiidaa</p>
        <p>📝 Qormaata Xumuraa</p>
        <p>🏆 Kabajaa Barattootaa</p>
      </div>

    </div>

  </div>
</section>


<!-- ================= ONLINE ================= -->

<section>
  <div class="container">

    <div class="section-title">
      <span>Online Learning</span>
      <h2>💻 Barnoota Fageenyaa</h2>
    </div>

    <div class="grid">

      <div class="card">
        <div class="card-icon">📱</div>
        <h3>WhatsApp</h3>
        <p>
          Barnoota, Odeeffannoo Fi Qajeelfama Barattootaaf.
        </p>
      </div>

      <div class="card">
        <div class="card-icon">✈️</div>
        <h3>Telegram</h3>
        <p>
          Kitaabota, Sagantaalee Fi Qophii Barnootaa.
        </p>
      </div>

      <div class="card">
        <div class="card-icon">📞</div>
        <h3>IMO</h3>
        <p>
          Walqunnamtii Barnootaa Fi Marii Barattootaa.
        </p>
      </div>

    </div>

  </div>
</section>


<!-- ================= REGISTRATION ================= -->

<section id="register">
  <div class="container">

    <div class="section-title">
      <span>Registration</span>
      <h2>📝 Galmee Barataa Haaraa</h2>

      <p>
        استمارة التسجيل في برامج العلوم الشرعية
      </p>

      <p>
        "نُعلّمك القرآن، ونُعرّفك نبيّك،
        انضم إلينا في رحلة بناء الجيل القرآني المتقن."
      </p>
    </div>

    <div class="form-box">

      <form onsubmit="submitForm(event)">

        <div class="form-grid">

          <input type="text"
            placeholder="👤 Maqaa Guutuu / الاسم الكامل"
            required>

          <input type="number"
            placeholder="🎂 Umurii / السن"
            required>

          <select required>
            <option value="">⚥ Saala / الجنس</option>
            <option>Dhiira / ذكر</option>
            <option>Dhalaa / أنثى</option>
          </select>

          <input type="text"
            placeholder="📍 Teessoo / العنوان">

          <input type="tel"
            placeholder="📞 Lakkoofsa Bilbilaa / رقم الهاتف"
            required>

          <input type="tel"
            placeholder="📱 WhatsApp">

          <input class="full"
            type="tel"
            placeholder="👨‍👩‍👦 Lakkoofsa Guddisaa — Ijoollee Qofa">

          <select class="full" required>
            <option value="">📖 Sadarkaa Qur'aanaa</option>
            <option>Hin Dubbisu — Jalqabaa</option>
            <option>Nan Dubbisa Garuu Na Rakkisa</option>
            <option>Sirriittan Dubbisa — Tajwiidaan Sirreeffachuu Barbaada</option>
            <option>Juzuu'ota Muraasa Haffazee</option>
          </select>

          <select class="full" required>
            <option value="">📚 Sagantaa Barbaaddu Filadhu</option>
            <option>🔤 Qaacidda Nooraniyyaa</option>
            <option>📖 Tilawaa Fi Tajwiid — Ji'a 3</option>
            <option>🌙 Seenaa Nabiyyii ﷺ — Ji'a 2</option>
            <option>🕌 Fiqhii Fi Ahkaam — Ji'a 3</option>
            <option>☝️ Aqiidaa Sirrii — Ji'a 2</option>
            <option>✨ Sagantaa Guutuu — Ji'a 3</option>
          </select>

          <select class="full">
            <option value="">⏰ Yeroo Barnootaa Filadhu</option>
            <option>☀️ Ganama</option>
            <option>🌤️ Waaree Booda</option>
            <option>🌙 Galgala</option>
          </select>

          <textarea class="full"
            placeholder="💬 Yaada Yookaan Gaaffii Dabalataa"></textarea>

          <button class="btn btn-primary full" type="submit">
            🚀 Galmee Ergi
          </button>

        </div>

      </form>

    </div>

  </div>
</section>


<!-- ================= SOCIAL POSTS ================= -->

<section>
  <div class="container">

    <div class="section-title">
      <span>Social Media</span>
      <h2>📢 Beeksisa Miidiyaa Hawaasaa</h2>
    </div>

    <div class="grid">

      <div class="card social-card">
        <h3>🌿 Beeksisa Waliigalaa</h3>

        <p>
          Oduu Gammachiisaa! Galmeen Markaza Uweysii Ibnu Aamir
          Jalqabeera! 🕌📖
        </p>

        <br>

        <p>
          Qur'aana Kabajamaa Akkuma Bu'etti Barachuu,
          Diinii Kee Hubachuu Fi Aqiidaa Kee Sirreessuu Ni Feetaa?
        </p>

        <br>

        <p>
          📞 0915455051
        </p>
      </div>


      <div class="card social-card">
        <h3>🌟 Sagantaa Guutuu</h3>

        <p>
          Lakkaa'i Siif, Muslima Aqiidaa Sirrii Qabu Ta'i.
          Markaza Uweysii Ibnu Aamir Keessatti
          Dubbisuu Qofa Si Hin Barsifnu.
        </p>

        <br>

        <p>
          Dhaloota Beekumsa Qabu Ijaaruuf Si Wajjin Hojjenna.
        </p>
      </div>


      <div class="card social-card">
        <h3>📖 Qur'aanni Si Eeggata!</h3>

        <p>
          🌿 Qur'aanni Si Eeggata!
        </p>

        <p>
          🕌 Bakki Asitti Jira!
        </p>

        <p>
          ⏰ Carraan Amma Jira!
        </p>

        <p>
          🚀 Imalli Barnootaa Amma Jalqaba!
        </p>

        <br>

        <p>
          Nuti Si Eegganna... Koottaa Haa Jalqabnu! 💖
        </p>
      </div>

    </div>

  </div>
</section>


<!-- ================= ARABIC MESSAGE ================= -->

<section>
  <div class="container">

    <div class="markaza-box">

      <div class="arabic">
        بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
      </div>

      <div class="arabic">
        الْقُرْآنُ يَنْتَظِرُكَ! 📖
      </div>

      <div class="arabic">
        الْمَكَانُ هُنَا! 🕌
      </div>

      <div class="arabic">
        الْفُرْصَةُ الْآنَ! ⏰
      </div>

      <div class="arabic">
        الرِّحْلَةُ تَبْدَأُ! 🚀
      </div>

      <div class="quote arabic">
        "نَحْنُ هُنَا لِنُعَلِّمَكَ الْقُرْآنَ كَمَا أُنْزِلَ،
        وَنُعَرِّفَكَ بِنَبِيِّكَ،
        وَنُفَهِّمَكَ دِينَكَ،
        وَنُصَحِّحَ لَكَ عَقِيدَتَكَ"
      </div>

      <div class="arabic">
        خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ ☀️
      </div>

    </div>

  </div>
</section>


<!-- ================= CONTACT ================= -->

<section id="contact">
  <div class="container">

    <div class="section-title">
      <span>Contact</span>
      <h2>📞 Nu Quunnamaa</h2>
    </div>

    <div class="contact-grid">

      <div class="card contact-card">
        <div class="card-icon">📞</div>
        <h3>Bilbila</h3>
        <a href="tel:+251915455051">
          0915455051
        </a>
      </div>

      <div class="card contact-card">
        <div class="card-icon">📱</div>
        <h3>WhatsApp</h3>
        <a href="https://wa.me/251915455051" target="_blank">
          0915455051
        </a>
      </div>

      <div class="card contact-card">
        <div class="card-icon">📧</div>
        <h3>Email</h3>
        <a href="mailto:Ferhanshaamil@gmail.com">
          Ferhanshaamil@gmail.com
        </a>
      </div>

    </div>

  </div>
</section>


<!-- ================= FINAL CTA ================= -->

<section>
  <div class="container">

    <div class="cta">

      <h2>🌿✨ Koottaa Haa Jalqabnu!</h2>

      <p class="big">
        "Irra Caalaan Keessan Nama Qur'aana Baratee Barsiise Dha."
      </p>

      <div class="arabic">
        خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ
      </div>

      <p>
        Lakkaa'i Siif, Qara'aa Cimaa Ta'i,
        Muslima Aqiidaa Sirrii Qabu Ta'i,
        Nabiyyii Kee ﷺ Hordofi.
      </p>

      <div class="buttons" style="justify-content:center;">

        <a class="btn btn-primary"
          href="https://wa.me/251915455051"
          target="_blank">
          📱 WhatsApp
        </a>

        <a class="btn btn-outline"
          href="#register">
          📝 Amma Galmaa'i
        </a>

      </div>

    </div>

  </div>
</section>


<!-- ================= FOOTER ================= -->

<footer>

  <div class="container">

    <div class="arabic">
      مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ
    </div>

    <p>
      🌿 Markaza Uweysii Ibnu Aamir
    </p>

    <p>
      Barsiisaa: <strong>Ferhan Shaamil</strong>
    </p>

    <p>
      Da'ii • Barsiisaa Qur'aanaa • Barataa Software Engineering
    </p>

    <br>

    <p>
      © 2026 Ferhan Shaamil. Mirgi Hunda Seeraan Eegama.
    </p>

  </div>

</footer>


<!-- ================= WHATSAPP ================= -->

<a
  class="whatsapp"
  href="https://wa.me/251915455051"
  target="_blank"
  aria-label="WhatsApp">
  📱
</a>


<!-- ================= JAVASCRIPT ================= -->

<script>

  function submitForm(event) {

    event.preventDefault();

    alert(
      "🌿 Galatoomi! Odeeffannoon Galmee Keessanii Fuulduratti Qoratama. 📖🕌"
    );

  }

</script>

</body>
</html><!DOCTYPE html>
<html lang="om">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ferhan Shaamil | Markaza Uweysii Ibnu Aamir</title>

  <meta name="description"
        content="Official website of Ferhan Shaamil AbdulGafur and Markaza Uweysii Ibnu Aamir — Qur'an, Tajweed and Islamic Sciences.">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --bg: #04100c;
      --bg2: #071a13;
      --card: rgba(13, 42, 31, .72);
      --card2: #0b2419;
      --green: #0d5138;
      --green-light: #18704d;
      --gold: #d6b45d;
      --gold-light: #f2d98d;
      --white: #f7f5ed;
      --text: #d8e2dc;
      --muted: #9eaea6;
      --border: rgba(214,180,93,.25);
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background:
        radial-gradient(circle at 15% 10%, rgba(214,180,93,.08), transparent 25%),
        radial-gradient(circle at 85% 40%, rgba(24,112,77,.12), transparent 30%),
        var(--bg);
      color: var(--white);
      line-height: 1.7;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: .035;
      background-image:
        linear-gradient(30deg, #fff 12%, transparent 12.5%, transparent 87%, #fff 87.5%, #fff),
        linear-gradient(150deg, #fff 12%, transparent 12.5%, transparent 87%, #fff 87.5%, #fff);
      background-size: 70px 120px;
      z-index: -1;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    .container {
      width: min(1180px, 92%);
      margin: auto;
    }

    /* ================= NAVBAR ================= */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 999;
      background: rgba(4,16,12,.88);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid var(--border);
    }

    .nav {
      min-height: 76px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 11px;
    }

    .logo-mark {
      width: 45px;
      height: 45px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      border: 1px solid var(--gold);
      background: rgba(214,180,93,.06);
      font-size: 22px;
    }

    .logo-text strong {
      display: block;
      color: var(--gold-light);
      font-size: 14px;
      letter-spacing: .7px;
    }

    .logo-text small {
      display: block;
      color: var(--muted);
      font-size: 9px;
    }

    .nav-links {
      display: flex;
      gap: 20px;
      align-items: center;
      list-style: none;
      font-size: 13px;
    }

    .nav-links a {
      color: var(--text);
      transition: .3s;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .nav-contact {
      border: 1px solid var(--gold);
      padding: 8px 15px;
      border-radius: 25px;
      color: var(--gold-light) !important;
    }

    /* ================= HERO ================= */

    .hero {
      min-height: 100vh;
      padding: 145px 0 80px;
      display: flex;
      align-items: center;
      position: relative;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 50px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      padding: 7px 15px;
      border: 1px solid var(--border);
      background: rgba(214,180,93,.06);
      border-radius: 30px;
      color: var(--gold-light);
      font-size: 12px;
      margin-bottom: 20px;
    }

    .hero h1 {
      font-size: clamp(40px, 6vw, 76px);
      line-height: 1.05;
      letter-spacing: -2px;
    }

    .hero h1 span {
      color: var(--gold-light);
    }

    .hero-title {
      color: var(--text);
      font-size: clamp(18px, 3vw, 25px);
      margin: 20px 0 12px;
    }

    .arabic {
      direction: rtl;
      text-align: right;
      font-family: "Times New Roman", serif;
    }

    .hero-arabic {
      color: var(--gold-light);
      font-size: clamp(22px, 3vw, 32px);
      margin: 15px 0;
    }

    .hero-description {
      max-width: 680px;
      color: var(--muted);
      font-size: 15px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 28px;
    }

    .btn {
      display: inline-block;
      padding: 12px 22px;
      border-radius: 30px;
      border: 1px solid var(--gold);
      font-weight: bold;
      font-size: 13px;
      transition: .3s;
    }

    .btn:hover {
      transform: translateY(-4px);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold-light), var(--gold));
      color: #07130e;
      border: none;
    }

    .hero-card {
      border: 1px solid var(--border);
      background: linear-gradient(145deg, rgba(18,68,48,.7), rgba(7,27,19,.8));
      border-radius: 35px;
      padding: 35px;
      text-align: center;
      box-shadow: 0 30px 70px rgba(0,0,0,.25);
    }

    .hero-symbol {
      width: 150px;
      height: 150px;
      margin: auto;
      border-radius: 50%;
      display: grid;
      place-items: center;
      border: 1px solid var(--gold);
      background: radial-gradient(circle, rgba(214,180,93,.15), transparent 65%);
      font-size: 70px;
    }

    .hero-card h3 {
      margin-top: 20px;
      color: var(--gold-light);
    }

    .hero-card p {
      color: var(--muted);
      font-size: 13px;
      margin-top: 7px;
    }

    /* ================= SECTIONS ================= */

    section {
      padding: 90px 0;
    }

    .section-head {
      text-align: center;
      max-width: 760px;
      margin: 0 auto 45px;
    }

    .section-mini {
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 3px;
      font-size: 11px;
    }

    .section-head h2 {
      font-size: clamp(29px, 5vw, 45px);
      margin: 7px 0;
    }

    .section-head p {
      color: var(--muted);
      font-size: 14px;
    }

    /* ================= PERSONAL ================= */

    .personal {
      background: rgba(7,26,19,.55);
    }

    .personal-grid {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 25px;
      align-items: stretch;
    }

    .profile-card,
    .content-card {
      border: 1px solid var(--border);
      background: var(--card);
      border-radius: 27px;
      padding: 32px;
    }

    .profile-icon {
      width: 115px;
      height: 115px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      margin-bottom: 20px;
      border: 1px solid var(--gold);
      background: rgba(214,180,93,.07);
      font-size: 50px;
    }

    .profile-card h3 {
      color: var(--gold-light);
      font-size: 23px;
    }

    .profile-card .role {
      color: var(--muted);
      margin: 6px 0 20px;
      font-size: 13px;
    }

    .profile-list {
      list-style: none;
      display: grid;
      gap: 9px;
      color: var(--text);
      font-size: 13px;
    }

    .content-card h3 {
      color: var(--gold-light);
      margin-bottom: 12px;
      font-size: 24px;
    }

    .content-card p {
      color: var(--muted);
      margin-bottom: 14px;
    }

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-top: 20px;
    }

    .skill {
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 6px 12px;
      color: var(--gold-light);
      background: rgba(214,180,93,.05);
      font-size: 11px;
    }

    /* ================= MARKAZA ================= */

    .markaza-box {
      position: relative;
      overflow: hidden;
      text-align: center;
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 60px 25px;
      background:
        radial-gradient(circle at center, rgba(24,112,77,.28), transparent 60%),
        rgba(8,29,21,.75);
    }

    .markaza-icon {
      font-size: 50px;
    }

    .markaza-box h2 {
      color: var(--gold-light);
      font-size: clamp(27px, 5vw, 46px);
      margin-top: 10px;
    }

    .markaza-arabic {
      color: #eee4c8;
      font-size: 25px;
      margin: 8px 0 20px;
    }

    .markaza-box p {
      max-width: 780px;
      margin: auto;
      color: var(--muted);
    }

    /* ================= PROGRAMS ================= */

    .program-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .program {
      position: relative;
      border: 1px solid var(--border);
      border-radius: 23px;
      padding: 28px;
      background: var(--card2);
      transition: .35s;
      overflow: hidden;
    }

    .program:hover {
      transform: translateY(-7px);
      border-color: var(--gold);
    }

    .program-icon {
      font-size: 37px;
    }

    .program h3 {
      font-size: 18px;
      margin-top: 8px;
    }

    .program p {
      color: var(--muted);
      font-size: 13px;
      margin: 7px 0 15px;
    }

    .duration {
      display: inline-block;
      padding: 5px 11px;
      border-radius: 20px;
      border: 1px solid var(--border);
      color: var(--gold-light);
      font-size: 10px;
    }

    /* ================= CURRICULUM ================= */

    .curriculum {
      background: rgba(7,26,19,.55);
    }

    .book-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
    }

    .book {
      display: flex;
      gap: 16px;
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 22px;
      background: var(--card);
    }

    .book-icon {
      font-size: 31px;
    }

    .book h3 {
      color: var(--gold-light);
      font-size: 16px;
    }

    .book p {
      color: var(--muted);
      font-size: 12px;
      margin-top: 4px;
    }

    /* ================= SCHEDULE ================= */

    .schedule-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
    }

    .week {
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 20px;
      background: var(--card);
    }

    .week h3 {
      color: var(--gold-light);
      margin-bottom: 12px;
      font-size: 16px;
    }

    .day {
      border-top: 1px solid rgba(255,255,255,.06);
      padding: 9px 0;
      font-size: 12px;
      color: var(--muted);
    }

    .day strong {
      color: var(--white);
      display: block;
    }

    /* ================= MESSAGE ================= */

    .message-box {
      max-width: 900px;
      margin: auto;
      text-align: center;
      padding: 45px 25px;
      border-radius: 28px;
      border: 1px solid var(--border);
      background: linear-gradient(135deg, #0d3021, #071c14);
    }

    .message-box .arabic {
      text-align: center;
      color: var(--gold-light);
      font-size: 25px;
      line-height: 1.9;
    }

    .message-box p {
      color: var(--muted);
      margin-top: 18px;
      font-size: 14px;
    }

    /* ================= ONLINE ================= */

    .online-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .online {
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 28px;
      text-align: center;
      background: var(--card);
    }

    .online-icon {
      font-size: 38px;
    }

    .online h3 {
      color: var(--gold-light);
      margin: 8px 0;
    }

    .online p {
      color: var(--muted);
      font-size: 12px;
    }

    /* ================= REGISTRATION ================= */

    .register {
      background: rgba(7,26,19,.6);
    }

    .register-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
    }

    .register-info,
    .register-card {
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 32px;
      background: var(--card);
    }

    .register-info h3,
    .register-card h3 {
      color: var(--gold-light);
      font-size: 25px;
      margin-bottom: 12px;
    }

    .register-info p {
      color: var(--muted);
      font-size: 14px;
    }

    .steps {
      margin-top: 22px;
      display: grid;
      gap: 11px;
    }

    .step {
      display: flex;
      gap: 12px;
      align-items: center;
      color: var(--text);
      font-size: 13px;
    }

    .step span {
      width: 29px;
      height: 29px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: rgba(214,180,93,.1);
      border: 1px solid var(--border);
      color: var(--gold-light);
      flex-shrink: 0;
    }

    .form-demo {
      display: grid;
      gap: 12px;
      margin-top: 18px;
    }

    .form-demo input,
    .form-demo select {
      width: 100%;
      padding: 12px 14px;
      border-radius: 12px;
      border: 1px solid var(--border);
      background: #061810;
      color: var(--text);
      outline: none;
    }

    .form-demo input:focus,
    .form-demo select:focus {
      border-color: var(--gold);
    }

    /* ================= CONTACT ================= */

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .contact-card {
      text-align: center;
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 28px;
      background: var(--card);
      transition: .3s;
    }

    .contact-card:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
    }

    .contact-icon {
      font-size: 34px;
    }

    .contact-card h3 {
      color: var(--gold-light);
      margin: 8px 0;
    }

    .contact-card p {
      color: var(--muted);
      font-size: 13px;
      word-break: break-word;
    }

    /* ================= CTA ================= */

    .cta {
      text-align: center;
      padding: 95px 20px;
      background:
        radial-gradient(circle, rgba(24,112,77,.3), transparent 60%);
    }

    .cta .arabic {
      text-align: center;
      color: var(--gold-light);
      font-size: 28px;
      margin-bottom: 12px;
    }

    .cta h2 {
      font-size: clamp(32px, 6vw, 55px);
      color: var(--gold-light);
    }

    .cta p {
      color: var(--muted);
      max-width: 650px;
      margin: 10px auto 25px;
    }

    /* ================= FOOTER ================= */

    footer {
      border-top: 1px solid var(--border);
      background: #020a07;
      padding: 40px 0;
      text-align: center;
    }

    footer .footer-logo {
      font-size: 28px;
      margin-bottom: 8px;
    }

    footer strong {
      color: var(--gold-light);
    }

    footer p {
      color: var(--muted);
      font-size: 11px;
      margin-top: 5px;
    }

    /* ================= FLOATING BUTTON ================= */

    .floating {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 500;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: #16804f;
      border: 2px solid rgba(255,255,255,.2);
      font-size: 25px;
      box-shadow: 0 10px 30px rgba(0,0,0,.4);
    }

    /* ================= RESPONSIVE ================= */

    @media(max-width: 900px) {

      .nav-links {
        display: none;
      }

      .hero-grid,
      .personal-grid,
      .register-grid {
        grid-template-columns: 1fr;
      }

      .program-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .schedule-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .contact-grid,
      .online-grid {
        grid-template-columns: 1fr;
      }
    }

    @media(max-width: 560px) {

      section {
        padding: 65px 0;
      }

      .hero {
        padding-top: 125px;
      }

      .hero h1 {
        font-size: 42px;
      }

      .hero-card {
        padding: 25px;
      }

      .program-grid,
      .book-grid,
      .schedule-grid {
        grid-template-columns: 1fr;
      }

      .profile-card,
      .content-card,
      .register-info,
      .register-card {
        padding: 24px;
      }

      .markaza-box {
        padding: 42px 18px;
      }
    }

  </style>
</head>


<body>


<!-- =========================================================
     NAVIGATION
========================================================= -->

<nav>

  <div class="container nav">

    <a href="#home" class="logo">

      <div class="logo-mark">🌿</div>

      <div class="logo-text">
        <strong>FERHAN SHAAMIL</strong>
        <small>مركز أويس بن عامر</small>
      </div>

    </a>

    <ul class="nav-links">

      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#markaza">Markaza</a></li>
      <li><a href="#programs">Programs</a></li>
      <li><a href="#curriculum">Curriculum</a></li>
      <li><a href="#register">Galmee</a></li>
      <li>
        <a href="#contact" class="nav-contact">
          Nu Qunnami
        </a>
      </li>

    </ul>

  </div>

</nav>


<!-- =========================================================
     HERO
========================================================= -->

<section class="hero" id="home">

  <div class="container hero-grid">

    <div>

      <div class="badge">
        🌿✨ OFFICIAL WEBSITE • QUR'AN • EDUCATION • TECHNOLOGY
      </div>

      <h1>
        FERHAN<br>
        <span>SHAAMIL</span>
      </h1>

      <div class="hero-title">
        Da'ii • Barsiisaa • Software Engineering Student
      </div>

      <div class="arabic hero-arabic">
        فرحان شامل عبدالغفور
      </div>

      <p class="hero-description">

        Ani Ferhan Shaamil AbdulGafur,
        Barsiisaa Markaza Uweysii Ibnu Aamir,
        Da'ii fi barataa Software Engineering ti.
        Kaayyoon koo Qur'aana, beekumsa Shari'aa,
        tarbiyaa fi teknooloojii karaa bu'a qabeessa ta'een
        hawaasaaf dhiyeessuudha.

      </p>

      <div class="hero-buttons">

        <a href="#markaza" class="btn btn-primary">
          🕌 Markazaa Ilaali
        </a>

        <a href="#programs" class="btn">
          📚 Barnoota Ilaali
        </a>

      </div>

    </div>


    <div class="hero-card">

      <div class="hero-symbol">
        🕌
      </div>

      <h3>
        MARKAZA UWEYSII IBNU AAMIR
      </h3>

      <p>
        مركز أويس بن عامر لدراسة العلوم الشرعية
      </p>

      <p style="margin-top:18px;">
        📖 Qur'aana<br>
        🕌 علوم شرعية<br>
        🌱 Tarbiyaa<br>
        💻 Teknooloojii
      </p>

    </div>

  </div>

</section>


<!-- =========================================================
     ABOUT FERHAN
========================================================= -->

<section class="personal" id="about">

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        About Me
      </div>

      <h2>
        👤 Waa'ee Koo
      </h2>

      <p>
        Barnoota, Da'awaa, Qur'aana fi Teknooloojii walitti fiduu.
      </p>

    </div>


    <div class="personal-grid">

      <div class="profile-card">

        <div class="profile-icon">
          👤
        </div>

        <h3>
          Ferhan Shaamil AbdulGafur
        </h3>

        <div class="role">
          Da'ii • Barsiisaa • Software Engineering Student
        </div>

        <ul class="profile-list">

          <li>🕌 Barsiisaa Markaza Uweysii Ibnu Aamir</li>

          <li>📖 Barnoota Qur'aanaa fi علوم شرعية</li>

          <li>🌱 Ijaarsa fi tarbiyaa dhalootaa</li>

          <li>💻 Software Engineering</li>

          <li>🚀 Teknooloojii fi Digital Education</li>

        </ul>

      </div>


      <div class="content-card">

        <h3>
          🌿 Kaayyoo Koo
        </h3>

        <p>

          Beekumsi nama qofaaf osoo hin taane
          hawaasaafis faayidaa qabaachuu qaba.
          Kanaaf Qur'aanaa fi beekumsa Shari'aa
          karaa ammayyaa ta'een dabarsuun,
          dhaloota beekumsa, akhlaaqa fi dandeettii
          qabu ijaaruuf hojjechaa jira.

        </p>

        <p>

          Akkasumas teknooloojii ammayyaa fayyadamuun
          barnoota online, website, digital content
          fi tajaajila hawaasaa babal'isuun kaayyoo koo keessaa isa tokko.

        </p>

        <div class="skills">

          <span class="skill">📖 Qur'an</span>
          <span class="skill">🕌 Da'wah</span>
          <span class="skill">📚 Islamic Studies</span>
          <span class="skill">💻 Software Engineering</span>
          <span class="skill">🌐 Web Development</span>
          <span class="skill">🎨 Digital Design</span>

        </div>

      </div>

    </div>

  </div>

</section>


<!-- =========================================================
     MARKAZA
========================================================= -->

<section id="markaza">

  <div class="container">

    <div class="markaza-box">

      <div class="markaza-icon">
        🌿✨🕌📖
      </div>

      <h2>
        MARKAZA UWEYSII IBNU AAMIR
      </h2>

      <div class="arabic markaza-arabic">
        مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ
        لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
      </div>

      <p>

        <strong>
          “Iddoo Beekumsa Shar'iyyaa fi Qur'aana Kabajamaa.”
        </strong>

        <br><br>

        “منارة لتعلم العلوم الشرعية والقرآن الكريم”

        <br><br>

        Nُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،
        وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ.

      </p>

    </div>

  </div>

</section>


<!-- =========================================================
     PROGRAMS
========================================================= -->

<section id="programs">

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        Education Programs
      </div>

      <h2>
        📚 Sagantaalee Barnootaa
      </h2>

      <p>
        Barnoota Qur'aanaa fi علوم شرعية sadarkaa adda addaatiin.
      </p>

    </div>


    <div class="program-grid">


      <div class="program">

        <div class="program-icon">🔤</div>

        <h3>
          Qaacidda Nooraniyyaa
        </h3>

        <p>
          Bu'uura dubbisa Qur'aanaa,
          qubee fi mallattoo dubbisaa.
        </p>

        <span class="duration">
          🌱 Jalqabdootaaf
        </span>

      </div>


      <div class="program">

        <div class="program-icon">📖</div>

        <h3>
          Tilawaa fi Tajwiid
        </h3>

        <p>
          Qara'a Qur'aanaa sirreessuu
          fi seera Tajwiidaa barachuu.
        </p>

        <span class="duration">
          ⏳ Ji'a 3
        </span>

      </div>


      <div class="program">

        <div class="program-icon">🌙</div>

        <h3>
          Seenaa Nabiyyii ﷺ
        </h3>

        <p>
          Jireenya Nabiyyii ﷺ irraa
          barnoota fi tarbiyaa fudhachuu.
        </p>

        <span class="duration">
          ⏳ Ji'a 2
        </span>

      </div>


      <div class="program">

        <div class="program-icon">🕌</div>

        <h3>
          Fiqhii fi Ahkaam
        </h3>

        <p>
          Ahkaama jireenya Muslimaa
          fi bu'uura Fiqhii.
        </p>

        <span class="duration">
          ⏳ Ji'a 3
        </span>

      </div>


      <div class="program">

        <div class="program-icon">☝️</div>

        <h3>
          Aqeedaa Sirrii
        </h3>

        <p>
          Tawhiida fi bu'uura Aqeedaa
          Islaamaa sirnaan barachuu.
        </p>

        <span class="duration">
          ⏳ Ji'a 2
        </span>

      </div>


      <div class="program">

        <div class="program-icon">✨</div>

        <h3>
          Sagantaa Guutuu
        </h3>

        <p>
          Tilawaa, Tajwiid, Aqeedaa,
          Fiqhii fi Seenaa walitti qabu.
        </p>

        <span class="duration">
          ⏳ Ji'a 3
        </span>

      </div>

    </div>

  </div>

</section>


<!-- =========================================================
     CURRICULUM
========================================================= -->

<section class="curriculum" id="curriculum">

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        Curriculum
      </div>

      <h2>
        📚 Kitaabota fi Qabiyyee
      </h2>

      <p>
        Kitaabota fi mata-dureewwan barnoota keessatti fayyadamnu.
      </p>

    </div>


    <div class="book-grid">


      <div class="book">

        <div class="book-icon">🔤</div>

        <div>

          <h3>
            القاعدة النورانية
          </h3>

          <p>
            Qaacidda Nooraniyyaa fi bu'uura dubbisa Qur'aanaa.
          </p>

        </div>

      </div>


      <div class="book">

        <div class="book-icon">📖</div>

        <div>

          <h3>
            التلاوة والتجويد
          </h3>

          <p>
            Tilawaa, Makhaarij, Sifaat fi Ahkaama Tajwiidaa.
          </p>

        </div>

      </div>


      <div class="book">

        <div class="book-icon">☝️</div>

        <div>

          <h3>
            الأصول الثلاثة
          </h3>

          <p>
            Bu'uura beekumsa Aqeedaa fi Tawhiidaa.
          </p>

        </div>

      </div>


      <div class="book">

        <div class="book-icon">🕌</div>

        <div>

          <h3>
            كتاب التوحيد والعقيدة الواسطية
          </h3>

          <p>
            Barnoota Tawhiidaa fi Aqeedaa.
          </p>

        </div>

      </div>


      <div class="book">

        <div class="book-icon">📕</div>

        <div>

          <h3>
            خذ عقيدتك
          </h3>

          <p>
            Barnoota bu'uuraa Aqeedaa Islaamaa.
          </p>

        </div>

      </div>


      <div class="book">

        <div class="book-icon">📚</div>

        <div>

          <h3>
            الأربعون النووية وبلوغ المرام
          </h3>

          <p>
            Hadiisa, Ahkaama fi barnoota Islaamaa.
          </p>

        </div>

      </div>


      <div class="book">

        <div class="book-icon">⚖️</div>

        <div>

          <h3>
            الأحكام الفقهية
          </h3>

          <p>
            Ahkaama Fiqhii fi hojii guyyaa guyyaa.
          </p>

        </div>

      </div>


      <div class="book">

        <div class="book-icon">🌙</div>

        <div>

          <h3>
            السيرة النبوية
          </h3>

          <p>
            Seenaa Nabiyyii ﷺ fi barnoota jireenyaa.
          </p>

        </div>

      </div>

    </div>

  </div>

</section>


<!-- =========================================================
     MONTHLY PROGRAM
========================================================= -->

<section>

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        Monthly Intensive
      </div>

      <h2>
        🗓️ Sagantaa Ji'a Tokkoo
      </h2>

      <p>
        Sagantaa cimsaa dargaggootaa fi shamarranii.
      </p>

    </div>


    <div class="schedule-grid">


      <div class="week">

        <h3>
          🟢 Torban 1 — Bu'uura
        </h3>

        <div class="day">
          <strong>Saturday</strong>
          Qubee Nooraniyyaa
        </div>

        <div class="day">
          <strong>Sunday</strong>
          Harakaat — Fatha, Kasra, Dhamma
        </div>

        <div class="day">
          <strong>Monday</strong>
          Tanween fi Sukoon
        </div>

        <div class="day">
          <strong>Tuesday</strong>
          Shaddaa fi Leen
        </div>

      </div>


      <div class="week">

        <h3>
          🔵 Torban 2 — Tajwiid
        </h3>

        <div class="day">
          <strong>Saturday</strong>
          Noon Saakinah — Izhaar / Idghaam
        </div>

        <div class="day">
          <strong>Sunday</strong>
          Iqlaab / Ikhfaa
        </div>

        <div class="day">
          <strong>Monday</strong>
          Ahkaama Meem Saakinah
        </div>

        <div class="day">
          <strong>Tuesday</strong>
          Ghunnah
        </div>

      </div>


      <div class="week">

        <h3>
          🟣 Torban 3 — Madd & Aqeedaa
        </h3>

        <div class="day">
          <strong>Saturday</strong>
          Madd Tabi'ii + Muttasil
        </div>

        <div class="day">
          <strong>Sunday</strong>
          Madd Munfasil + Badal
        </div>

        <div class="day">
          <strong>Monday</strong>
          Tawhiida Allah
        </div>

        <div class="day">
          <strong>Tuesday</strong>
          Ikhlaas + Faatihah
        </div>

      </div>


      <div class="week">

        <h3>
          🟡 Torban 4 — Xumura
        </h3>

        <div class="day">
          <strong>Saturday</strong>
          Irra Deebii Nooraniyyaa
        </div>

        <div class="day">
          <strong>Sunday</strong>
          Irra Deebii Noon / Meem
        </div>

        <div class="day">
          <strong>Monday</strong>
          Madd + Aqeedaa
        </div>

        <div class="day">
          <strong>Tuesday</strong>
          Qormaata + Beekkamsa
        </div>

      </div>

    </div>

  </div>

</section>


<!-- =========================================================
     MESSAGE
========================================================= -->

<section>

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        Our Mission
      </div>

      <h2>
        🌿 Ergaa Keenya
      </h2>

    </div>


    <div class="message-box">

      <div class="arabic">

        نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،
        وَنُعَرِّفُكَ بِنَبِيِّكَ ﷺ،
        وَنُفَهِّمُكَ دِينَكَ،
        وَنُصَحِّحُ لَكَ عَقِيدَتَكَ.

      </div>

      <p>

        Akka ati Qur'aana sirriitti qaraatu,
        Muslima Aqeedaa sirrii qabu taatu,
        Diinii kee hubattu,
        Nabiyyii kee ﷺ hordoftuuf si qopheessina.

      </p>

    </div>

  </div>

</section>


<!-- =========================================================
     ONLINE LEARNING
========================================================= -->

<section class="personal">

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        Online Learning
      </div>

      <h2>
        💻 Barnoota Online
      </h2>

      <p>
        Barnoota bakka jirtutti argachuu dandeessa.
      </p>

    </div>


    <div class="online-grid">


      <div class="online">

        <div class="online-icon">
          💬
        </div>

        <h3>
          WhatsApp
        </h3>

        <p>
          Odeeffannoo, qunnamtii fi
          hordoffii barnootaa.
        </p>

      </div>


      <div class="online">

        <div class="online-icon">
          ✈️
        </div>

        <h3>
          Telegram
        </h3>

        <p>
          Qabiyyee barnootaa fi
          beeksisa Markazaa.
        </p>

      </div>


      <div class="online">

        <div class="online-icon">
          📱
        </div>

        <h3>
          IMO
        </h3>

        <p>
          Qunnamtii fi barnoota
          karaa online.
        </p>

      </div>

    </div>

  </div>

</section>


<!-- =========================================================
     REGISTRATION
========================================================= -->

<section class="register" id="register">

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        Registration
      </div>

      <h2>
        📝 Galmaa'i Amma
      </h2>

      <p>
        Imala barnootaa kee har'a jalqabi.
      </p>

    </div>


    <div class="register-grid">


      <div class="register-info">

        <h3>
          🚀 Akkamitti Galmaa'uu?
        </h3>

        <p>
          Sagantaa siif mijatu filadhu;
          odeeffannoo kee guutiitii
          Markazaa waliin qunnami.
        </p>

        <div class="steps">

          <div class="step">
            <span>1</span>
            Sagantaa barachuu barbaaddu filadhu.
          </div>

          <div class="step">
            <span>2</span>
            Maqaa fi odeeffannoo kee qopheessi.
          </div>

          <div class="step">
            <span>3</span>
            Foormii galmee guuti.
          </div>

          <div class="step">
            <span>4</span>
            Nu qunnami.
          </div>

          <div class="step">
            <span>5</span>
            Barnoota jalqabi. 📖
          </div>

        </div>

      </div>


      <div class="register-card">

        <h3>
          استمارة التسجيل
        </h3>

        <p style="color:var(--muted);font-size:13px;">
          نُعلّمك القرآن، ونُعرّفك نبيّك،
          انضم إلينا في رحلة بناء الجيل القرآني المتقن.
        </p>

        <div class="form-demo">

          <input
            type="text"
            placeholder="Maqaa Guutuu"
          >

          <input
            type="number"
            placeholder="Umurii"
          >

          <input
            type="tel"
            placeholder="Lakkoofsa Bilbila"
          >

          <select>

            <option>
              Sagantaa Filadhu
            </option>

            <option>
              Qaacidda Nooraniyyaa
            </option>

            <option>
              Tilawaa fi Tajwiid
            </option>

            <option>
              Seenaa Nabiyyii ﷺ
            </option>

            <option>
              Fiqhii fi Ahkaam
            </option>

            <option>
              Aqeedaa Sirrii
            </option>

            <option>
              Sagantaa Guutuu
            </option>

          </select>

          <a
            href="https://forms.google.com"
            target="_blank"
            class="btn btn-primary"
            style="text-align:center;"
          >
            📝 Foormii Guutuu
          </a>

        </div>

      </div>

    </div>

  </div>

</section>


<!-- =========================================================
     CONTACT
========================================================= -->

<section id="contact">

  <div class="container">

    <div class="section-head">

      <div class="section-mini">
        Contact
      </div>

      <h2>
        📞 Nu Qunnami
      </h2>

      <p>
        Odeeffannoo dabalataaf karaa armaan gadiitiin nu qunnami.
      </p>

    </div>


    <div class="contact-grid">


      <a
        href="tel:0915455051"
        class="contact-card"
      >

        <div class="contact-icon">
          📞
        </div>

        <h3>
          Bilbila
        </h3>

        <p>
          0915455051
        </p>

      </a>


      <a
        href="https://wa.me/251915455051"
        target="_blank"
        class="contact-card"
      >

        <div class="contact-icon">
          💬
        </div>

        <h3>
          WhatsApp
        </h3>

        <p>
          0915455051
        </p>

      </a>


      <a
        href="mailto:Ferhanshaamil@gmail.com"
        class="contact-card"
      >

        <div class="contact-icon">
          📧
        </div>

        <h3>
          Email
        </h3>

        <p>
          Ferhanshaamil@gmail.com
        </p>

      </a>

    </div>

  </div>

</section>


<!-- =========================================================
     FINAL CTA
========================================================= -->

<section class="cta">

  <div class="container">

    <div class="arabic">
      خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ
    </div>

    <h2>
      Qur'aanni Si Eeggata! 📖
    </h2>

    <p>

      Bakki as jira. 🕌
      Carraan amma jira. ⏰
      Imalli barnootaa har'a jalqaba. 🚀

    </p>

    <a href="#register" class="btn btn-primary">
      📝 Amma Galmaa'i
    </a>

  </div>

</section>


<!-- =========================================================
     FOOTER
========================================================= -->

<footer>

  <div class="container">

    <div class="footer-logo">
      🌿✨🕌📖
    </div>

    <p>
      <strong>
        FERHAN SHAAMIL ABDULGAFUR
      </strong>
    </p>

    <p>
      Markaza Uweysii Ibnu Aamir
    </p>

    <p>
      مركز أويس بن عامر لدراسة العلوم الشرعية
    </p>

    <p>
      © 2026 Ferhan Shaamil. All Rights Reserved.
    </p>

  </div>

</footer>


<!-- =========================================================
     FLOATING WHATSAPP
========================================================= -->

<a
  href="https://wa.me/251915455051"
  target="_blank"
  class="floating"
  title="WhatsApp"
>
  💬
</a>


</body>
</html><!DOCTYPE html>
<html lang="om">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ferhan Shaamil | Da'ii & Barsiisaa</title>

  <meta
    name="description"
    content="Ferhan Shaamil — Da'ii, Barsiisaa Qur'aanaa fi Beekumsa Shari'aa. Dhaloota Qur'aanaa, beekumsa Shari'aa fi akkaataa jireenyaa gaarii ijaaruuf."
  >

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #061713;
      color: #f5f1df;
      line-height: 1.7;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* =========================
       NAVBAR
    ========================== */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;

      display: flex;
      justify-content: space-between;
      align-items: center;

      padding: 18px 7%;

      background: rgba(6, 23, 19, 0.88);
      backdrop-filter: blur(15px);

      border-bottom: 1px solid rgba(212, 175, 55, 0.15);
    }

    .logo {
      font-size: 22px;
      font-weight: 800;
      color: #d4af37;
      letter-spacing: 1px;
    }

    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
    }

    .nav-links a {
      color: #eee;
      font-size: 14px;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: #d4af37;
    }

    /* =========================
       HERO
    ========================== */

    .hero {
      min-height: 100vh;

      display: flex;
      align-items: center;
      justify-content: center;

      text-align: center;

      padding: 120px 7% 80px;

      position: relative;
      overflow: hidden;

      background:
        radial-gradient(circle at top right, rgba(212,175,55,0.15), transparent 35%),
        radial-gradient(circle at bottom left, rgba(0,120,90,0.20), transparent 35%),
        #061713;
    }

    .hero-content {
      max-width: 900px;
    }

    .small-title {
      color: #d4af37;
      font-size: 14px;
      letter-spacing: 4px;
      text-transform: uppercase;
      margin-bottom: 20px;
    }

    .hero h1 {
      font-size: clamp(48px, 10vw, 100px);
      line-height: 1;
      font-weight: 900;
      margin-bottom: 20px;
      letter-spacing: -3px;
    }

    .arabic {
      font-family: "Times New Roman", serif;
      font-size: clamp(25px, 5vw, 42px);
      color: #d4af37;
      margin-bottom: 20px;
      direction: rtl;
    }

    .hero h2 {
      font-size: clamp(20px, 4vw, 32px);
      color: #ffffff;
      margin-bottom: 25px;
    }

    .hero p {
      max-width: 760px;
      margin: auto;
      font-size: 18px;
      color: #c7d0cb;
    }

    .hero-tags {
      margin-top: 30px;

      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
    }

    .tag {
      padding: 9px 16px;
      border: 1px solid rgba(212,175,55,0.35);
      border-radius: 30px;
      background: rgba(212,175,55,0.06);
      color: #e5d49a;
      font-size: 14px;
    }

    .buttons {
      margin-top: 35px;

      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
    }

    .btn {
      padding: 14px 25px;
      border-radius: 40px;
      font-weight: bold;
      transition: 0.3s;
      display: inline-block;
    }

    .btn-primary {
      background: #d4af37;
      color: #061713;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 30px rgba(212,175,55,0.2);
    }

    .btn-outline {
      border: 1px solid #d4af37;
      color: #d4af37;
    }

    .btn-outline:hover {
      background: #d4af37;
      color: #061713;
    }

    /* =========================
       SECTIONS
    ========================== */

    section {
      padding: 100px 7%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 55px;
    }

    .section-title span {
      color: #d4af37;
      font-size: 13px;
      letter-spacing: 3px;
      text-transform: uppercase;
    }

    .section-title h2 {
      font-size: clamp(32px, 5vw, 55px);
      margin-top: 10px;
    }

    .section-title p {
      max-width: 700px;
      margin: 15px auto 0;
      color: #aebbb5;
    }

    /* =========================
       ABOUT
    ========================== */

    .about {
      background: #081e18;
    }

    .about-grid {
      max-width: 1100px;
      margin: auto;

      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 35px;
    }

    .card {
      padding: 35px;

      border-radius: 25px;

      background: rgba(255,255,255,0.035);

      border: 1px solid rgba(212,175,55,0.13);

      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: rgba(212,175,55,0.4);
    }

    .card h3 {
      color: #d4af37;
      margin-bottom: 15px;
      font-size: 24px;
    }

    .card p {
      color: #c4cec9;
    }

    .skills {
      margin-top: 25px;

      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .skill {
      background: #0d2a22;
      padding: 8px 14px;
      border-radius: 20px;
      color: #e4d69f;
      font-size: 13px;
    }

    /* =========================
       MARKAZA
    ========================== */

    .markaza {
      background:
        radial-gradient(circle at center, rgba(0,100,75,0.18), transparent 50%),
        #061713;
    }

    .markaza-box {
      max-width: 1100px;
      margin: auto;

      padding: 55px 35px;

      text-align: center;

      border-radius: 30px;

      background: linear-gradient(
        145deg,
        rgba(15,48,38,0.9),
        rgba(5,23,18,0.95)
      );

      border: 1px solid rgba(212,175,55,0.25);
    }

    .markaza-box .arabic {
      margin-top: 15px;
    }

    .markaza-subtitle {
      color: #d4af37;
      font-size: 20px;
      margin: 20px 0;
    }

    .markaza-quote {
      max-width: 800px;
      margin: 25px auto;

      font-family: "Times New Roman", serif;
      font-size: 25px;
      direction: rtl;
      color: #f5f1df;
    }

    /* =========================
       PROGRAMS
    ========================== */

    .programs {
      background: #081e18;
    }

    .program-grid {
      max-width: 1200px;
      margin: auto;

      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .program {
      padding: 30px;

      border-radius: 22px;

      background: #0a251d;

      border: 1px solid rgba(212,175,55,0.12);

      transition: 0.3s;
    }

    .program:hover {
      transform: translateY(-7px);
      border-color: rgba(212,175,55,0.4);
    }

    .program-icon {
      font-size: 35px;
      margin-bottom: 15px;
    }

    .program h3 {
      color: #fff;
      margin-bottom: 10px;
    }

    .program p {
      color: #aebbb5;
      font-size: 15px;
    }

    .duration {
      display: inline-block;
      margin-top: 18px;

      color: #d4af37;

      font-size: 13px;
      font-weight: bold;
    }

    /* =========================
       CURRICULUM
    ========================== */

    .curriculum {
      background: #061713;
    }

    .book-grid {
      max-width: 1000px;
      margin: auto;

      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
    }

    .book {
      padding: 20px;

      background: #0b251e;

      border-left: 3px solid #d4af37;

      border-radius: 10px;
    }

    .book strong {
      color: #fff;
    }

    .book span {
      display: block;
      margin-top: 5px;
      color: #aebbb5;
      font-family: "Times New Roman", serif;
      direction: rtl;
    }

    /* =========================
       MESSAGE
    ========================== */

    .message {
      text-align: center;
      background:
        linear-gradient(rgba(6,23,19,0.9), rgba(6,23,19,0.9)),
        #061713;
    }

    .message-box {
      max-width: 850px;
      margin: auto;
    }

    .message-box .arabic {
      font-size: clamp(25px, 5vw, 42px);
      line-height: 1.8;
    }

    .message-box p {
      color: #c3cec9;
      font-size: 18px;
    }

    /* =========================
       CONTACT
    ========================== */

    .contact {
      background: #081e18;
    }

    .contact-grid {
      max-width: 1000px;
      margin: auto;

      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .contact-card {
      text-align: center;
      padding: 30px;

      background: #0a251d;

      border-radius: 20px;

      border: 1px solid rgba(212,175,55,0.12);
    }

    .contact-card .icon {
      font-size: 30px;
      margin-bottom: 10px;
    }

    .contact-card h3 {
      color: #d4af37;
      margin-bottom: 5px;
    }

    .contact-card p {
      color: #c1ccc7;
    }

    /* =========================
       CTA
    ========================== */

    .cta {
      padding: 100px 7%;

      text-align: center;

      background:
        radial-gradient(circle, rgba(212,175,55,0.15), transparent 50%),
        #061713;
    }

    .cta h2 {
      font-size: clamp(35px, 7vw, 65px);
      margin-bottom: 15px;
    }

    .cta .arabic {
      font-size: 30px;
    }

    /* =========================
       FOOTER
    ========================== */

    footer {
      padding: 45px 7%;

      text-align: center;

      background: #04110e;

      border-top: 1px solid rgba(212,175,55,0.12);
    }

    footer h3 {
      color: #d4af37;
      margin-bottom: 10px;
    }

    footer p {
      color: #81918a;
      font-size: 14px;
    }

    .footer-arabic {
      font-family: "Times New Roman", serif;
      direction: rtl;
      color: #d4af37;
      font-size: 20px;
      margin: 10px 0;
    }

    /* =========================
       WHATSAPP
    ========================== */

    .whatsapp {
      position: fixed;
      right: 20px;
      bottom: 20px;

      width: 58px;
      height: 58px;

      display: flex;
      align-items: center;
      justify-content: center;

      border-radius: 50%;

      background: #25D366;
      color: white;

      font-size: 28px;

      box-shadow: 0 8px 30px rgba(0,0,0,0.35);

      z-index: 999;
    }

    /* =========================
       MOBILE
    ========================== */

    @media (max-width: 800px) {

      nav {
        padding: 15px 5%;
      }

      .nav-links {
        display: none;
      }

      section {
        padding: 75px 5%;
      }

      .hero {
        padding: 120px 5% 80px;
      }

      .hero h1 {
        letter-spacing: -2px;
      }

      .about-grid,
      .program-grid,
      .book-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .card {
        padding: 25px;
      }

      .markaza-box {
        padding: 40px 22px;
      }

      .markaza-quote {
        font-size: 21px;
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       NAVBAR
  ========================== -->

  <nav>

    <a href="#home" class="logo">
      FERHAN
    </a>

    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">Waa’ee Kiyya</a></li>
      <li><a href="#markaza">Markaza</a></li>
      <li><a href="#programs">Barnoota</a></li>
      <li><a href="#contact">Qunnamtii</a></li>
    </ul>

  </nav>


  <!-- =========================
       HERO
  ========================== -->

  <section class="hero" id="home">

    <div class="hero-content">

      <div class="small-title">
        Da'ii • Barsiisaa • Software Engineering Student
      </div>

      <h1>
        Ferhan Shaamil
      </h1>

      <div class="arabic">
        فرحان شامل عبدالغفور
      </div>

      <h2>
        داعية ومعلّم للقرآن والعلوم الشرعية
      </h2>

      <p>
        Barsiisaa Markaza Uweysii Ibnu Aamir,
        Da’ii fi Nama Dhaloota Qur’aanaa,
        Beekumsa Shari’aa fi Akkaataa Jireenyaa Gaarii
        Irratti Kakaasu.
      </p>

      <div class="hero-tags">

        <div class="tag">📖 Qur’aana</div>
        <div class="tag">📚 Barnoota</div>
        <div class="tag">🕌 Da’waa</div>
        <div class="tag">💻 Teknooloojii</div>

      </div>

      <div class="buttons">

        <a href="#about" class="btn btn-primary">
          Waa’ee Kiyya
        </a>

        <a href="#markaza" class="btn btn-outline">
          Markaza Uweysii
        </a>

      </div>

    </div>

  </section>


  <!-- =========================
       ABOUT
  ========================== -->

  <section class="about" id="about">

    <div class="section-title">

      <span>About Me</span>

      <h2>Waa’ee Kiyya</h2>

      <p>
        Nama Qur’aanaa, beekumsa Shari’aa fi jireenya gaarii
        dhaloota keessatti dagaagsuuf hojjetu.
      </p>

    </div>


    <div class="about-grid">

      <div class="card">

        <h3>🌿 Ferhan Shaamil</h3>

        <p>
          Ani Ferhan Shaamil AbdulGafur,
          Barsiisaa Markaza Uweysii Ibnu Aamir,
          Da’ii fi nama dhaloota Qur’aanaa fi
          beekumsa Shari’aa irratti kakaasuudha.
        </p>

        <br>

        <p>
          Kaayyoon koo Qur’aana barsiisuu qofa osoo hin taane,
          dhaloota beekumsa qabu, amala gaarii qabu,
          Rabbii isaa beeku fi jireenya isaa sirriitti ijaaru
          gargaARUudha.
        </p>

      </div>


      <div class="card">

        <h3>💡 Waan Ani Irratti Hojjedhu</h3>

        <div class="skills">

          <div class="skill">📖 Qur’aana</div>
          <div class="skill">🕌 Da’waa</div>
          <div class="skill">📚 Ulūmul-Sharī’ah</div>
          <div class="skill">🌱 Tarbiyaa</div>
          <div class="skill">💻 Software Engineering</div>
          <div class="skill">🌐 Web Development</div>
          <div class="skill">🎨 Digital Design</div>
          <div class="skill">🚀 Technology</div>

        </div>

      </div>

    </div>

  </section>


  <!-- =========================
       MARKAZA
  ========================== -->

  <section class="markaza" id="markaza">

    <div class="section-title">

      <span>Islamic Learning Center</span>

      <h2>Markaza Uweysii Ibnu Aamir</h2>

    </div>


    <div class="markaza-box">

      <h2>
        🌿✨ MARKAZA UWEYSII IBNU AAMIR ✨🌿
      </h2>

      <div class="arabic">
        مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ
        لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ
      </div>

      <div class="markaza-subtitle">
        Iddoo Beekumsa Shari’aa fi Qur’aana Kabajamaa
      </div>

      <p>
        منارة لتعلم العلوم الشرعية والقرآن الكريم
      </p>

      <div class="markaza-quote">
        نُعَلِّمُكَ الْقُرْآنَ كَمَا أُنْزِلَ،
        وَنُرَبِّي الْجِيلَ الْقُرْآنِيَّ الْمُتْقَنَ.
      </div>

      <p>
        Markazni kun bakka Qur’aana,
        Tajwiida, Aqiidaa, Fiqhii, Seeraa Nabiyyii ﷺ
        fi beekumsa Shari’aa itti baratanidha.
      </p>

      <br>

      <a href="#programs" class="btn btn-primary">
        Sagantaalee Barnootaa Ilaali
      </a>

    </div>

  </section>


  <!-- =========================
       PROGRAMS
  ========================== -->

  <section class="programs" id="programs">

    <div class="section-title">

      <span>Our Programs</span>

      <h2>Sagantaalee Barnootaa</h2>

      <p>
        Barnoota bu’uuraa irraa kaasee hanga
        beekumsa Shari’aa fi Qur’aanaa gadi fagoo.
      </p>

    </div>


    <div class="program-grid">


      <div class="program">

        <div class="program-icon">🔤</div>

        <h3>Qaacidda Nooraniyyaa</h3>

        <p>
          Namoota Qur’aana dubbisuu jalqaban,
          daa’immanii fi beginners'f.
        </p>

        <span class="duration">
          BEGINNER
        </span>

      </div>


      <div class="program">

        <div class="program-icon">📖</div>

        <h3>Tilawaa fi Tajwiid</h3>

        <p>
          Sirnaan Qur’aana dubbisuu,
          Makhaarij, Ahkaam fi Tajwiida barachuu.
        </p>

        <span class="duration">
          3 JI’A
        </span>

      </div>


      <div class="program">

        <div class="program-icon">🌙</div>

        <h3>Seenaa Nabiyyii ﷺ</h3>

        <p>
          Jireenya Nabiyyii ﷺ,
          akhlaaqa isaa fi barnoota irraa argamu.
        </p>

        <span class="duration">
          2 JI’A
        </span>

      </div>


      <div class="program">

        <div class="program-icon">🕌</div>

        <h3>Fiqhii fi Ahkaam</h3>

        <p>
          Ahkaama ibaadaa fi jireenya Muslimni
          guyyaa guyyaan itti fayyadamu.
        </p>

        <span class="duration">
          3 JI’A
        </span>

      </div>


      <div class="program">

        <div class="program-icon">☝️</div>

        <h3>Aqiidaa Sirrii</h3>

        <p>
          Bu’uura Tawhiidaa fi Aqiidaa Islaamaa
          irratti hubannoo sirrii ijaaruu.
        </p>

        <span class="duration">
          2 JI’A
        </span>

      </div>


      <div class="program">

        <div class="program-icon">✨</div>

        <h3>Sagantaa Guutuu</h3>

        <p>
          Qur’aana, Tajwiid, Aqiidaa, Fiqhii
          fi Seeraa Nabiyyii ﷺ walitti qabu.
        </p>

        <span class="duration">
          3 JI’A
        </span>

      </div>

    </div>

  </section>


  <!-- =========================
       CURRICULUM
  ========================== -->

  <section class="curriculum" id="curriculum">

    <div class="section-title">

      <span>Curriculum</span>

      <h2>Manhajaa fi Kitaabota</h2>

      <p>
        Barnoonni keenya kitaabota bu’uuraa
        fi madda beekumsa Shari’aa irratti hundaa’a.
      </p>

    </div>


    <div class="book-grid">

      <div class="book">
        <strong>📖 Qaacidda Nooraniyyaa</strong>
        <span>القاعدة النورانية</span>
      </div>

      <div class="book">
        <strong>📚 Tilawaa fi Tajwiid</strong>
        <span>التلاوة والتجويد</span>
      </div>

      <div class="book">
        <strong>☝️ Al-Usuul Ath-Thalaathah</strong>
        <span>الأصول الثلاثة</span>
      </div>

      <div class="book">
        <strong>🕌 Kitaaba Tawhiid</strong>
        <span>كتاب التوحيد</span>
      </div>

      <div class="book">
        <strong>📕 Al-Aqiidatul-Waasixiyyah</strong>
        <span>العقيدة الواسطية</span>
      </div>

      <div class="book">
        <strong>📗 Khudh Aqeedataka</strong>
        <span>خذ عقيدتك</span>
      </div>

      <div class="book">
        <strong>🌙 Seeraa Nabiyyii ﷺ</strong>
        <span>السيرة النبوية</span>
      </div>

      <div class="book">
        <strong>📜 Arba’iin & Bulughul Maraam</strong>
        <span>الأربعون النووية وبلوغ المرام</span>
      </div>

      <div class="book">
        <strong>⚖️ Ahkaama Fiqhii</strong>
        <span>الأحكام الفقهية</span>
      </div>

      <div class="book">
        <strong>🌱 Tarbiyaa fi Akhlaaq</strong>
        <span>التربية والأخلاق</span>
      </div>

    </div>

  </section>


  <!-- =========================
       MESSAGE
  ========================== -->

  <section class="message">

    <div class="message-box">

      <div class="arabic">
        خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ
      </div>

      <p>
        “Irra caalaan keessan nama Qur’aana baratee
        barsiise dha.”
      </p>

      <br>

      <p>
        Kaayyoon keenya Qur’aana si barsiisuu,
        Nabiyyii kee ﷺ si beeksisuu,
        Diinii kee si hubachiisuu,
        Aqiidaa kee sirreessuu fi
        akka Muslimni sirrii taatee jiraattu si gargaaruudha.
      </p>

    </div>

  </section>


  <!-- =========================
       CONTACT
  ========================== -->

  <section class="contact" id="contact">

    <div class="section-title">

      <span>Contact</span>

      <h2>Nu Qunnami</h2>

      <p>
        Barnoota, Da’waa fi Markaza Uweysii Ibnu Aamir
        ilaalchisee nu qunnami.
      </p>

    </div>


    <div class="contact-grid">


      <div class="contact-card">

        <div class="icon">📱</div>

        <h3>Bilbila</h3>

        <p>0915 455 051</p>

      </div>


      <div class="contact-card">

        <div class="icon">💬</div>

        <h3>WhatsApp</h3>

        <p>
          0915 455 051
        </p>

      </div>


      <div class="contact-card">

        <div class="icon">📧</div>

        <h3>Email</h3>

        <p>
          Ferhanshaamil@gmail.com
        </p>

      </div>

    </div>

  </section>


  <!-- =========================
       CTA
  ========================== -->

  <section class="cta">

    <div class="arabic">
      الْقُرْآنُ يَنْتَظِرُكَ! 📖
    </div>

    <h2>
      Beekumsa Baradhu.
    </h2>

    <p>
      Dhaloota Ijaari. Jireenya Keessan Ifa Godhi.
    </p>

    <br>

    <a href="#contact" class="btn btn-primary">
      Amma Nu Qunnami
    </a>

  </section>


  <!-- =========================
       FOOTER
  ========================== -->

  <footer>

    <h3>
      FERHAN SHAAMIL
    </h3>

    <div class="footer-arabic">
      فرحان شامل عبدالغفور
    </div>

    <p>
      داعية ومعلّم للقرآن والعلوم الشرعية
    </p>

    <br>

    <p>
      🌿 Markaza Uweysii Ibnu Aamir
    </p>

    <br>

    <p>
      © 2026 Ferhan Shaamil. All Rights Reserved.
    </p>

  </footer>


  <!-- WHATSAPP -->

  <a
    class="whatsapp"
    href="https://wa.me/251915455051"
    target="_blank"
    aria-label="WhatsApp"
  >
    💬
  </a>


</body>
</html>



