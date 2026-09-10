<!DOCTYPE html>
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
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth}
:root{
  --bg:#040d09;--bg2:#0a1f15;--card:rgba(11,44,30,0.75);
  --gold:#d6b45d;--gold-light:#f2d98d;--green:#0d9e6e;
  --white:#f7f5ed;--text:#d1ddd6;--muted:#98aea4;--border:rgba(214,180,93,0.25);
}
body{
  font-family:'Cairo','Amiri',sans-serif;
  background:radial-gradient(circle at 10% 20%,rgba(214,180,93,0.08),transparent 30%),
             radial-gradient(circle at 90% 70%,rgba(13,158,110,0.15),transparent 35%),
             var(--bg);
  color:var(--white);line-height:1.9;min-height:100vh;overflow-x:hidden;
}
a{color:inherit;text-decoration:none}
.container{width:min(1180px,92%);margin:0 auto}

/* ===== NAVBAR ===== */
nav{position:fixed;top:0;right:0;left:0;z-index:999;
  background:rgba(4,13,9,0.92);backdrop-filter:blur(16px);
  border-bottom:1px solid var(--border);padding:0 5%}
.nav-inner{display:flex;justify-content:space-between;align-items:center;min-height:75px}
.logo{display:flex;align-items:center;gap:12px}
.logo-icon{width:44px;height:44px;border-radius:50%;border:1px solid var(--gold);
  display:grid;place-items:center;font-size:22px;color:var(--gold-light)}
.logo-text strong{display:block;color:var(--gold-light);font-size:15px;letter-spacing:0.5px}
.logo-text small{display:block;color:var(--muted);font-size:9px;font-family:'Amiri',serif}
.nav-links{display:flex;gap:25px;list-style:none;font-size:14px;align-items:center}
.nav-links a{color:var(--text);transition:0.3s;font-weight:600;position:relative;padding:4px 0}
.nav-links a::after{content:'';position:absolute;bottom:0;left:0;width:0;height:2px;
  background:var(--gold);transition:0.3s}
.nav-links a:hover{color:var(--gold-light)}
.nav-links a:hover::after{width:100%}
.nav-cta{border:1px solid var(--gold);padding:8px 18px;border-radius:30px;color:var(--gold-light)!important}
.menu-btn{display:none;font-size:28px;cursor:pointer;color:var(--gold-light);user-select:none}

/* ===== HERO ===== */
.hero{min-height:100vh;display:flex;align-items:center;padding:150px 0 80px;position:relative;overflow:hidden}
.hero::before{content:"";position:absolute;width:500px;height:500px;
  background:radial-gradient(circle,rgba(13,158,110,0.2),transparent 70%);border-radius:50%;
  top:-100px;right:-100px;z-index:-1;animation:float 8s ease-in-out infinite}
.hero::after{content:"";position:absolute;width:400px;height:400px;
  background:radial-gradient(circle,rgba(214,180,93,0.15),transparent 70%);border-radius:50%;
  bottom:-100px;left:-100px;z-index:-1;animation:float 10s ease-in-out infinite reverse}
@keyframes float{0%,100%{transform:translate(0,0)}50%{transform:translate(-30px,30px)}}
.hero-grid{display:grid;grid-template-columns:1.2fr 0.8fr;gap:50px;align-items:center}
.badge{display:inline-block;border:1px solid var(--border);background:rgba(214,180,93,0.08);
  padding:8px 18px;border-radius:40px;color:var(--gold-light);font-size:13px;margin-bottom:20px;
  font-weight:700;animation:pulse 3s ease-in-out infinite}
