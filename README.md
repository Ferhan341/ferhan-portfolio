<!DOCTYPE html>
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
      gap: 20px;
      list-style: none;
      font-size: 13px;
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
      font-size: clamp(18px, 2.5vw, 24px);
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

    /* ===== WORK / SERVICES ===== */
    .work-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
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
      font-size: 17px;
      margin-bottom: 8px;
    }

    .work-item p {
      color: var(--muted);
      font-size: 13px;
    }

    /* ===== EDUCATION / PROGRAMS ===== */
    .edu-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .edu-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 28px 22px;
      transition: 0.4s;
      position: relative;
      overflow: hidden;
    }

    .edu-card:hover {
      transform: translateY(-7px);
      border-color: var(--gold);
    }

    .edu-card::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: linear-gradient(90deg, var(--gold), var(--gold-light));
    }

    .edu-card .icon {
      font-size: 38px;
      margin-bottom: 12px;
    }

    .edu-card h4 {
      color: var(--gold-light);
      font-size: 18px;
      margin-bottom: 8px;
    }

    .edu-card p {
      color: var(--muted);
      font-size: 13px;
    }

    .edu-card .duration {
      display: inline-block;
      margin-top: 14px;
      padding: 5px 14px;
      border-radius: 20px;
      background: rgba(214, 180, 93, 0.1);
      border: 1px solid var(--border);
      color: var(--gold-light);
      font-size: 12px;
      font-weight: 700;
    }

    /* ===== MATERIALS BUTTONS ===== */
    .materials {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 16px;
      padding-top: 16px;
      border-top: 1px solid var(--border);
    }

    .mat-btn {
      display: inline-flex;
      align-items: center;
      gap: 5px;
      padding: 7px 13px;
      border-radius: 20px;
      font-size: 11px;
      font-weight: 700;
      transition: 0.3s;
      border: 1px solid var(--border);
      background: rgba(255, 255, 255, 0.03);
      color: var(--text);
    }

    .mat-btn:hover {
      transform: translateY(-2px);
    }

    .mat-btn.pdf {
      color: #ff8a8a;
      border-color: rgba(255, 138, 138, 0.3);
    }
    .mat-btn.pdf:hover {
      background: rgba(255, 138, 138, 0.1);
      border-color: #ff8a8a;
    }

    .mat-btn.video {
      color: #8ac6ff;
      border-color: rgba(138, 198, 255, 0.3);
    }
    .mat-btn.video:hover {
      background: rgba(138, 198, 255, 0.1);
      border-color: #8ac6ff;
    }

    .mat-btn.audio {
      color: #8affb5;
      border-color: rgba(138, 255, 181, 0.3);
    }
    .mat-btn.audio:hover {
      background: rgba(138, 255, 181, 0.1);
      border-color: #8affb5;
    }

    .mat-btn.text {
      color: var(--gold-light);
      border-color: var(--border);
    }
    .mat-btn.text:hover {
      background: rgba(214, 180, 93, 0.1);
      border-color: var(--gold);
    }

    /* ===== SCHEDULE ===== */
    .schedule-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
      max-width: 800px;
      margin: 0 auto;
    }

    .schedule-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 35px 25px;
      text-align: center;
      transition: 0.4s;
    }

    .schedule-card:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
    }

    .schedule-card .icon {
      font-size: 45px;
      margin-bottom: 12px;
    }

    .schedule-card h4 {
      color: var(--gold-light);
      font-size: 20px;
      margin-bottom: 10px;
    }

    .schedule-card p {
      color: var(--text);
      font-size: 16px;
      font-weight: 600;
    }

    /* ===== MARKAZA ===== */
    .markaza-box {
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 55px 30px;
      background: radial-gradient(circle at center, rgba(13, 158, 110, 0.12), transparent 60%), rgba(8, 25, 18, 0.8);
      text-align: center;
    }

    .markaza-box h2 {
      color: var(--gold-light);
      font-size: clamp(28px, 4vw, 42px);
      margin-bottom: 15px;
    }

    .markaza-box p {
      color: var(--muted);
      max-width: 800px;
      margin: 0 auto 12px;
      font-size: 16px;
    }

    /* ===== VISION ===== */
    .vision-box {
      border: 1px solid var(--gold);
      border-radius: 32px;
      padding: 50px 30px;
      background: radial-gradient(circle at center, rgba(13, 158, 110, 0.12), transparent 60%), rgba(8, 25, 18, 0.8);
      text-align: center;
    }

    .vision-box p {
      color: var(--muted);
      max-width: 800px;
      margin: 0 auto;
      font-size: 16px;
    }

    /* ===== MESSAGE ===== */
    .message-box {
      border: 1px solid var(--border);
      border-radius: 28px;
      padding: 45px 30px;
      background: var(--card);
      text-align: center;
    }

    .message-box blockquote {
      font-size: clamp(22px, 3.5vw, 34px);
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

    /* ===== PROJECTS ===== */
    .project-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .project {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 28px;
      transition: 0.4s;
    }

    .project:hover {
      transform: translateY(-6px);
      border-color: var(--gold);
    }

    .project h4 {
      color: var(--gold-light);
      font-size: 18px;
      margin-bottom: 10px;
    }

    .project p {
      color: var(--muted);
      font-size: 13px;
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
      .edu-grid {
        grid-template-columns: 1fr 1fr;
      }
      .project-grid {
        grid-template-columns: 1fr;
      }
      .social-grid {
        grid-template-columns: 1fr 1fr;
      }
      .schedule-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 550px) {
      .work-grid,
      .edu-grid,
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
      .markaza-box {
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
          <strong>FERHAN SHAAMIL</strong>
          <small>Markaza Uweysii Ibnu Aamir</small>
        </div>
      </a>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#work">Work</a></li>
        <li><a href="#education">Barnoota</a></li>
        <li><a href="#markaza">Markaza</a></li>
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
          <a href="#education" class="btn btn-outline">📚 Barnoota</a>
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

  <!-- ===== EDUCATION / PROGRAMS WITH MATERIALS ===== -->
  <section id="education">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">Education Programs</div>
        <h2>📚 Sagantaalee Barnootaa</h2>
        <p>Barnoota Qur'aanaa fi Beekumsa Shari'aa sadarkaa adda addaatiin.</p>
      </div>

      <div class="edu-grid">

        <!-- 1. QAACIDDA NOORANIYYAA -->
        <div class="edu-card">
          <div class="icon">🔤</div>
          <h4>Qaacidda Nooraniyyaa</h4>
          <p>Sadarkaa jalqabaa fi daa'immaniif.</p>
          <span class="duration">🌱 Jalqabaaf</span>
          <div class="materials">
            <a href="#" class="mat-btn pdf">📄 PDF</a>
            <a href="#" class="mat-btn video">🎥 Video</a>
            <a href="#" class="mat-btn audio">🎧 Sagalee</a>
            <a href="#" class="mat-btn text">📝 Barreeffama</a>
          </div>
        </div>

        <!-- 2. TILAWAA FI TAJWIID -->
        <div class="edu-card">
          <div class="icon">📖</div>
          <h4>Tilawaa fi Tajwiid</h4>
          <p>Makhaarij, Sifaat fi Ahkaama Tajwiid.</p>
          <span class="duration">⏳ 3 Ji'a</span>
          <div class="materials">
            <a href="#" class="mat-btn pdf">📄 PDF</a>
            <a href="#" class="mat-btn video">🎥 Video</a>
            <a href="#" class="mat-btn audio">🎧 Sagalee</a>
            <a href="#" class="mat-btn text">📝 Barreeffama</a>
          </div>
        </div>

        <!-- 3. AQIIDAA -->
        <div class="edu-card">
          <div class="icon">☝️</div>
          <h4>Aqiidaa</h4>
          <p>Tawhiida fi bu'uura Aqiidaa Islaamaa.</p>
          <span class="duration">⏳ 2 Ji'a</span>
          <div class="materials">
            <a href="#" class="mat-btn pdf">📄 PDF</a>
            <a href="#" class="mat-btn video">🎥 Video</a>
            <a href="#" class="mat-btn audio">🎧 Sagalee</a>
            <a href="#" class="mat-btn text">📝 Barreeffama</a>
          </div>
        </div>

        <!-- 4. FIQHII FI AHKAAM -->
        <div class="edu-card">
          <div class="icon">⚖️</div>
          <h4>Fiqhii fi Ahkaam</h4>
          <p>Ahkaama ibaadaa fi jireenyaa.</p>
          <span class="duration">⏳ 3 Ji'a</span>
          <div class="materials">
            <a href="#" class="mat-btn pdf">📄 PDF</a>
            <a href="#" class="mat-btn video">🎥 Video</a>
            <a href="#" class="mat-btn audio">🎧 Sagalee</a>
            <a href="#" class="mat-btn text">📝 Barreeffama</a>
          </div>
        </div>

        <!-- 5. SEENAA NABIYYII ﷺ -->
        <div class="edu-card">
          <div class="icon">🌙</div>
          <h4>Seenaa Nabiyyii ﷺ</h4>
          <p>Jireenya fi Akhlaaqa Nabiyyii ﷺ.</p>
          <span class="duration">⏳ 2 Ji'a</span>
          <div class="materials">
            <a href="#" class="mat-btn pdf">📄 PDF</a>
            <a href="#" class="mat-btn video">🎥 Video</a>
            <a href="#" class="mat-btn audio">🎧 Sagalee</a>
            <a href="#" class="mat-btn text">📝 Barreeffama</a>
          </div>
        </div>

        <!-- 6. SAGANTAA GUUTUU -->
        <div class="edu-card">
          <div class="icon">✨</div>
          <h4>Sagantaa Guutuu</h4>
          <p>Qur'aana, Tajwiida, Aqiidaa, Fiqhii fi Seeraa.</p>
          <span class="duration">⏳ Ji'a 4</span>
          <div class="materials">
            <a href="#" class="mat-btn pdf">📄 PDF</a>
            <a href="#" class="mat-btn video">🎥 Video</a>
            <a href="#" class="mat-btn audio">🎧 Sagalee</a>
            <a href="#" class="mat-btn text">📝 Barreeffama</a>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ===== SCHEDULE ===== -->
  <section style="background: rgba(7, 22, 15, 0.4);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">Learning Schedule</div>
        <h2>📅 Sagantaa</h2>
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
        <h2>🌿 Markaza Uweysii</h2>
        <p>Iddoo Qur'aanaa, Beekumsa Shari'aa fi Tarbiyaa.</p>
      </div>
      <div class="markaza-box">
        <h2>🌿✨ MARKAZA UWEYSII IBNU AAMIR ✨🌿</h2>
        <p>
          Markazni Uweysii Ibnu Aamir iddoo Qur'aana, Tajwiida, Aqiidaa, Fiqhii, Seenaa Nabiyyii ﷺ fi Akhlaaqa itti baratan.
        </p>
      </div>
    </div>
  </section>

  <!-- ===== VISION ===== -->
  <section id="vision" style="background: rgba(7, 22, 15, 0.3);">
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
  <section>
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

  <!-- ===== PROJECTS ===== -->
  <section style="background: rgba(7, 22, 15, 0.4);">
    <div class="container">
      <div class="section-head">
        <div class="section-mini">My Work</div>
        <h2>🚀 Projects</h2>
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

  <!-- ===== SOCIAL MEDIA ===== -->
  <section id="social">
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
          <a href="ht
      
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
</html>
