[index .html](https://github.com/user-attachments/files/30662738/index.html)
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LAURA BEAUTY — Làn da khỏe đẹp chỉ sau 14 ngày</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,500&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ===================================================
   LAURA BEAUTY — Landing Page Styles
   Palette: Trắng / Hồng pastel / Beige / Gold nhạt
   Type: Cormorant Garamond (display) + Jost (body)
=================================================== */

:root{
  --white:#ffffff;
  --beige:#f6efe4;
  --beige-deep:#efe3d1;
  --pink:#f3dce0;
  --pink-deep:#e7bcc4;
  --gold:#c9a25a;
  --gold-soft:#e4cd9d;
  --ink:#2e2622;
  --ink-soft:#6b5f57;
  --shadow: 0 20px 45px -20px rgba(46,38,34,0.18);
  --radius-lg: 28px;
  --radius-md: 18px;
  --font-display:'Cormorant Garamond', Georgia, 'Times New Roman', serif;
  --font-body:'Jost', Arial, Helvetica, sans-serif;
}

*{ box-sizing:border-box; margin:0; padding:0; }

html{ scroll-behavior:smooth; }

body{
  font-family:var(--font-body);
  color:var(--ink);
  background:var(--white);
  font-weight:300;
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  text-rendering:optimizeLegibility;
}

.container{
  max-width:1160px;
  margin:0 auto;
  padding:0 28px;
}

h1,h2,h3{ font-family:var(--font-display); font-weight:500; color:var(--ink); }

a{ text-decoration:none; color:inherit; }

.eyebrow{
  font-family:var(--font-body);
  letter-spacing:0.22em;
  text-transform:uppercase;
  font-size:12px;
  color:var(--gold);
  font-weight:500;
  margin-bottom:10px;
}
.eyebrow.center{ text-align:center; }

.section-title{ font-size:clamp(28px,4vw,42px); margin-bottom:44px; }
.section-title.center{ text-align:center; }

/* ---------- Reveal on scroll ---------- */
.reveal{
  opacity:0;
  transform:translateY(28px);
  transition:opacity 0.8s ease, transform 0.8s ease;
}
.reveal.is-visible{ opacity:1; transform:translateY(0); }

/* ---------- Buttons ---------- */
.btn{
  -webkit-appearance:none;
  -moz-appearance:none;
  appearance:none;
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:16px 34px;
  border-radius:100px;
  font-family:var(--font-body);
  font-weight:500;
  font-size:15px;
  letter-spacing:0.03em;
  border:none;
  cursor:pointer;
  transition:transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease;
}
.btn-primary{
  background:linear-gradient(135deg, var(--gold), var(--gold-soft));
  color:var(--white);
  box-shadow:0 14px 30px -10px rgba(201,162,90,0.55);
}
.btn-primary:hover{ transform:translateY(-3px); box-shadow:0 20px 36px -10px rgba(201,162,90,0.65); }
.btn-block{ width:100%; }
.btn-header{
  background:var(--ink);
  color:var(--white);
  padding:11px 24px;
  font-size:13px;
}
.btn-header:hover{ background:var(--gold); }

/* ---------- Header ---------- */
.site-header{
  position:fixed; top:0; left:0; right:0; z-index:100;
  background:rgba(255,255,255,0.85);
  -webkit-backdrop-filter:blur(10px);
  backdrop-filter:blur(10px);
  border-bottom:1px solid rgba(201,162,90,0.15);
}
.header-inner{
  display:flex; align-items:center; justify-content:space-between;
  padding:16px 28px;
}
.logo{ font-family:var(--font-display); font-size:22px; letter-spacing:0.04em; font-weight:600; }
.logo span{ color:var(--gold); font-weight:400; }
.nav-links{ display:flex; gap:32px; font-size:14px; }
.nav-links a{ position:relative; padding:4px 0; }
.nav-links a::after{
  content:''; position:absolute; left:0; bottom:0; width:0; height:1px; background:var(--gold);
  transition:width 0.3s ease;
}
.nav-links a:hover::after{ width:100%; }

/* ---------- Hero ---------- */
.hero{
  position:relative;
  padding:170px 0 100px;
  background:linear-gradient(180deg, var(--beige) 0%, var(--white) 100%);
  overflow:hidden;
}
.hero-glow{
  position:absolute; top:-120px; right:-120px; width:480px; height:480px; border-radius:50%;
  background:radial-gradient(circle, var(--pink) 0%, transparent 70%);
  opacity:0.8;
}
.hero-inner{
  display:grid; grid-template-columns:1.1fr 0.9fr; gap:60px; align-items:center; position:relative;
}
.hero-copy h1{ font-size:clamp(36px,5vw,58px); line-height:1.15; margin-bottom:22px; }
.gold-underline{ position:relative; color:var(--gold); font-style:italic; }
.hero-sub{ font-size:17px; color:var(--ink-soft); max-width:480px; margin-bottom:32px; }
.hero-cta-row{ display:flex; align-items:center; gap:24px; margin-bottom:20px; flex-wrap:wrap; }
.hero-price{ display:flex; flex-direction:column; }
.price-old{ text-decoration:line-through; color:var(--ink-soft); font-size:14px; }
.price-new{ font-family:var(--font-display); font-size:26px; color:var(--gold); font-weight:600; }
.hero-note{ font-size:13px; color:var(--ink-soft); }

/* ---------- Hero visual: ritual ring signature element ---------- */
.hero-visual{ display:flex; align-items:center; justify-content:center; }
.ritual-ring{
  position:relative; width:340px; height:340px;
  border:1.5px dashed var(--gold-soft);
  border-radius:50%;
  display:flex; align-items:center; justify-content:center;
  animation:spin 40s linear infinite;
  will-change:transform;
}
.ritual-core{
  width:150px; height:150px; border-radius:50%;
  background:linear-gradient(135deg, var(--pink), var(--beige));
  box-shadow:var(--shadow);
  display:flex; flex-direction:column; align-items:center; justify-content:center;
  animation:counterspin 40s linear infinite;
  will-change:transform;
}
.ritual-day{ font-family:var(--font-display); font-size:44px; color:var(--gold); font-weight:600; line-height:1; }
.ritual-label{ font-size:12px; text-align:center; color:var(--ink-soft); margin-top:4px; }
.ritual-node{
  position:absolute; width:96px; text-align:center;
  background:var(--white); border-radius:14px; padding:10px 8px;
  font-size:12px; box-shadow:var(--shadow);
  animation:counterspin 40s linear infinite;
}
.ritual-node small{ color:var(--ink-soft); font-weight:300; }
.n1{ top:-14px; left:50%; transform:translateX(-50%); }
.n2{ right:-30px; top:50%; transform:translateY(-50%); }
.n3{ bottom:-14px; left:50%; transform:translateX(-50%); }
.n4{ left:-30px; top:50%; transform:translateY(-50%); }

@keyframes spin{ from{ transform:rotate(0deg);} to{ transform:rotate(360deg);} }
@keyframes counterspin{ from{ transform:rotate(0deg);} to{ transform:rotate(-360deg);} }

/* ---------- Problems ---------- */
.problems{ padding:100px 0; background:var(--white); }
.problem-grid{
  display:grid; grid-template-columns:repeat(5,1fr); gap:20px;
}
.problem-card{
  background:var(--beige); border-radius:var(--radius-md);
  padding:28px 20px; text-align:center;
  transition:transform 0.35s ease, box-shadow 0.35s ease;
}
.problem-card:hover{ transform:translateY(-8px); box-shadow:var(--shadow); }
.problem-icon{ font-size:30px; margin-bottom:14px; }
.problem-card h3{ font-size:18px; margin-bottom:8px; }
.problem-card p{ font-size:13.5px; color:var(--ink-soft); }

/* ---------- Products ---------- */
.products{ padding:100px 0; background:var(--pink); }
.product-grid{ display:grid; grid-template-columns:repeat(3,1fr); gap:30px; }
.product-card{
  background:var(--white); border-radius:var(--radius-lg); padding:34px 28px;
  text-align:center; box-shadow:var(--shadow);
  transition:transform 0.35s ease;
}
.product-card:hover{ transform:translateY(-8px); }
.product-img{ display:flex; justify-content:center; margin-bottom:22px; }
.bottle{ width:64px; height:130px; border-radius:32px 32px 10px 10px; position:relative; }
.bottle::before{ content:''; position:absolute; top:-16px; left:50%; transform:translateX(-50%); width:26px; height:20px; background:var(--gold); border-radius:4px; }
.bottle-1{ background:linear-gradient(180deg, var(--beige-deep), var(--beige)); }
.bottle-2{ background:linear-gradient(180deg, var(--pink-deep), var(--pink)); }
.bottle-3{ background:linear-gradient(180deg, var(--gold-soft), #fff6e6); }
.product-card h3{ font-size:20px; margin-bottom:8px; }
.product-desc{ font-size:14px; color:var(--ink-soft); margin-bottom:16px; }
.ingredient-tag{
  display:inline-block; padding:6px 16px; border-radius:100px;
  background:var(--beige); color:var(--gold); font-size:12px; letter-spacing:0.05em;
}
.ceramide-note{ text-align:center; margin-top:44px; color:var(--ink-soft); font-size:15px; }

/* ---------- Benefits ---------- */
.benefits{ padding:100px 0; background:var(--white); }
.benefit-grid{ display:grid; grid-template-columns:repeat(3,1fr); gap:26px; }
.benefit-card{
  padding:30px; border-radius:var(--radius-md); background:var(--beige);
  transition:transform 0.35s ease, background 0.35s ease;
}
.benefit-card:hover{ transform:translateY(-6px); background:var(--pink); }
.benefit-num{ font-family:var(--font-display); font-size:26px; color:var(--gold-soft); font-weight:600; }
.benefit-card h3{ font-size:19px; margin:10px 0 8px; }
.benefit-card p{ font-size:14px; color:var(--ink-soft); }

/* ---------- Feedback / Carousel ---------- */
.feedback{ padding:100px 0; background:var(--beige); }
.carousel{ position:relative; max-width:640px; margin:0 auto; overflow:hidden; }
.carousel-track{ display:flex; transition:transform 0.5s ease; }
.testimonial-card{
  min-width:100%; background:var(--white); border-radius:var(--radius-lg);
  padding:40px; text-align:center; box-shadow:var(--shadow);
}
.stars{ color:var(--gold); letter-spacing:4px; margin-bottom:16px; }
.testimonial-card p{ font-size:17px; font-style:italic; color:var(--ink); margin-bottom:24px; }
.testi-user{ display:flex; align-items:center; justify-content:center; gap:12px; }
.avatar{
  width:40px; height:40px; border-radius:50%; background:var(--pink-deep);
  display:flex; align-items:center; justify-content:center; font-family:var(--font-display); font-weight:600;
}
.testi-user small{ display:block; color:var(--ink-soft); font-size:12px; }
.carousel-dots{ display:flex; justify-content:center; gap:8px; margin-top:24px; }
.dot{ width:8px; height:8px; border-radius:50%; background:var(--pink-deep); cursor:pointer; transition:background 0.3s ease, width 0.3s ease; }
.dot.active{ background:var(--gold); width:22px; border-radius:6px; }

/* ---------- Promo ---------- */
.promo{ padding:90px 0; background:linear-gradient(135deg, var(--ink), #45372f); color:var(--white); }
.promo-inner{ display:grid; grid-template-columns:1.1fr 0.9fr; gap:50px; align-items:center; }
.promo h2{ color:var(--white); font-size:clamp(26px,3.4vw,36px); margin:10px 0 20px; }
.promo .eyebrow{ color:var(--gold-soft); }
.promo-list{ list-style:none; display:flex; flex-direction:column; gap:10px; font-size:15px; color:#e7ded4; }
.promo-timer{ background:rgba(255,255,255,0.06); border:1px solid rgba(255,255,255,0.12); border-radius:var(--radius-lg); padding:30px; text-align:center; }
.timer-label{ font-size:13px; color:#cdbfae; margin-bottom:14px; letter-spacing:0.05em; }
.countdown{ display:flex; justify-content:center; gap:14px; margin-bottom:24px; }
.time-box{
  background:rgba(255,255,255,0.08); border-radius:12px; padding:14px 16px; min-width:64px;
}
.time-box span{ display:block; font-family:var(--font-display); font-size:28px; color:var(--gold-soft); font-weight:600; }
.time-box small{ font-size:11px; color:#cdbfae; }

/* ---------- Order Form ---------- */
.order{ padding:100px 0; background:var(--white); }
.order-inner{ display:grid; grid-template-columns:0.9fr 1.1fr; gap:60px; }
.order-copy h2{ font-size:clamp(28px,3.6vw,38px); margin:8px 0 16px; }
.order-copy p{ color:var(--ink-soft); margin-bottom:26px; }
.order-price-card{
  background:var(--beige); border-radius:var(--radius-md); padding:20px 24px;
  display:flex; align-items:center; justify-content:space-between; font-size:15px;
}
.order-form{
  background:var(--pink); border-radius:var(--radius-lg); padding:36px;
  display:flex; flex-direction:column; gap:16px; box-shadow:var(--shadow);
}
.order-form label{ font-size:13px; color:var(--ink-soft); display:flex; flex-direction:column; gap:6px; }
.order-form input, .order-form textarea{
  -webkit-appearance:none;
  -moz-appearance:none;
  appearance:none;
  font-family:var(--font-body); padding:13px 16px; border-radius:10px; border:1px solid rgba(46,38,34,0.12);
  font-size:14px; background:var(--white); color:var(--ink); outline:none;
  transition:border 0.3s ease, box-shadow 0.3s ease;
}
.order-form input:focus, .order-form textarea:focus{ border-color:var(--gold); box-shadow:0 0 0 3px rgba(201,162,90,0.18); }
.order-form textarea{ min-height:80px; resize:vertical; }
.form-success{
  display:none; text-align:center; font-size:14px; color:#5b7d5b; background:#e7f2e7; padding:12px; border-radius:10px;
}
.form-success.visible{ display:block; }

/* ---------- FAQ ---------- */
.faq{ padding:100px 0; background:var(--beige); }
.faq-list{ max-width:760px; margin:0 auto; display:flex; flex-direction:column; gap:14px; }
.faq-item{ background:var(--white); border-radius:var(--radius-md); overflow:hidden; box-shadow:var(--shadow); }
.faq-question{
  width:100%; background:none; border:none; text-align:left; padding:22px 26px;
  font-family:var(--font-body); font-size:16px; font-weight:500; color:var(--ink);
  display:flex; justify-content:space-between; align-items:center; cursor:pointer;
}
.faq-question span{ color:var(--gold); font-size:20px; transition:transform 0.3s ease; }
.faq-item.active .faq-question span{ transform:rotate(45deg); }
.faq-answer{ max-height:0; overflow:hidden; transition:max-height 0.4s ease, padding 0.4s ease; padding:0 26px; }
.faq-item.active .faq-answer{ max-height:200px; padding:0 26px 22px; }
.faq-answer p{ color:var(--ink-soft); font-size:14.5px; }

/* ---------- Footer ---------- */
.site-footer{ background:var(--ink); color:#dcd2c8; padding:70px 0 26px; }
.footer-inner{ display:grid; grid-template-columns:1.4fr 1fr 1fr 1fr; gap:36px; }
.footer-brand .logo{ color:var(--white); }
.footer-brand .logo span{ color:var(--gold-soft); }
.footer-brand p{ font-size:13.5px; color:#a99d90; margin-top:10px; }
.footer-col h4{ font-family:var(--font-body); font-size:14px; color:var(--white); margin-bottom:14px; letter-spacing:0.04em; }
.footer-col p{ font-size:13.5px; margin-bottom:8px; color:#c2b6a8; }
.footer-col a:hover{ color:var(--gold-soft); }
.footer-copy{ text-align:center; margin-top:50px; font-size:12px; color:#8a7f73; }

/* ===================================================
   RESPONSIVE
=================================================== */
@media (max-width: 900px){
  .nav-links{ display:none; }
  .hero-inner, .promo-inner, .order-inner{ grid-template-columns:1fr; }
  .hero{ padding:140px 0 70px; text-align:center; }
  .hero-cta-row{ justify-content:center; }
  .hero-note{ text-align:center; }
  .hero-visual{ margin-top:40px; }
  .problem-grid{ grid-template-columns:repeat(2,1fr); }
  .product-grid, .benefit-grid{ grid-template-columns:1fr; }
  .footer-inner{ grid-template-columns:repeat(2,1fr); }
}
@media (max-width: 480px){
  .ritual-ring{ width:280px; height:280px; }
  .ritual-node{ width:80px; font-size:11px; }
  .problem-grid{ grid-template-columns:1fr 1fr; }
  .footer-inner{ grid-template-columns:1fr; }
  .countdown{ gap:8px; }
  .time-box{ min-width:52px; padding:10px 8px; }
}

/* Reduced motion */
@media (prefers-reduced-motion: reduce){
  .ritual-ring, .ritual-core, .ritual-node{ animation:none; }
  .reveal{ transition:none; opacity:1; transform:none; }
}

</style>
</head>
<body>

<!-- ============ HEADER ============ -->
<header class="site-header" id="siteHeader">
  <div class="container header-inner">
    <div class="logo">LAURA <span>BEAUTY</span></div>
    <nav class="nav-links">
      <a href="#products">Sản phẩm</a>
      <a href="#benefits">Lợi ích</a>
      <a href="#feedback">Đánh giá</a>
      <a href="#faq">FAQ</a>
    </nav>
    <a href="#order" class="btn btn-header">Đặt hàng ngay</a>
  </div>
</header>

<!-- ============ 1. HERO SECTION ============ -->
<section class="hero">
  <div class="hero-glow"></div>
  <div class="container hero-inner">
    <div class="hero-copy reveal">
      <p class="eyebrow">LAURA BEAUTY · Skincare cao cấp</p>
      <h1>Làn da khỏe đẹp<br>chỉ sau <span class="gold-underline">14 ngày</span> sử dụng.</h1>
      <p class="hero-sub">Bộ 3 sản phẩm dưỡng da chuyên sâu — Niacinamide, Hyaluronic Acid &amp; Vitamin C — được hơn 12.000 cô gái Việt tin dùng mỗi tháng.</p>
      <div class="hero-cta-row">
        <a href="#order" class="btn btn-primary">Đặt hàng ngay</a>
        <div class="hero-price">
          <span class="price-old">899.000đ</span>
          <span class="price-new">599.000đ</span>
        </div>
      </div>
      <p class="hero-note">✓ Giao hàng toàn quốc &nbsp; ✓ Đổi trả trong 7 ngày &nbsp; ✓ Kiểm tra hàng trước khi nhận</p>
    </div>
    <div class="hero-visual reveal">
      <div class="ritual-ring">
        <div class="ritual-core">
          <span class="ritual-day">14</span>
          <span class="ritual-label">ngày<br>thay đổi</span>
        </div>
        <div class="ritual-node n1">Ngày 1<br><small>Cấp ẩm</small></div>
        <div class="ritual-node n2">Ngày 5<br><small>Sáng da</small></div>
        <div class="ritual-node n3">Ngày 10<br><small>Giảm mụn</small></div>
        <div class="ritual-node n4">Ngày 14<br><small>Phục hồi</small></div>
      </div>
    </div>
  </div>
</section>

<!-- ============ 2. VẤN ĐỀ KHÁCH HÀNG ============ -->
<section class="problems">
  <div class="container">
    <p class="eyebrow center">Bạn có đang gặp phải?</p>
    <h2 class="section-title center reveal">Làn da đang "kêu cứu" mỗi ngày</h2>
    <div class="problem-grid">
      <div class="problem-card reveal">
        <div class="problem-icon">💧</div>
        <h3>Da khô, bong tróc</h3>
        <p>Thiếu ẩm sâu khiến da căng rát, dễ lão hóa sớm.</p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-icon">🌫️</div>
        <h3>Da xỉn màu</h3>
        <p>Thiếu sức sống, thiếu tự tin khi không trang điểm.</p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-icon">🔴</div>
        <h3>Mụn ẩn</h3>
        <p>Ẩn dưới da, sần sùi, khó điều trị dứt điểm.</p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-icon">⚪</div>
        <h3>Lỗ chân lông to</h3>
        <p>Da không đều, khó che phủ dù trang điểm kỹ.</p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-icon">❓</div>
        <h3>Không biết chọn gì</h3>
        <p>Quá nhiều sản phẩm trên thị trường, không biết đâu là phù hợp.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ 3. GIỚI THIỆU SẢN PHẨM ============ -->
<section class="products" id="products">
  <div class="container">
    <p class="eyebrow center">Bộ giải pháp 3 bước</p>
    <h2 class="section-title center reveal">Sản phẩm trong combo của bạn</h2>
    <div class="product-grid">
      <div class="product-card reveal">
        <div class="product-img"><div class="bottle bottle-1"></div></div>
        <h3>Serum Niacinamide 10%</h3>
        <p class="product-desc">Làm sáng da, mờ thâm, se khít lỗ chân lông.</p>
        <span class="ingredient-tag">Niacinamide</span>
      </div>
      <div class="product-card reveal">
        <div class="product-img"><div class="bottle bottle-2"></div></div>
        <h3>Serum Hyaluronic Acid</h3>
        <p class="product-desc">Cấp ẩm chuyên sâu, căng mọng suốt 24 giờ.</p>
        <span class="ingredient-tag">Hyaluronic Acid</span>
      </div>
      <div class="product-card reveal">
        <div class="product-img"><div class="bottle bottle-3"></div></div>
        <h3>Serum Vitamin C</h3>
        <p class="product-desc">Chống oxy hóa, đều màu da, ngừa lão hóa.</p>
        <span class="ingredient-tag">Vitamin C</span>
      </div>
    </div>
    <p class="ceramide-note reveal">✦ Toàn bộ công thức đều chứa <strong>Ceramide</strong> giúp phục hồi và bảo vệ hàng rào da tự nhiên.</p>
  </div>
</section>

<!-- ============ 4. LỢI ÍCH KHI SỬ DỤNG ============ -->
<section class="benefits" id="benefits">
  <div class="container">
    <p class="eyebrow center">Vì sao chọn LAURA BEAUTY</p>
    <h2 class="section-title center reveal">6 lợi ích bạn nhận được</h2>
    <div class="benefit-grid">
      <div class="benefit-card reveal"><span class="benefit-num">01</span><h3>Dưỡng ẩm</h3><p>Cấp nước tức thời, duy trì độ ẩm cả ngày.</p></div>
      <div class="benefit-card reveal"><span class="benefit-num">02</span><h3>Làm sáng da</h3><p>Cải thiện sắc tố, đều màu chỉ sau 2 tuần.</p></div>
      <div class="benefit-card reveal"><span class="benefit-num">03</span><h3>Giảm mụn</h3><p>Kháng viêm nhẹ dịu, giảm mụn ẩn hiệu quả.</p></div>
      <div class="benefit-card reveal"><span class="benefit-num">04</span><h3>Phục hồi da</h3><p>Tái tạo hàng rào bảo vệ da tự nhiên.</p></div>
      <div class="benefit-card reveal"><span class="benefit-num">05</span><h3>Không chứa cồn</h3><p>Dịu nhẹ, an toàn cho da nhạy cảm.</p></div>
      <div class="benefit-card reveal"><span class="benefit-num">06</span><h3>Mọi loại da</h3><p>Phù hợp da dầu, da khô và da hỗn hợp.</p></div>
    </div>
  </div>
</section>

<!-- ============ 5. FEEDBACK KHÁCH HÀNG ============ -->
<section class="feedback" id="feedback">
  <div class="container">
    <p class="eyebrow center">Khách hàng nói gì</p>
    <h2 class="section-title center reveal">Hơn 12.000 làn da đã thay đổi</h2>
    <div class="carousel reveal">
      <div class="carousel-track" id="carouselTrack">
        <div class="testimonial-card">
          <div class="stars">★★★★★</div>
          <p>"Da mình đỡ khô hẳn chỉ sau 1 tuần, lên tone rõ rệt. Rất đáng tiền!"</p>
          <div class="testi-user"><div class="avatar">M</div><div><strong>Minh Anh</strong><small>Sinh viên, TP.HCM</small></div></div>
        </div>
        <div class="testimonial-card">
          <div class="stars">★★★★★</div>
          <p>"Mụn ẩn giảm thấy rõ, da mềm mịn hơn nhiều so với trước đây."</p>
          <div class="testi-user"><div class="avatar">T</div><div><strong>Thu Trang</strong><small>Nhân viên văn phòng</small></div></div>
        </div>
        <div class="testimonial-card">
          <div class="stars">★★★★★</div>
          <p>"Kết cấu nhẹ, thấm nhanh, không nhờn rít. Sẽ mua lại lần nữa."</p>
          <div class="testi-user"><div class="avatar">H</div><div><strong>Hồng Nhung</strong><small>Sinh viên, Hà Nội</small></div></div>
        </div>
      </div>
      <div class="carousel-dots" id="carouselDots"></div>
    </div>
  </div>
</section>

<!-- ============ 6. CHƯƠNG TRÌNH KHUYẾN MÃI ============ -->
<section class="promo">
  <div class="container promo-inner reveal">
    <div class="promo-text">
      <p class="eyebrow">Ưu đãi có hạn</p>
      <h2>Giảm ngay 30% + Freeship toàn quốc</h2>
      <ul class="promo-list">
        <li>✓ Giảm 30% cho đơn đặt hôm nay</li>
        <li>✓ Miễn phí vận chuyển toàn quốc</li>
        <li>✓ Tặng kèm mặt nạ dưỡng da</li>
        <li>✓ Chỉ áp dụng trong 24 giờ tới</li>
      </ul>
    </div>
    <div class="promo-timer">
      <p class="timer-label">Ưu đãi kết thúc sau</p>
      <div class="countdown" id="countdown">
        <div class="time-box"><span id="cd-hours">00</span><small>Giờ</small></div>
        <div class="time-box"><span id="cd-minutes">00</span><small>Phút</small></div>
        <div class="time-box"><span id="cd-seconds">00</span><small>Giây</small></div>
      </div>
      <a href="#order" class="btn btn-primary btn-block">Nhận ưu đãi ngay</a>
    </div>
  </div>
</section>

<!-- ============ 7. FORM ĐẶT HÀNG ============ -->
<section class="order" id="order">
  <div class="container order-inner reveal">
    <div class="order-copy">
      <p class="eyebrow">Chỉ còn vài bước</p>
      <h2>Đặt hàng ngay hôm nay</h2>
      <p>Điền thông tin bên dưới — đội ngũ LAURA BEAUTY sẽ liên hệ xác nhận đơn trong vòng 15 phút.</p>
      <div class="order-price-card">
        <span>Combo 3 sản phẩm</span>
        <div><span class="price-old">899.000đ</span> <span class="price-new">599.000đ</span></div>
      </div>
    </div>
    <form class="order-form" id="orderForm">
      <label>Họ và tên
        <input type="text" name="name" placeholder="Nguyễn Thị A" required>
      </label>
      <label>Số điện thoại
        <input type="tel" name="phone" placeholder="09xxxxxxxx" required>
      </label>
      <label>Địa chỉ nhận hàng
        <input type="text" name="address" placeholder="Số nhà, đường, quận/huyện, tỉnh/thành" required>
      </label>
      <label>Ghi chú (không bắt buộc)
        <textarea name="note" placeholder="Giao giờ hành chính, gọi trước khi giao..."></textarea>
      </label>
      <button type="submit" class="btn btn-primary btn-block">ĐẶT HÀNG NGAY — NHẬN ƯU ĐÃI</button>
      <p class="form-success" id="formSuccess">✓ Cảm ơn bạn! Đơn hàng đã được ghi nhận, LAURA BEAUTY sẽ liên hệ sớm nhất.</p>
    </form>
  </div>
</section>

<!-- ============ 8. FAQ ============ -->
<section class="faq" id="faq">
  <div class="container">
    <p class="eyebrow center">Giải đáp thắc mắc</p>
    <h2 class="section-title center reveal">Câu hỏi thường gặp</h2>
    <div class="faq-list reveal">
      <div class="faq-item">
        <button class="faq-question">Có phù hợp da nhạy cảm không? <span>+</span></button>
        <div class="faq-answer"><p>Sản phẩm không chứa cồn, hương liệu nồng, đã kiểm nghiệm da liễu và phù hợp với da nhạy cảm.</p></div>
      </div>
      <div class="faq-item">
        <button class="faq-question">Bao lâu thì thấy hiệu quả? <span>+</span></button>
        <div class="faq-answer"><p>Đa số khách hàng cảm nhận da mềm mịn hơn sau 3-5 ngày, hiệu quả rõ rệt sau 14 ngày sử dụng đều đặn.</p></div>
      </div>
      <div class="faq-item">
        <button class="faq-question">Có được kiểm tra hàng trước khi thanh toán không? <span>+</span></button>
        <div class="faq-answer"><p>Có. LAURA BEAUTY hỗ trợ đồng kiểm — bạn kiểm tra hàng trước khi thanh toán khi nhận (COD).</p></div>
      </div>
      <div class="faq-item">
        <button class="faq-question">Chính sách đổi trả như thế nào? <span>+</span></button>
        <div class="faq-answer"><p>Đổi trả miễn phí trong vòng 7 ngày nếu sản phẩm còn nguyên seal hoặc lỗi từ nhà sản xuất.</p></div>
      </div>
    </div>
  </div>
</section>

<!-- ============ 9. FOOTER ============ -->
<footer class="site-footer">
  <div class="container footer-inner">
    <div class="footer-brand">
      <div class="logo">LAURA <span>BEAUTY</span></div>
      <p>Skincare cao cấp cho làn da khỏe đẹp mỗi ngày.</p>
    </div>
    <div class="footer-col">
      <h4>Liên hệ</h4>
      <p>Hotline: 1900 6868</p>
      <p>Email: hello@laurabeauty.vn</p>
    </div>
    <div class="footer-col">
      <h4>Kết nối</h4>
      <p><a href="#">Facebook</a></p>
      <p><a href="#">TikTok</a></p>
    </div>
    <div class="footer-col">
      <h4>Chính sách</h4>
      <p><a href="#">Chính sách bảo mật</a></p>
      <p><a href="#">Chính sách đổi trả</a></p>
    </div>
  </div>
  <p class="footer-copy">© 2026 LAURA BEAUTY. Landing Page demo — dùng cho bài thuyết trình môn Nhập môn Digital Marketing.</p>
</footer>

<script>
/* ===================================================
   LAURA BEAUTY — script.js
   1. Scroll reveal animation
   2. Countdown timer (24h khuyến mãi)
   3. Testimonial carousel
   4. FAQ accordion
   5. Order form (demo submit)
=================================================== */

document.addEventListener('DOMContentLoaded', function () {

  /* ---------- 1. Scroll reveal ---------- */
  const revealEls = document.querySelectorAll('.reveal');
  const revealObserver = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.add('is-visible');
        revealObserver.unobserve(entry.target);
      }
    });
  }, { threshold: 0.15 });
  revealEls.forEach((el) => revealObserver.observe(el));


  /* ---------- 2. Countdown timer ---------- */
  // Đếm ngược 24 giờ kể từ lúc trang được tải (demo cho khuyến mãi "trong 24h")
  const countdownDuration = 24 * 60 * 60 * 1000; // 24h tính bằng mili-giây
  const countdownEnd = Date.now() + countdownDuration;

  const hoursEl = document.getElementById('cd-hours');
  const minutesEl = document.getElementById('cd-minutes');
  const secondsEl = document.getElementById('cd-seconds');

  function pad(num) {
    return String(num).padStart(2, '0');
  }

  function updateCountdown() {
    const remaining = countdownEnd - Date.now();

    if (remaining <= 0) {
      hoursEl.textContent = '00';
      minutesEl.textContent = '00';
      secondsEl.textContent = '00';
      clearInterval(countdownInterval);
      return;
    }

    const hours = Math.floor(remaining / (1000 * 60 * 60));
    const minutes = Math.floor((remaining % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((remaining % (1000 * 60)) / 1000);

    hoursEl.textContent = pad(hours);
    minutesEl.textContent = pad(minutes);
    secondsEl.textContent = pad(seconds);
  }

  updateCountdown();
  const countdownInterval = setInterval(updateCountdown, 1000);


  /* ---------- 3. Testimonial carousel ---------- */
  const track = document.getElementById('carouselTrack');
  const dotsWrap = document.getElementById('carouselDots');
  const slides = track ? Array.from(track.children) : [];
  let currentSlide = 0;
  let carouselTimer;

  function goToSlide(index) {
    currentSlide = (index + slides.length) % slides.length;
    track.style.transform = `translateX(-${currentSlide * 100}%)`;
    Array.from(dotsWrap.children).forEach((dot, i) => {
      dot.classList.toggle('active', i === currentSlide);
    });
  }

  function startAutoPlay() {
    clearInterval(carouselTimer);
    carouselTimer = setInterval(() => goToSlide(currentSlide + 1), 4500);
  }

  if (track && slides.length) {
    slides.forEach((_, i) => {
      const dot = document.createElement('div');
      dot.className = 'dot' + (i === 0 ? ' active' : '');
      dot.addEventListener('click', () => {
        goToSlide(i);
        startAutoPlay();
      });
      dotsWrap.appendChild(dot);
    });
    startAutoPlay();
  }


  /* ---------- 4. FAQ accordion ---------- */
  const faqItems = document.querySelectorAll('.faq-item');
  faqItems.forEach((item) => {
    const question = item.querySelector('.faq-question');
    question.addEventListener('click', () => {
      const isActive = item.classList.contains('active');
      faqItems.forEach((i) => i.classList.remove('active'));
      if (!isActive) item.classList.add('active');
    });
  });


  /* ---------- 5. Order form (demo — không gửi server thật) ---------- */
  const orderForm = document.getElementById('orderForm');
  const formSuccess = document.getElementById('formSuccess');

  if (orderForm) {
    orderForm.addEventListener('submit', function (e) {
      e.preventDefault();
      // Trong bản demo này, form chỉ hiển thị thông báo thành công.
      // Khi triển khai thật, thay đoạn này bằng lời gọi API/Google Sheet/CRM của bạn.
      formSuccess.classList.add('visible');
      orderForm.reset();
      setTimeout(() => formSuccess.classList.remove('visible'), 5000);
    });
  }

});

</script>
</body>
</html>