@keyframes pulse{0%,100%{box-shadow:0 0 0 0 rgba(214,180,93,0.3)}50%{box-shadow:0 0 0 12px rgba(214,180,93,0)}}
.hero h1{font-size:clamp(38px,6vw,70px);line-height:1.1;font-weight:900;letter-spacing:-1px}
.hero h1 span{background:linear-gradient(135deg,var(--gold-light),var(--gold));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.hero-sub{font-size:clamp(20px,3vw,30px);color:var(--gold);margin:15px 0 10px;font-weight:700}
.hero-motto{font-family:'Amiri',serif;font-size:clamp(22px,3.5vw,38px);color:#f5eace;
  margin:15px 0 20px;line-height:1.7;border-right:4px solid var(--gold);padding-right:20px}
.hero-desc{color:var(--muted);font-size:16px;max-width:650px}
.hero-buttons{display:flex;flex-wrap:wrap;gap:15px;margin-top:30px}
.btn{padding:13px 28px;border-radius:35px;font-weight:700;font-size:14px;
  transition:0.3s;display:inline-block;border:1px solid var(--gold);cursor:pointer}
.btn-primary{background:linear-gradient(135deg,var(--gold-light),var(--gold));color:#07130d;border:none}
.btn-primary:hover{transform:translateY(-4px);box-shadow:0 12px 30px rgba(214,180,93,0.3)}
.btn-outline{background:transparent;color:var(--white)}
.btn-outline:hover{background:rgba(214,180,93,0.1);border-color:var(--gold-light)}
.hero-card{border:1px solid var(--border);background:var(--card);backdrop-filter:blur(10px);
  border-radius:35px;padding:35px 25px;text-align:center;box-shadow:0 30px 70px rgba(0,0,0,0.4);transition:0.4s}
.hero-card:hover{transform:translateY(-8px);border-color:var(--gold);box-shadow:0 40px 100px rgba(0,0,0,0.5)}
.hero-symbol{width:130px;height:130px;margin:0 auto 20px;border-radius:50%;
  border:1px solid var(--gold);display:grid;place-items:center;font-size:60px;
  background:radial-gradient(circle,rgba(214,180,93,0.15),transparent 65%);
  box-shadow:0 0 40px rgba(214,180,93,0.25),inset 0 0 30px rgba(214,180,93,0.1);
  animation:glow 4s ease-in-out infinite}
@keyframes glow{0%,100%{box-shadow:0 0 40px rgba(214,180,93,0.25),inset 0 0 30px rgba(214,180,93,0.1)}
  50%{box-shadow:0 0 60px rgba(214,180,93,0.4),inset 0 0 40px rgba(214,180,93,0.2)}}
.hero-card h3{color:var(--gold-light);font-size:22px;margin-bottom:5px}
.hero-card p{color:var(--muted);font-size:13px}
.hero-card .arabic-tag{font-family:'Amiri',serif;font-size:18px;color:#eee4c8;margin-top:12px}

/* ===== SECTIONS ===== */
section{padding:100px 0}
.section-head{text-align:center;max-width:800px;margin:0 auto 55px}
.section-mini{color:var(--gold);text-transform:uppercase;letter-spacing:4px;font-size:12px;font-weight:700}
.section-head h2{font-size:clamp(30px,5vw,48px);margin:10px 0}
.section-head h2 span{color:var(--gold-light)}
.section-head p{color:var(--muted);font-size:15px}
.section-head .arabic-sub{font-family:'Amiri',serif;color:var(--gold-light);font-size:22px;margin-top:5px}

/* ===== MISSION / VISION ===== */
.mission-box{border:1px solid var(--gold);border-radius:32px;padding:60px 30px;
  background:radial-gradient(circle at center,rgba(13,158,110,0.15),transparent 60%),rgba(8,25,18,0.8);
  text-align:center}
.mission-box .big-arabic{font-family:'Amiri',serif;font-size:clamp(28px,4vw,45px);
  color:var(--gold-light);line-height:2}
.mission-box p{color:var(--muted);max-width:800px;margin:20px auto 0;font-size:16px}

/* ===== FEATURES ===== */
.features-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px}
.feature{background:var(--card);border:1px solid var(--border);border-radius:25px;
  padding:32px 25px;text-align:center;transition:0.4s;backdrop-filter:blur(6px);position:relative;overflow:hidden}
.feature::before{content:"";position:absolute;top:0;left:0;width:100%;height:3px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
  transform:translateX(-100%);transition:0.6s}
.feature:hover::before{transform:translateX(0)}
.feature:hover{transform:translateY(-10px);border-color:var(--gold);box-shadow:0 20px 50px rgba(0,0,0,0.3)}
.feature .icon{font-size:45px;margin-bottom:15px}
.feature h3{color:var(--gold-light);font-size:19px;margin-bottom:10px}
.feature p{color:var(--muted);font-size:13px}
.feature .ar-desc{font-family:'Amiri',serif;font-size:14px;color:#c7d4cd;margin-top:8px}

/* ===== TOOLS ===== */
.tools-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}
.tool{background:var(--card);border:1px solid var(--border);border-radius:20px;
  padding:25px 15px;text-align:center;transition:0.3s}
.tool:hover{transform:translateY(-5px);border-color:var(--gold)}
.tool .icon{font-size:32px}
.tool h4{color:var(--gold-light);font-size:15px;margin-top:8px}
.tool span{display:block;color:var(--muted);font-size:11px}

/* ===== CURRICULUM ===== */
.curr-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:15px}
.curr-item{display:flex;gap:18px;align-items:center;background:var(--card);
  border:1px solid var(--border);border-radius:18px;padding:20px;transition:0.3s}
.curr-item:hover{transform:translateX(-5px);border-color:var(--gold)}
.curr-item .lvl{font-size:28px}
.curr-item h4{color:var(--gold-light);font-size:16px}
.curr-item p{color:var(--muted);font-size:12px}

/* ===== SOCIAL ===== */
.social-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;max-width:900px;margin:0 auto}
.social-card{background:var(--card);border:1px solid var(--border);border-radius:25px;
  padding:30px 20px;text-align:center;transition:0.4s;position:relative;overflow:hidden}
