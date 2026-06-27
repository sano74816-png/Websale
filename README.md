<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WebSale — Готовые сайты</title>
<link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}

:root{
  --bg:#0B0C10;
  --surface:#13151C;
  --card:#1A1D28;
  --accent:#6C63FF;
  --accent2:#FF6B6B;
  --cyan:#4ECDC4;
  --white:#F5F6FA;
  --muted:#6B7280;
  --muted2:#9CA3AF;
  --border:rgba(255,255,255,0.07);
}

html{scroll-behavior:smooth}
body{font-family:'Manrope',sans-serif;background:var(--bg);color:var(--white);overflow-x:hidden;line-height:1.6}

/* ── NAV ── */
nav{
  position:fixed;top:0;left:0;right:0;z-index:100;
  display:flex;align-items:center;justify-content:space-between;
  padding:0 5%;height:64px;
  background:rgba(11,12,16,0.8);
  backdrop-filter:blur(20px);
  border-bottom:1px solid var(--border);
}
.logo{font-size:1.3rem;font-weight:800;letter-spacing:-.5px;color:var(--white)}
.logo span{color:var(--accent)}
.nav-r{display:flex;align-items:center;gap:1.5rem}
.nav-r a{color:var(--muted2);text-decoration:none;font-size:.85rem;font-weight:500;transition:color.2s}
.nav-r a:hover{color:var(--white)}
.cta-nav{
  background:var(--accent);color:#fff;border:none;
  padding:9px 20px;border-radius:8px;font-family:inherit;
  font-size:.85rem;font-weight:700;cursor:pointer;
  transition:opacity.2s,transform.2s;
}
.cta-nav:hover{opacity:.85;transform:translateY(-1px)}

/* ── HERO ── */
.hero{
  min-height:100vh;display:flex;flex-direction:column;
  align-items:center;justify-content:center;
  text-align:center;padding:100px 5% 60px;
  position:relative;overflow:hidden;
}
.hero-blob{
  position:absolute;width:600px;height:600px;border-radius:50%;
  background:radial-gradient(circle,rgba(108,99,255,0.12),transparent 70%);
  top:50%;left:50%;transform:translate(-50%,-55%);pointer-events:none;
}
.hero-blob2{
  position:absolute;width:400px;height:400px;border-radius:50%;
  background:radial-gradient(circle,rgba(78,205,196,0.08),transparent 70%);
  bottom:10%;right:5%;pointer-events:none;
}
.chip{
  display:inline-flex;align-items:center;gap:6px;
  background:rgba(108,99,255,0.12);border:1px solid rgba(108,99,255,0.3);
  border-radius:50px;padding:5px 14px;
  font-size:.72rem;font-weight:700;letter-spacing:.1em;
  color:var(--accent);text-transform:uppercase;margin-bottom:24px;
}
.dot-live{width:6px;height:6px;border-radius:50%;background:var(--cyan);
  box-shadow:0 0 8px var(--cyan);animation:blink 2s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}

.hero h1{
  font-size:clamp(2.4rem,6vw,4.8rem);font-weight:800;
  line-height:1.08;letter-spacing:-2px;max-width:780px;margin-bottom:20px;
}
.hero h1 .hi{
  background:linear-gradient(135deg,var(--accent),var(--cyan));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
}
.hero p{color:var(--muted2);font-size:1rem;max-width:460px;margin-bottom:36px}
.hero-btns{display:flex;gap:12px;flex-wrap:wrap;justify-content:center}
.btn-main{
  background:var(--accent);color:#fff;border:none;
  padding:13px 28px;border-radius:10px;font-family:inherit;
  font-size:.9rem;font-weight:700;cursor:pointer;text-decoration:none;
  transition:all.22s;box-shadow:0 4px 20px rgba(108,99,255,0.35);
}
.btn-main:hover{transform:translateY(-2px);box-shadow:0 8px 30px rgba(108,99,255,0.5)}
.btn-sec{
  background:rgba(255,255,255,0.06);color:var(--muted2);
  border:1px solid var(--border);
  padding:13px 28px;border-radius:10px;font-family:inherit;
  font-size:.9rem;font-weight:600;cursor:pointer;text-decoration:none;
  transition:all.22s;
}
.btn-sec:hover{background:rgba(255,255,255,0.1);color:var(--white)}