.social-card::before{content:"";position:absolute;top:-50%;left:-50%;width:200%;height:200%;
  background:radial-gradient(circle,rgba(214,180,93,0.08),transparent 60%);opacity:0;transition:0.5s}
.social-card:hover{transform:translateY(-8px);border-color:var(--gold);box-shadow:0 15px 40px rgba(0,0,0,0.3)}
.social-card:hover::before{opacity:1}
.social-card .s-icon{font-size:40px;margin-bottom:12px;position:relative;z-index:1;transition:0.3s}
.social-card:hover .s-icon{transform:scale(1.15)}
.social-card h4{color:var(--gold-light);font-size:18px;margin-bottom:5px;position:relative;z-index:1}
.social-card a{display:inline-block;color:var(--muted);font-size:13px;word-break:break-word;
  transition:0.3s;position:relative;z-index:1;border-bottom:1px solid transparent}
.social-card a:hover{color:var(--white);border-bottom-color:var(--gold)}

/* ===== CTA ===== */
.cta{text-align:center;padding:100px 20px;
  background:radial-gradient(circle,rgba(214,180,93,0.1),transparent 55%);position:relative;overflow:hidden}
.cta .arabic{font-family:'Amiri',serif;font-size:35px;color:var(--gold-light)}
.cta h2{font-size:clamp(32px,5vw,52px);color:var(--white);margin:15px 0}
.cta p{color:var(--muted);max-width:600px;margin:0 auto 30px}