/* stats row */
.stats{
  display:flex;gap:0;margin-top:60px;
  border:1px solid var(--border);border-radius:14px;overflow:hidden;
}
.s{
  flex:1;padding:22px 28px;text-align:center;
  border-right:1px solid var(--border);
}
.s:last-child{border-right:none}
.s strong{display:block;font-size:1.8rem;font-weight:800;letter-spacing:-1px;color:var(--white)}
.s span{font-size:.72rem;color:var(--muted);text-transform:uppercase;letter-spacing:.07em}

/* ── SECTIONS ── */
.sec{padding:80px 5%;position:relative;z-index:1}
.sec-dark{background:var(--surface)}
.sec-head{margin-bottom:48px}
.sec-label{
  font-size:.7rem;font-weight:700;letter-spacing:.14em;
  color:var(--accent);text-transform:uppercase;margin-bottom:10px;
}
.sec-title{font-size:clamp(1.7rem,3.5vw,2.6rem);font-weight:800;letter-spacing:-1px;line-height:1.15}
.sec-sub{color:var(--muted2);font-size:.9rem;margin-top:8px;max-width:440px}

/* ── CARDS GRID ── */
.grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.grid2{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}

/* ── SITE CARDS ── */
.site-card{
  background:var(--card);border:1px solid var(--border);
  border-radius:16px;overflow:hidden;cursor:pointer;
  transition:transform.3s cubic-bezier(.22,1,.36,1),border-color.3s,box-shadow.3s;
}
.site-card:hover{
  transform:translateY(-8px) scale(1.01);
  border-color:rgba(108,99,255,0.4);
  box-shadow:0 24px 60px rgba(0,0,0,0.5),0 0 40px rgba(108,99,255,0.08);
}
.card-preview{height:160px;position:relative;overflow:hidden}
.card-inner{
  position:absolute;inset:0;padding:14px 16px;
  display:flex;flex-direction:column;
}
.cb{display:flex;gap:4px;margin-bottom:12px}
.cb span{width:8px;height:8px;border-radius:50%}
.cb span:nth-child(1){background:#FF5F57}
.cb span:nth-child(2){background:#FEBC2E}
.cb span:nth-child(3){background:#28C840}
.cl{border-radius:4px;margin-bottom:7px;opacity:.55}
.card-info{padding:18px}
.c-tag{
  font-size:.65rem;font-weight:700;letter-spacing:.08em;
  text-transform:uppercase;color:var(--cyan);
  background:rgba(78,205,196,0.1);border-radius:4px;
  padding:2px 8px;display:inline-block;margin-bottom:8px;
}
.c-name{font-size:.95rem;font-weight:700;margin-bottom:4px}
.c-bot{display:flex;align-items:center;justify-content:space-between;margin-top:12px}
.c-price{font-size:1rem;font-weight:800;color:var(--white)}
.c-old{font-size:.75rem;color:var(--muted);text-decoration:line-through;margin-left:6px}
.c-buy{
  background:rgba(108,99,255,0.15);color:var(--accent);
  border:1px solid rgba(108,99,255,0.3);border-radius:7px;
  padding:6px 14px;font-size:.78rem;font-weight:700;
  cursor:pointer;transition:all.2s;font-family:inherit;
}
.c-buy:hover{background:rgba(108,99,255,0.3)}

/* card themes */
.t-rest .card-inner{background:linear-gradient(150deg,#0F0500,#2A1000)}
.t-rest .cl{background:linear-gradient(90deg,#FF6B35,#FF9A5C)}
.t-beauty .card-inner{background:linear-gradient(150deg,#100020,#280050)}
.t-beauty .cl{background:linear-gradient(90deg,#C77DFF,#E0AAFF)}
.t-tech .card-inner{background:linear-gradient(150deg,#001020,#002848)}
.t-tech .cl{background:linear-gradient(90deg,#6C63FF,#4ECDC4)}
.t-fit .card-inner{background:linear-gradient(150deg,#001800,#003000)}
.t-fit .cl{background:linear-gradient(90deg,#39FF14,#A8FF78)}
.t-hotel .card-inner{background:linear-gradient(150deg,#181000,#302000)}
.t-hotel .cl{background:linear-gradient(90deg,#FFD700,#FFE566)}
.t-med .card-inner{background:linear-gradient(150deg,#001520,#003040)}
.t-med .cl{background:linear-gradient(90deg,#4ECDC4,#80F4FF)}

/* ── FEATURES ── */
.feat-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.feat{
  background:var(--card);border:1px solid var(--border);
  border-radius:14px;padding:26px 22px;
  transition:border-color.25s,transform.25s;
}
.feat:hover{border-color:rgba(108,99,255,0.3);transform:translateY(-3px)}
.feat-icon{font-size:1.6rem;margin-bottom:14px}
.feat h3{font-size:.9rem;font-weight:700;margin-bottom:6px}
.feat p{font-size:.8rem;color:var(--muted2);line-height:1.55}

/* ── PRICING ── */
.plans{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;align-items:start}
.plan{
  background:var(--card);border:1px solid var(--border);
  border-radius:16px;padding:30px 26px;position:relative;
}
.plan.pop{
  border-color:rgba(108,99,255,0.5);
  box-shadow:0 0 0 1px rgba(108,99,255,0.15),0 20px 60px rgba(108,99,255,0.1);
  background:linear-gradient(160deg,#16182A,#0E1020);
}
.plan-badge{
  position:absolute;top:-12px;left:50%;transform:translateX(-50%);
  background:var(--accent);color:#fff;border-radius:50px;
  padding:4px 16px;font-size:.68rem;font-weight:800;
  text-transform:uppercase;letter-spacing:.1em;white-space:nowrap;
}
.plan-n{font-size:.7rem;font-weight:700;text-transform:uppercase;
  letter-spacing:.1em;color:var(--muted);margin-bottom:12px}
.plan-p{font-size:2.2rem;font-weight:800;letter-spacing:-1.5px;margin-bottom:4px}
.plan-p small{font-size:.9rem;font-weight:500;letter-spacing:0}
.plan-per{font-size:.78rem;color:var(--muted);margin-bottom:22px}
.plan hr{border:none;border-top:1px solid var(--border);margin-bottom:18px}
.plan ul{list-style:none;margin-bottom:24px}
.plan ul li{font-size:.82rem;color:var(--muted2);padding:6px 0;
  display:flex;align-items:flex-start;gap:8px}
.plan ul li .ck{color:var(--cyan);flex-shrink:0;margin-top:1px}
.plan ul li.no{opacity:.35}
.plan ul li.no .ck{color:var(--muted)}
.plan-btn{
  width:100%;padding:11px;border-radius:9px;font-family:inherit;
  font-size:.85rem;font-weight:700;cursor:pointer;transition:all.2s;border:none;
}
.plan-btn-main{background:var(--accent);color:#fff;
  box-shadow:0 4px 16px rgba(108,99,255,0.35)}
.plan-btn-main:hover{opacity:.85}
.plan-btn-ghost{background:rgba(255,255,255,0.06);color:var(--muted2);
  border:1px solid var(--border)}
.plan-btn-ghost:hover{background:rgba(255,255,255,0.1);color:var(--white)}

/* ── REVIEWS ── */
.rev-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.rev{
  background:var(--card);border:1px solid var(--border);
  border-radius:14px;padding:24px 22px;
  transition:border-color.25s,transform.25s;
}
.rev:hover{border-color:rgba(108,99,255,0.25);transform:translateY(-3px)}
.rev-stars{color:#FFD700;font-size:.85rem;letter-spacing:2px;margin-bottom:10px}
.rev-text{font-size:.82rem;color:var(--muted2);line-height:1.6;margin-bottom:16px}
.rev-author{display:flex;align-items:center;gap:10px}
.rev-av{
  width:36px;height:36px;border-radius:50%;flex-shrink:0;
  display:flex;align-items:center;justify-content:center;
  font-size:.8rem;font-weight:800;color:#fff;
}
.rev-name{font-size:.82rem;font-weight:700}
.rev-role{font-size:.72rem;color:var(--muted)}

/* ── CTA BOX ── */
.cta-wrap{
  background:linear-gradient(135deg,rgba(108,99,255,0.12),rgba(78,205,196,0.06));
  border:1px solid rgba(108,99,255,0.2);border-radius:20px;
  padding:60px 40px;text-align:center;position:relative;overflow:hidden;
}
.cta-wrap::before{
  content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,rgba(108,99,255,0.6),transparent);
}
.cta-wrap h2{font-size:clamp(1.8rem,4vw,2.8rem);font-weight:800;
  letter-spacing:-1px;margin-bottom:14px}
.cta-wrap p{color:var(--muted2);font-size:.9rem;max-width:400px;margin:0 auto 32px}

/* ── FOOTER ── */
footer{
  border-top:1px solid var(--border);padding:28px 5%;
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:12px;
}
footer p{font-size:.78rem;color:var(--muted)}
.f-links{display:flex;gap:20px}
.f-links a{font-size:.78rem;color:var(--muted);text-decoration:none;transition:color.2s}
.f-links a:hover{color:var(--white)}
.f-logo{font-size:1.1rem;font-weight:800;color:var(--white)}
.f-logo span{color:var(--accent)}

/* ── MODAL ── */
.overlay{
  position:fixed;inset:0;z-index:500;
  background:rgba(11,12,16,0.85);backdrop-filter:blur(14px);
  display:flex;align-items:center;justify-content:center;padding:20px;
  opacity:0;pointer-events:none;transition:opacity.25s;
}
.overlay.open{opacity:1;pointer-events:all}
.modal{
  background:#13151C;border:1px solid rgba(108,99,255,0.25);
  border-radius:20px;padding:40px 34px;width:100%;max-width:440px;
  transform:translateY(20px) scale(.97);
  transition:transform.3s cubic-bezier(.22,1,.36,1);position:relative;
}
.modal::before{
  content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,rgba(108,99,255,0.7),transparent);
}
.overlay.open .modal{transform:translateY(0) scale(1)}
.modal h3{font-size:1.4rem;font-weight:800;margin-bottom:6px;letter-spacing:-.4px}
.modal>.sub{color:var(--muted2);font-size:.85rem;margin-bottom:26px}
.fg{margin-bottom:13px}
.fg label{display:block;font-size:.72rem;font-weight:700;
  letter-spacing:.06em;text-transform:uppercase;color:var(--muted);margin-bottom:6px}
.fg input,.fg select{
  width:100%;padding:11px 13px;
  background:rgba(255,255,255,0.05);border:1px solid var(--border);
  border-radius:9px;color:var(--white);font-family:inherit;font-size:.88rem;
  outline:none;transition:border-color.2s;
}
.fg input:focus,.fg select:focus{border-color:rgba(108,99,255,0.5)}
.fg input::placeholder{color:var(--muted)}
.fg select option{background:#13151C}
.m-btns{display:flex;gap:10px;margin-top:20px}
.m-cancel{
  background:rgba(255,255,255,0.05);border:1px solid var(--border);
  color:var(--muted2);border-radius:9px;padding:11px 18px;
  cursor:pointer;font-family:inherit;font-size:.85rem;transition:all.2s;
}
.m-cancel:hover{background:rgba(255,255,255,0.09);color:var(--white)}
.m-send{
  flex:1;background:var(--accent);color:#fff;border:none;
  border-radius:9px;padding:11px;font-family:inherit;
  font-size:.85rem;font-weight:700;cursor:pointer;transition:opacity.2s;
}
.m-send:hover{opacity:.85}

/* ── TOAST ── */
.toast{
  position:fixed;bottom:28px;left:50%;transform:translateX(-50%) translateY(60px);
  z-index:999;background:rgba(78,205,196,0.12);border:1px solid rgba(78,205,196,0.35);
  backdrop-filter:blur(16px);border-radius:10px;padding:12px 22px;
  font-size:.85rem;font-weight:600;color:var(--cyan);
  transition:transform.4s cubic-bezier(.22,1,.36,1),opacity.4s;opacity:0;
}
.toast.show{transform:translateX(-50%) translateY(0);opacity:1}

/* ── SCROLL REVEAL ── */
.sr{
  opacity:0;transform:translateY(36px);
  transition:opacity.6s cubic-bezier(.22,1,.36,1),transform.6s cubic-bezier(.22,1,.36,1);
}
.sr.on{opacity:1;transform:translateY(0)}
.sr-delay-1{transition-delay:.08s}
.sr-delay-2{transition-delay:.16s}
.sr-delay-3{transition-delay:.24s}
.sr-delay-4{transition-delay:.32s}
.sr-delay-5{transition-delay:.40s}
.sr-delay-6{transition-delay:.48s}

/* ── RESPONSIVE ── */
@media(max-width:900px){
  .grid3,.feat-grid,.plans,.rev-grid{grid-template-columns:1fr 1fr}
  .nav-r a{display:none}
}
@media(max-width:580px){
  .grid3,.feat-grid,.plans,.rev-grid,.grid2{grid-template-columns:1fr}
  .stats{flex-direction:column}
  .s{border-right:none;border-bottom:1px solid var(--border)}
  .s:last-child{border-bottom:none}
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">Web<span>Sale</span></div>
  <div class="nav-r">
    <a href="#catalog">Каталог</a>
    <a href="#pricing">Цены</a>
    <a href="#reviews">Отзывы</a>
    <button class="cta-nav" onclick="openM('Консультация')">Связаться</button>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-blob"></div>
  <div class="hero-blob2"></div>
  <div class="chip"><span class="dot-live"></span>200+ сайтов продано</div>
  <h1>Готовый сайт<br>для бизнеса <span class="hi">за 24 часа</span></h1>
  <p>Покупайте профессиональные сайты без разработки и ожидания. Передача за 48 часов.</p>
  <div class="hero-btns">
    <a href="#catalog" class="btn-main">Смотреть каталог →</a>
    <a href="#pricing" class="btn-sec">Тарифы</a>
  </div>
  <div class="stats sr">
    <div class="s"><strong>200+</strong><span>Продано</span></div>
    <div class="s"><strong>48ч</strong><span>Передача</span></div>
    <div class="s"><strong>4.9★</strong><span>Оценка</span></div>
    <div class="s"><strong>0 ₸</strong><span>Скрытых плат</span></div>
  </div>
</section>

<!-- CATALOG -->
<section class="sec sec-dark" id="catalog">
  <div class="sec-head sr">
    <div class="sec-label">Каталог</div>
    <div class="sec-title">Выберите свой сайт</div>
    <div class="sec-sub">Уникальный дизайн, рабочий функционал, поддержка при передаче.</div>
  </div>
  <div class="grid3">
    <div class="site-card sr sr-delay-1 t-rest" onclick="openM('Ресторан')">
      <div class="card-preview"><div class="card-inner">
        <div class="cb"><span></span><span></span><span></span></div>
        <div class="cl" style="width:55%;height:14px"></div>
        <div class="cl" style="width:90%;height:8px"></div>
        <div class="cl" style="width:70%;height:8px"></div>
        <div class="cl" style="width:38%;height:26px;border-radius:7px;margin-top:8px"></div>
      </div></div>
      <div class="card-info">
        <span class="c-tag">Ресторан</span>
        <div class="c-name">Сайт ресторана</div>
        <div style="font-size:.78rem;color:var(--muted2)">Меню, бронирование, галерея</div>
        <div class="c-bot">
          <div><span class="c-price">900 ₸</span><span class="c-old">1 500 ₸</span></div>
          <button class="c-buy">Купить</button>
        </div>
      </div>
    </div>

    <div class="site-card sr sr-delay-2 t-beauty" onclick="openM('Салон красоты')">
      <div class="card-preview"><div class="card-inner">
        <div class="cb"><span></span><span></span><span></span></div>
        <div class="cl" style="width:48%;height:14px"></div>
        <div class="cl" style="width:85%;height:8px"></div>
        <div class="cl" style="width:65%;height:8px"></div>
        <div class="cl" style="width:36%;height:26px;border-radius:7px;margin-top:8px"></div>
      </div></div>
      <div class="card-info">
        <span class="c-tag">Красота</span>
        <div class="c-name">Салон красоты</div>
        <div style="font-size:.78rem;color:var(--muted2)">Запись, портфолио, прайс</div>
        <div class="c-bot">
          <div><span class="c-price">700 ₸</span><span class="c-old">1 200 ₸</span></div>
          <button class="c-buy">Купить</button>
        </div>
      </div>
    </div>

    <div class="site-card sr sr-delay-3 t-tech" onclick="openM('IT-компания')">
      <div class="card-preview"><div class="card-inner">
        <div class="cb"><span></span><span></span><span></span></div>
        <div class="cl" style="width:62%;height:14px"></div>
        <div class="cl" style="width:100%;height:8px"></div>
        <div class="cl" style="width:78%;height:8px"></div>
        <div class="cl" style="width:42%;height:26px;border-radius:7px;margin-top:8px"></div>
      </div></div>
      <div class="card-info">
        <span class="c-tag">IT</span>
        <div class="c-name">IT-компания</div>
        <div style="font-size:.78rem;color:var(--muted2)">Кейсы, анимации, форма заявки</div>
        <div class="c-bot">
          <div><span class="c-price">1 200 ₸</span><span class="c-old">1 500 ₸</span></div>
          <button class="c-buy">Купить</button>
        </div>
      </div>
    </div>

    <div class="site-card sr sr-delay-4 t-fit" onclick="openM('Фитнес-клуб')">
      <div class="card-preview"><div class="card-inner">
        <div class="cb"><span></span><span></span><span></span></div>
        <div class="cl" style="width:52%;height:14px"></div>
        <div class="cl" style="width:88%;height:8px"></div>
        <div class="cl" style="width:68%;height:8px"></div>
        <div class="cl" style="width:40%;height:26px;border-radius:7px;margin-top:8px"></div>
      </div></div>
      <div class="card-info">
        <span class="c-tag">Спорт</span>
        <div class="c-name">Фитнес-клуб</div>
        <div style="font-size:.78rem;color:var(--muted2)">Расписание, абонементы, тренеры</div>
        <div class="c-bot">
          <div><span class="c-price">800 ₸</span><span class="c-old">1 300 ₸</span></div>
          <button class="c-buy">Купить</button>
        </div>
      </div>
    </div>

    <div class="site-card sr sr-delay-5 t-hotel" onclick="openM('Отель')">
      <div class="card-preview"><div class="card-inner">
        <div class="cb"><span></span><span></span><span></span></div>
        <div class="cl" style="width:58%;height:14px"></div>
        <div class="cl" style="width:92%;height:8px"></div>
        <div class="cl" style="width:74%;height:8px"></div>
        <div class="cl" style="width:44%;height:26px;border-radius:7px;margin-top:8px"></div>
      </div></div>
      <div class="card-info">
        <span class="c-tag">Отель</span>
        <div class="c-name">Бутик-отель</div>
        <div style="font-size:.78rem;color:var(--muted2)">Бронирование, галерея, отзывы</div>
        <div class="c-bot">
          <div><span class="c-price">1 400 ₸</span><span class="c-old">1 500 ₸</span></div>
          <button class="c-buy">Купить</button>
        </div>
      </div>
    </div>

    <div class="site-card sr sr-delay-6 t-med" onclick="openM('Медклиника')">
      <div class="card-preview"><div class="card-inner">
        <div class="cb"><span></span><span></span><span></span></div>
        <div class="cl" style="width:55%;height:14px"></div>
        <div class="cl" style="width:86%;height:8px"></div>
        <div class="cl" style="width:70%;height:8px"></div>
        <div class="cl" style="width:42%;height:26px;border-radius:7px;margin-top:8px"></div>
      </div></div>
      <div class="card-info">
        <span class="c-tag">Медицина</span>
        <div class="c-name">Медклиника</div>
        <div style="font-size:.78rem;color:var(--muted2)">Запись к врачу, услуги, команда</div>
        <div class="c-bot">
          <div><span class="c-price">1 100 ₸</span><span class="c-old">1 500 ₸</span></div>
          <button class="c-buy">Купить</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FEATURES -->
<section class="sec" id="why">
  <div class="sec-head sr">
    <div class="sec-label">Преимущества</div>
    <div class="sec-title">Почему выбирают нас</div>
  </div>
  <div class="feat-grid">
    <div class="feat sr sr-delay-1"><div class="feat-icon">⚡</div><h3>Передача за 48 часов</h3><p>Все файлы, домен и доступы — в течение двух суток после оплаты.</p></div>
    <div class="feat sr sr-delay-2"><div class="feat-icon">🎨</div><h3>Уникальный дизайн</h3><p>Каждый сайт разработан с нуля, без шаблонов.</p></div>
    <div class="feat sr sr-delay-3"><div class="feat-icon">📱</div><h3>Мобильная адаптация</h3><p>Идеально выглядит на любом устройстве.</p></div>
    <div class="feat sr sr-delay-4"><div class="feat-icon">🛡️</div><h3>Поддержка 30 дней</h3><p>Правки, вопросы и консультации — бесплатно после покупки.</p></div>
    <div class="feat sr sr-delay-5"><div class="feat-icon">🔒</div><h3>Чистый код</h3><p>Без вирусов и скрытых скриптов. Код проверен перед продажей.</p></div>
    <div class="feat sr sr-delay-6"><div class="feat-icon">📈</div><h3>SEO с первого дня</h3><p>Оптимизированная структура и мета-теги из коробки.</p></div>
  </div>
</section>

<!-- PRICING -->
<section class="sec sec-dark" id="pricing">
  <div class="sec-head sr">
    <div class="sec-label">Тарифы</div>
    <div class="sec-title">Прозрачные цены</div>
    <div class="sec-sub">Оплата в тенге, без скрытых платежей.</div>
  </div>
  <div class="plans">
    <div class="plan sr sr-delay-1">
      <div class="plan-n">Базовый</div>
      <div class="plan-p">от 500 <small>₸</small></div>
      <div class="plan-per">единоразово</div>
      <hr>
      <ul>
        <li><span class="ck">✓</span>Готовый сайт из каталога</li>
        <li><span class="ck">✓</span>Передача всех файлов</li>
        <li><span class="ck">✓</span>Базовая настройка</li>
        <li><span class="ck">✓</span>Поддержка 14 дней</li>
        <li class="no"><span class="ck">—</span>Правки дизайна</li>
        <li class="no"><span class="ck">—</span>SEO-настройка</li>
      </ul>
      <button class="plan-btn plan-btn-ghost" onclick="openM('Базовый')">Выбрать</button>
    </div>
    <div class="plan pop sr sr-delay-2">
      <div class="plan-badge">Популярный</div>
      <div class="plan-n">Бизнес</div>
      <div class="plan-p">от 900 <small>₸</small></div>
      <div class="plan-per">единоразово</div>
      <hr>
      <ul>
        <li><span class="ck">✓</span>Готовый сайт из каталога</li>
        <li><span class="ck">✓</span>Передача всех файлов</li>
        <li><span class="ck">✓</span>Настройка под ваш бренд</li>
        <li><span class="ck">✓</span>Поддержка 30 дней</li>
        <li><span class="ck">✓</span>До 10 правок дизайна</li>
        <li><span class="ck">✓</span>SEO-настройка</li>
      </ul>
      <button class="plan-btn plan-btn-main" onclick="openM('Бизнес')">Выбрать</button>
    </div>
    <div class="plan sr sr-delay-3">
      <div class="plan-n">Корпоративный</div>
      <div class="plan-p" style="font-size:1.6rem">По запросу</div>
      <div class="plan-per">под ключ</div>
      <hr>
      <ul>
        <li><span class="ck">✓</span>Индивидуальная разработка</li>
        <li><span class="ck">✓</span>Неограниченные правки</li>
        <li><span class="ck">✓</span>CRM / ERP интеграция</li>
        <li><span class="ck">✓</span>Поддержка 90 дней</li>
        <li><span class="ck">✓</span>SEO + аналитика</li>
        <li><span class="ck">✓</span>Личный менеджер</li>
      </ul>
      <button class="plan-btn plan-btn-ghost" onclick="openM('Корпоративный')">Обсудить</button>
    </div>
  </div>
</section>

<!-- REVIEWS -->
<section class="sec" id="reviews">
  <div class="sec-head sr">
    <div class="sec-label">Отзывы</div>
    <div class="sec-title">Что говорят клиенты</div>
  </div>
  <div class="rev-grid">
    <div class="rev sr sr-delay-1">
      <div class="rev-stars">★★★★★</div>
      <div class="rev-text">«Сайт для ресторана запустили за 2 дня. Бронирование заработало сразу — клиенты довольны.»</div>
      <div class="rev-author">
        <div class="rev-av" style="background:linear-gradient(135deg,#FF6B35,#FF9A5C)">А</div>
        <div><div class="rev-name">Асель Нурланова</div><div class="rev-role">Владелец ресторана, Алматы</div></div>
      </div>
    </div>
    <div class="rev sr sr-delay-2">
      <div class="rev-stars">★★★★★</div>
      <div class="rev-text">«Сайт IT-компании выглядит дорого и профессионально. Передали быстро, поддержка на связи.»</div>
      <div class="rev-author">
        <div class="rev-av" style="background:linear-gradient(135deg,#6C63FF,#4ECDC4)">Д</div>
        <div><div class="rev-name">Даурен Сейткали</div><div class="rev-role">CEO, TechStudio KZ</div></div>
      </div>
    </div>
    <div class="rev sr sr-delay-3">
      <div class="rev-stars">★★★★★</div>
      <div class="rev-text">«Онлайн-запись для салона работает идеально. Клиенты записываются даже ночью. Окупился за неделю!»</div>
      <div class="rev-author">
        <div class="rev-av" style="background:linear-gradient(135deg,#C77DFF,#E0AAFF)">М</div>
        <div><div class="rev-name">Мадина Ахметова</div><div class="rev-role">Салон красоты, Астана</div></div>
      </div>
    </div>
  </div>
</section>

<!-- CTA -->
<section class="sec sec-dark">
  <div class="cta-wrap sr">
    <h2>Готовы запустить<br>бизнес онлайн?</h2>
    <p>Оставьте заявку — подберём сайт под ваши задачи бесплатно.</p>
    <button class="btn-main" onclick="openM('Консультация')">Получить консультацию →</button>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="f-logo">Web<span>Sale</span></div>
  <p>© 2026 WebSale. Все права защищены.</p>
  <div class="f-links">
    <a href="#">Политика</a>
    <a href="#">Оферта</a>
    <a href="#">Контакты</a>
  </div>
</footer>

<!-- MODAL -->
<div class="overlay" id="modal" onclick="closeOut(event)">
  <div class="modal">
    <h3>Оставить заявку</h3>
    <p class="sub" id="msub">Свяжемся в течение часа</p>
    <div class="fg"><label>Имя</label><input type="text" placeholder="Алибек Джаксыбеков"></div>
    <div class="fg"><label>Телефон или e-mail</label><input type="text" placeholder="+7 (700) 000-00-00"></div>
    <div class="fg">
      <label>Продукт</label>
      <select id="msel">
        <option>Консультация</option>
        <option>Базовый</option>
        <option>Бизнес</option>
        <option>Корпоративный</option>
        <option>Ресторан</option>
        <option>Салон красоты</option>
        <option>IT-компания</option>
        <option>Фитнес-клуб</option>
        <option>Отель</option>
        <option>Медклиника</option>
      </select>
    </div>
    <div class="m-btns">
      <button class="m-cancel" onclick="closeM()">Отмена</button>
      <button class="m-send" onclick="send()">Отправить</button>
    </div>
  </div>
</div>
<div class="toast" id="toast">✓ Заявка отправлена! Свяжемся в течение часа.</div>

<script>
// Scroll reveal
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('on') });
}, {threshold: 0.08});
document.querySelectorAll('.sr').forEach(el => obs.observe(el));

// Modal
function openM(p) {
  document.getElementById('modal').classList.add('open');
  document.getElementById('msub').textContent = p ? 'Вы выбрали: ' + p : 'Свяжемся в течение часа';
  const s = document.getElementById('msel');
  for(let o of s.options) { if(o.textContent.includes(p)) { s.value = o.value; break; } }
}
function closeM() { document.getElementById('modal').classList.remove('open') }
function closeOut(e) { if(e.target.id === 'modal') closeM() }
async function send() {
  const inputs = document.querySelectorAll('.fg input');
  const name    = inputs[0].value.trim() || 'Не указано';
  const contact = inputs[1].value.trim() || 'Не указано';
  const product = document.getElementById('msel').value;

  const TOKEN = '8676412217:AAFFJ8dM4N6F23cBXmnMA5i3Im-jgtnQJlQ';
  const CHAT  = '5889693603';
  const text  = '📩 Новая заявка!\n\n👤 Имя: ' + name + '\n📞 Контакт: ' + contact + '\n🛒 Продукт: ' + product + '\n🕐 ' + new Date().toLocaleString('ru-RU');

  try {
    await fetch('https://api.telegram.org/bot' + TOKEN + '/sendMessage', {
      method: 'POST',
      headers: {'Content-Type':'application/json'},
      body: JSON.stringify({chat_id: CHAT, text: text})
    });
  } catch(e) { console.error(e); }

  closeM();
  inputs[0].value = '';
  inputs[1].value = '';
  const t = document.getElementById('toast');
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 3500);
}
</script>
</body>
</html>