/* ===== FOOTER ===== */
footer{border-top:1px solid var(--border);background:#020906;padding:45px 0;text-align:center}
footer strong{color:var(--gold-light);font-size:16px}
footer .ar{font-family:'Amiri',serif;color:#d4cbaa;font-size:20px;margin:5px 0}
footer p{color:var(--muted);font-size:12px;margin:4px 0}
.footer-socials{margin-top:15px;display:flex;justify-content:center;gap:18px;flex-wrap:wrap}
.footer-socials a{color:var(--muted);font-size:24px;transition:0.3s;display:inline-block}
.footer-socials a:hover{color:var(--gold-light);transform:scale(1.15) translateY(-3px)}

/* ===== WHATSAPP ===== */
.wa{position:fixed;bottom:20px;left:20px;width:55px;height:55px;border-radius:50%;
  background:linear-gradient(135deg,#25d366,#128c7e);display:grid;place-items:center;
  font-size:28px;z-index:500;box-shadow:0 10px 30px rgba(0,0,0,0.5);transition:0.3s;
  animation:waPulse 2s ease-in-out infinite}
.wa:hover{transform:scale(1.1);box-shadow:0 15px 45px rgba(37,211,102,0.6)}
@keyframes waPulse{0%,100%{box-shadow:0 10px 30px rgba(37,211,102,0.4)}
  50%{box-shadow:0 10px 30px rgba(37,211,102,0.4),0 0 0 15px rgba(37,211,102,0)}}

/* ===== RESPONSIVE ===== */
@media(max-width:900px){
  .nav-links{position:absolute;top:75px;left:0;width:100%;background:var(--bg2);
    flex-direction:column;padding:25px;gap:15px;display:none;border-bottom:1px solid var(--border)}
  .nav-links.active{display:flex}
  .menu-btn{display:block}
  .hero-grid{grid-template-columns:1fr;text-align:center}
  .hero-motto{border-right:none;padding-right:0;text-align:center}
  .hero-desc{margin:0 auto}
  .hero-buttons{justify-content:center}
  .features-grid{grid-template-columns:1fr 1fr}
  .tools-grid{grid-template-columns:1fr 1fr}
  .curr-grid{grid-template-columns:1fr}
  .social-grid{grid-template-columns:1fr 1fr}
}
@media(max-width:550px){
  .features-grid,.tools-grid,.social-grid{grid-template-columns:1fr}
  .hero{padding-top:120px}
  section{padding:70px 0}
  .mission-box{padding:40px 20px}
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
        <strong>مَرْكَزُ أُوَيْسِ بْنِ عَامِرٍ</strong>
        <small>لِدِرَاسَةِ الْعُلُومِ الشَّرْعِيَّةِ</small>
      </div>
    </a>
    <div class="menu-btn" onclick="toggleMenu()">☰</div>
    <ul class="nav-links" id="navLinks">
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

<!-- ===== VISION ===== -->
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
      <p style="margin-top:15px;font-family:'Amiri',serif;color:var(--gold-light);font-size:20px;">
        "مِنَ الْكِتَابِ إِلَى التِّقْنِيَةِ، وَمِنَ التَّعَلُّمِ إِلَى التَّمَيُّزِ"
      </p>
    </div>
  </div>
</section>

<!-- ===== FEATURES ===== -->
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

<!-- ===== TOOLS ===== -->
<section id="tools" style="background:rgba(7,22,15,0.6);">
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

<!-- ===== SOCIAL ===== -->
<section id="social" style="background:rgba(7,22,15,0.4);">
  <div class="container">
    <div class="section-head">
      <div class="section-mini">تَابِعُونَا</div>
      <h2>وَسَائِلُ التَّوَاصُلِ الِاجْتِمَاعِيِّ</h2>
      <p>اِنْضَمَّ إِلَيْنَا عَلَى مَنَصَّاتِنَا الرَّقْمِيَّةِ لِتُوَاصِلَ التَّعَلُّمَ وَالدَّعْوَةَ</p>
    </div>
    <div class="social-grid">
      <div class="social-card">
        <div class="s-icon">📘</div>
        <h4>فَيْسْبُوك</h4>
        <a href="https://www.facebook.com/share/1D9P96HFwe/" target="_blank">facebook.com/share/1D9P96HFwe</a>
      </div>
      <div class="social-card">
        <div class="s-icon">🎵</div>
        <h4>تِيكْ توك</h4>
        <a href="https://www.tiktok.com/@mirkanihararge" target="_blank">@mirkanihararge</a>
      </div>
      <div class="social-card">
        <div class="s-icon">▶️</div>
        <h4>يُوتْيُوب</h4>
        <a href="https://youtube.com/@ferhanshaamil" target="_blank">@ferhanshaamil</a>
      </div>
      <div class="social-card">
        <div class="s-icon">✈️</div>
        <h4>تِلِغْرَام</h4>
        <a href="https://t.me/Ferhan_Shaamil" target="_blank">t.me/Ferhan_Shaamil</a>
      </div>
      <div class="social-card">
        <div class="s-icon">💬</div>
        <h4>وَاتْسَاب</h4>
        <a href="https://wa.me/251915455051" target="_blank">+251 915 455 051</a>
      </div>
      <div class="social-card">
        <div class="s-icon">📧</div>
        <h4>اَلْبَرِيدُ</h4>
        <a href="mailto:Ferhanshaamil@gmail.com">Ferhanshaamil@gmail.com</a>
      </div>
    </div>
  </div>
</section>

<!-- ===== CTA ===== -->
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
    <p><strong>فَرْحَانُ شَامِلٌ</strong> — مُدَرِّسُ الْمَرْكَزِ</p>
    <p style="font-size:13px;color:var(--gold-light);">
      دَاعِيَةٌ • مُعَلِّمُ الْقُرْآنِ وَالْعُلُومِ الشَّرْعِيَّةِ • طَالِبُ هَنْدَسَةِ الْبَرْمَجِيَّاتِ
    </p>
    <div class="footer-socials">
      <a href="https://www.facebook.com/share/1D9P96HFwe/" target="_blank" title="Facebook">📘</a>
      <a href="https://www.tiktok.com/@mirkanihararge" target="_blank" title="TikTok">🎵</a>
      <a href="https://youtube.com/@ferhanshaamil" target="_blank" title="YouTube">▶️</a>
      <a href="https://t.me/Ferhan_Shaamil" target="_blank" title="Telegram">✈️</a>
      <a href="https://wa.me/251915455051" target="_blank" title="WhatsApp">💬</a>
      <a href="mailto:Ferhanshaamil@gmail.com" title="Email">📧</a>
    </div>
    <p style="margin-top:15px;">© 2026 جَمِيعُ الْحُقُوقِ مَحْفُوظَةٌ</p>
  </div>
</footer>

<!-- ===== WHATSAPP ===== -->
<a href="https://wa.me/251915455051" target="_blank" class="wa" title="واتساب">💬</a>

<script>
function toggleMenu(){document.getElementById("navLinks").classList.toggle("active")}
document.querySelectorAll(".nav-links a").forEach(l=>l.addEventListener("click",()=>document.getElementById("navLinks").classList.remove("active")));
window.addEventListener('scroll',()=>{
  document.getElementById('navbar').style.boxShadow=window.scrollY>50?'0 10px 40px rgba(0,0,0,0.4)':'none';
});
</script>

</body>
</html>
