[index.html](https://github.com/user-attachments/files/27303390/index.html)
<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>お食事処 サンマール 門川</title>
<style>
:root{
  --bg:#f7f2e8;
  --paper:#fffdf5;
  --ink:#1e1608;
  --sub:#6a5740;
  --accent:#c4411c;
  --gold:#c8922a;
  --green:#2e6b2e;
  --line:rgba(30,22,8,0.15);
}
*{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{
  font-family:"Yu Gothic","Hiragino Kaku Gothic ProN",Meiryo,sans-serif;
  color:var(--ink);background:var(--bg);line-height:1.85;
}
a{color:inherit;text-decoration:none;}
img{display:block;width:100%;object-fit:cover;}

/* ── HEADER ── */
header{
  position:fixed;top:0;left:0;right:0;z-index:100;
  background:rgba(28,18,8,0.88);color:#fff;
  backdrop-filter:blur(12px);
}
.nav{
  max-width:1100px;margin:0 auto;padding:14px 24px;
  display:flex;align-items:center;justify-content:space-between;gap:16px;
}
.logo{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:17px;letter-spacing:.1em;font-weight:700;
}
.logo small{font-size:12px;opacity:.7;margin-left:6px;font-family:"Yu Gothic",sans-serif;}
.nav-links{display:flex;gap:22px;font-size:13px;letter-spacing:.06em;}
.nav-links a{opacity:.85;transition:opacity .2s;}
.nav-links a:hover{opacity:1;}
.nav-cta{
  padding:8px 18px;border:1px solid rgba(255,255,255,.65);
  border-radius:999px;font-size:13px;letter-spacing:.06em;
  transition:background .2s;
}
.nav-cta:hover{background:rgba(255,255,255,.12);}

/* ── HERO ── */
.hero{
  min-height:93vh;display:grid;place-items:center;
  padding:120px 24px 80px;text-align:center;color:#fff;
  background:
    linear-gradient(rgba(22,12,4,.52),rgba(22,12,4,.68)),
    url("images/131204_396.jpg") center/cover;
  position:relative;overflow:hidden;
}
.hero::after{
  content:'';position:absolute;inset:0;
  background:radial-gradient(ellipse at 50% 80%,rgba(196,65,28,.18) 0%,transparent 70%);
}
.hero-inner{max-width:860px;position:relative;z-index:1;}
.eyebrow{
  display:inline-block;margin-bottom:20px;
  padding:6px 18px;border:1px solid rgba(255,255,255,.5);
  border-radius:999px;font-size:13px;letter-spacing:.18em;
  animation:fadein .7s ease both;
}
.hero h1{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:clamp(38px,7vw,78px);line-height:1.18;letter-spacing:.08em;
  text-shadow:0 6px 32px rgba(0,0,0,.4);
  animation:fadein .8s ease both;
}
.hero h1 em{color:#f9d080;font-style:normal;}
.hero p{
  margin:24px auto 0;max-width:680px;
  font-size:clamp(15px,2vw,19px);opacity:.88;
  animation:fadein 1s ease both;
}
.hero-btns{
  margin-top:36px;display:flex;justify-content:center;gap:14px;flex-wrap:wrap;
  animation:fadein 1.1s ease both;
}
.btn{
  display:inline-block;padding:13px 28px;border-radius:999px;
  font-weight:700;font-size:15px;letter-spacing:.06em;transition:.2s;
}
.btn-primary{background:var(--accent);color:#fff;}
.btn-primary:hover{background:#a8351500;background:color-mix(in srgb,var(--accent) 88%,#000);transform:translateY(-2px);}
.btn-secondary{border:1px solid rgba(255,255,255,.7);color:#fff;}
.btn-secondary:hover{background:rgba(255,255,255,.1);transform:translateY(-2px);}

/* ── PROMISE BAR ── */
.promise{
  background:var(--accent);display:flex;justify-content:center;
  flex-wrap:wrap;gap:0;
}
.promise-item{
  color:#fff;font-size:13px;font-weight:700;letter-spacing:.1em;
  padding:10px 28px;border-right:1px solid rgba(255,255,255,.25);
}
.promise-item:last-child{border-right:none;}

/* ── SECTION ── */
section{padding:88px 24px;}
.container{max-width:1100px;margin:0 auto;}
.section-title{text-align:center;margin-bottom:52px;}
.section-title .kicker{
  display:inline-block;color:var(--accent);
  font-weight:700;letter-spacing:.18em;font-size:12px;margin-bottom:10px;
}
.section-title h2{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:clamp(28px,4vw,46px);letter-spacing:.08em;
}
.section-title p{
  margin-top:14px;color:var(--sub);font-size:15px;max-width:560px;
  margin-left:auto;margin-right:auto;
}

/* ── CONCEPT ── */
.concept{background:var(--paper);}
.concept-grid{
  display:grid;grid-template-columns:1fr 1fr;gap:44px;align-items:center;
}
.concept-card{
  background:#fff;border-radius:28px;padding:40px;
  box-shadow:0 20px 48px rgba(60,35,10,.1);
}
.concept-card .kicker{color:var(--accent);font-size:12px;font-weight:700;letter-spacing:.18em;display:block;margin-bottom:10px;}
.concept-card h2{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:clamp(22px,2.8vw,32px);letter-spacing:.06em;
  margin-bottom:20px;line-height:1.4;
}
.concept-card p{color:var(--sub);font-size:15px;margin-bottom:14px;line-height:1.9;}
.concept-card p:last-child{margin-bottom:0;}
.photo-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
.photo-grid .ph{border-radius:20px;overflow:hidden;box-shadow:0 14px 30px rgba(60,35,10,.14);}
.photo-grid .ph img{height:200px;}
.photo-grid .ph:first-child{grid-column:span 2;}
.photo-grid .ph:first-child img{height:260px;}

/* ── MENU ── */
.menu-grid{
  display:grid;grid-template-columns:repeat(3,1fr);gap:24px;margin-bottom:40px;
}
.menu-card{
  background:#fff;border-radius:24px;overflow:hidden;
  box-shadow:0 16px 36px rgba(60,35,10,.1);
  border:1px solid rgba(30,22,8,.05);
  transition:transform .25s,box-shadow .25s;
}
.menu-card:hover{transform:translateY(-6px);box-shadow:0 24px 52px rgba(60,35,10,.18);}
.menu-card .thumb{height:200px;position:relative;background:#f0e4cc;}
.menu-card .thumb img{height:100%;object-fit:cover;}
.menu-tag{
  position:absolute;top:14px;left:14px;
  background:var(--accent);color:#fff;
  font-size:11px;font-weight:700;padding:4px 12px;
  border-radius:999px;letter-spacing:.08em;
}
.menu-tag.gold{background:var(--gold);}
.menu-tag.green{background:var(--green);}
.menu-body{padding:22px 24px 26px;}
.menu-body h3{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:20px;margin-bottom:8px;letter-spacing:.04em;
}
.menu-body p{color:var(--sub);font-size:13px;line-height:1.8;margin-bottom:14px;}
.price{color:var(--accent);font-weight:800;font-size:20px;letter-spacing:.04em;}
.price small{font-size:13px;font-weight:400;color:var(--sub);margin-left:4px;}

/* ── MENU LIST ── */
.menu-list{display:grid;grid-template-columns:1fr 1fr;gap:28px;}
.list-box{
  background:var(--paper);border-radius:24px;padding:30px 32px;
  border:1px solid var(--line);
}
.list-box h3{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:24px;letter-spacing:.06em;margin-bottom:16px;
  padding-bottom:12px;border-bottom:2px solid var(--gold);
  color:var(--ink);
}
.item{
  display:flex;justify-content:space-between;align-items:baseline;
  gap:12px;padding:11px 0;border-bottom:1px dashed var(--line);
  font-size:14px;
}
.item:last-child{border-bottom:none;}
.item span{color:var(--ink);}
.item strong{color:var(--accent);font-weight:800;font-size:15px;white-space:nowrap;}

/* ── TAKEOUT ── */
.takeout{background:var(--paper);}
.takeout-grid{
  display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:20px;
}
.to-card{
  background:#fff;border-radius:20px;padding:26px 22px;text-align:center;
  border:1.5px solid var(--gold);
  box-shadow:0 8px 24px rgba(60,35,10,.07);
  transition:transform .22s,box-shadow .22s;
}
.to-card:hover{transform:translateY(-5px);box-shadow:0 16px 36px rgba(60,35,10,.14);}
.to-icon{font-size:32px;margin-bottom:10px;}
.to-name{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:16px;margin-bottom:8px;
}
.to-price{color:var(--accent);font-weight:800;font-size:20px;}

/* ── MASCOT ── */
.mascot-sec{
  background:
    linear-gradient(rgba(28,14,4,.88),rgba(28,14,4,.92)),
    url("https://images.unsplash.com/photo-1555396273-367ea4eb4db5?auto=format&fit=crop&w=1400&q=80") center/cover;
  color:#fff;text-align:center;padding:80px 24px;
}
.mascot-inner{max-width:700px;margin:0 auto;}
.mascot-img{
  width:150px;margin:0 auto 28px;
  animation:bob 3.5s ease-in-out infinite;
  filter:drop-shadow(0 12px 32px rgba(0,0,0,.5));
}
@keyframes bob{0%,100%{transform:translateY(0)rotate(-3deg);}50%{transform:translateY(-14px)rotate(3deg);}}
.mascot-sec h2{
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;
  font-size:clamp(24px,3.5vw,38px);letter-spacing:.08em;margin-bottom:16px;
}
.mascot-sec h2 em{color:#f9d080;font-style:normal;}
.mascot-sec p{font-size:15px;opacity:.82;line-height:2;max-width:540px;margin:0 auto;}

/* ── INFO ── */
.info{background:var(--paper);}
.info-grid{display:grid;grid-template-columns:0.9fr 1.1fr;gap:36px;}
.info-card{
  background:#fff;border-radius:28px;padding:36px;
  box-shadow:0 20px 48px rgba(60,35,10,.1);
}
.info-row{padding:16px 0;border-bottom:1px solid var(--line);}
.info-row:last-of-type{border-bottom:none;}
.info-row strong{display:block;color:var(--accent);font-size:12px;letter-spacing:.14em;margin-bottom:5px;}
.info-row span{font-size:15px;}
.map-ph{
  min-height:360px;border-radius:28px;
  background:linear-gradient(135deg,#e2d4bd,#f5ead5);
  display:grid;place-items:center;text-align:center;
  border:1px solid var(--line);padding:32px;color:var(--sub);
  font-size:14px;line-height:2;
}
.map-ph strong{font-size:16px;color:var(--ink);display:block;margin-bottom:8px;}

/* ── FOOTER ── */
footer{
  background:#1a0e06;color:rgba(255,255,255,.6);
  text-align:center;padding:34px 20px;font-size:13px;letter-spacing:.06em;
}
footer strong{color:#f9d080;display:block;font-size:15px;margin-bottom:6px;
  font-family:"Yu Mincho","Hiragino Mincho ProN",serif;letter-spacing:.1em;}

/* ── ANIMATIONS ── */
@keyframes fadein{from{opacity:0;transform:translateY(14px);}to{opacity:1;transform:translateY(0);}}
.reveal{opacity:0;transform:translateY(24px);transition:opacity .65s ease,transform .65s ease;}
.reveal.on{opacity:1;transform:translateY(0);}

/* ── RESPONSIVE ── */
@media(max-width:900px){
  .nav-links{display:none;}
  .concept-grid,.info-grid{grid-template-columns:1fr;}
  .menu-grid{grid-template-columns:1fr 1fr;}
}
@media(max-width:640px){
  .nav-cta{display:none;}
  section{padding:60px 16px;}
  .menu-grid,.menu-list{grid-template-columns:1fr;}
  .photo-grid .ph img{height:170px;}
  .photo-grid .ph:first-child img{height:210px;}
  .promise-item{font-size:12px;padding:9px 14px;}
}
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="nav">
    <a href="#top" class="logo">お食事処 サンマール<small>門川</small></a>
    <nav class="nav-links">
      <a href="#concept">こだわり</a>
      <a href="#menu">お料理</a>
      <a href="#takeout">お持ち帰り</a>
      <a href="#access">店舗情報</a>
    </nav>
    <a href="tel:0000-00-0000" class="nav-cta">ご来店はこちら</a>
  </div>
</header>

<!-- HERO -->
<main id="top">
<section class="hero">
  <div class="hero-inner">
    <span class="eyebrow">CHANPON / ANKAKE / CHICKEN NANBAN</span>
    <h1>毎日仕込む、<br><em>本物の美味しさ</em>を。</h1>
    <p>保存料・合成着色料不使用。素材と手間を惜しまない、門川が誇る地元食堂。</p>
    <div class="hero-btns">
      <a href="#menu" class="btn btn-primary">メニューを見る</a>
      <a href="#takeout" class="btn btn-secondary">お持ち帰り</a>
    </div>
  </div>
</section>

<!-- PROMISE -->
<div class="promise">
  <div class="promise-item">✓ 保存料不使用</div>
  <div class="promise-item">✓ 合成着色料不使用</div>
  <div class="promise-item">✓ 毎日手作り</div>
  <div class="promise-item">✓ 地元に愛されて続けて</div>
</div>

<!-- CONCEPT -->
<section id="concept" class="concept">
  <div class="container concept-grid">
    <div class="concept-card reveal">
      <span class="kicker">CONCEPT</span>
      <h2>素材のうまみを、丁寧に。毎日来たくなる一皿へ。</h2>
      <p>サンマール門川は、地元の皆さまに長く愛されてきたお食事処です。毎朝仕込むスープ、厳選した食材、余計なものを使わない誠実な料理づくりが、私たちのこだわりです。</p>
      <p>チャンポン、あんかけ焼きそば、チキン南蛮定食——どれも「また食べたい」と思っていただける、記憶に残る味を目指しています。ぜひ一度、ご来店ください。</p>
    </div>
    <div class="photo-grid reveal">
      <div class="ph">
        <img src="images/131204_396.jpg" alt="チキン南蛮"/>
      </div>
      <div class="ph">
        <img src="images/131204_443.jpg" alt="ちゃんぽん"/>
      </div>
      <div class="ph">
        <img src="images/131204_440.jpg" alt="あんかけ"/>
      </div>
    </div>
  </div>
</section>

<!-- MENU -->
<section id="menu">
  <div class="container">
    <div class="section-title reveal">
      <div class="kicker">FOOD MENU</div>
      <h2>おすすめ料理</h2>
      <p>看板メニューから定食、サイドまで。毎日通えるラインナップ。</p>
    </div>

    <div class="menu-grid">
      <article class="menu-card reveal">
        <div class="thumb">
          <img src="images/131204_443.jpg" alt="チャンポン"/>
          <span class="menu-tag">人気No.1</span>
        </div>
        <div class="menu-body">
          <h3>チャンポン</h3>
          <p>具材たっぷりのボリューム満点スープ。毎日通いたくなる、サンマールの顔。</p>
          <div class="price">¥950<small>（ミドル ¥750）</small></div>
        </div>
      </article>

      <article class="menu-card reveal" style="transition-delay:.1s">
        <div class="thumb">
          <img src="images/131204_440.jpg" alt="あんかけ焼きそば"/>
          <span class="menu-tag gold">名物</span>
        </div>
        <div class="menu-body">
          <h3>あんかけ焼きそば</h3>
          <p>とろとろのあんが香ばしい麺に絡む、門川名物。お持ち帰りでも大人気。</p>
          <div class="price">¥1,000</div>
        </div>
      </article>

      <article class="menu-card reveal" style="transition-delay:.2s">
        <div class="thumb">
          <img src="images/131204_396.jpg" alt="チキン南蛮定食"/>
          <span class="menu-tag green">ボリューム満点</span>
        </div>
        <div class="menu-body">
          <h3>チキン南蛮定食</h3>
          <p>ジューシーなもも肉4貫、自家製タルタル添え。ご飯・みそ汁付き。</p>
          <div class="price">¥1,100</div>
        </div>
      </article>
    </div>

    <div class="menu-list reveal">
      <div class="list-box">
        <h3>一品料理・定食</h3>
        <div class="item"><span>カレーライス</span><strong>780円</strong></div>
        <div class="item"><span>かけうどん・そば</span><strong>600円</strong></div>
        <div class="item"><span>日替り定食</span><strong>780円</strong></div>
        <div class="item"><span>うどん＆南蛮セット</span><strong>1,000円</strong></div>
        <div class="item"><span>アジフライ定食</span><strong>1,300円</strong></div>
        <div class="item"><span>アジフライ＆南蛮定食</span><strong>1,300円</strong></div>
      </div>
      <div class="list-box">
        <h3>サイドメニュー</h3>
        <div class="item"><span>ご飯</span><strong>200円</strong></div>
        <div class="item"><span>ご飯・大盛り</span><strong>+100円</strong></div>
        <div class="item"><span>みそ汁</span><strong>100円</strong></div>
        <div class="item"><span>生卵（1個）</span><strong>50円</strong></div>
        <div class="item"><span>麺・大盛り（チャンポン・焼きそば）</span><strong>+100円</strong></div>
      </div>
    </div>
  </div>
</section>

<!-- TAKEOUT -->
<section id="takeout" class="takeout">
  <div class="container">
    <div class="section-title reveal">
      <div class="kicker">TAKEOUT</div>
      <h2>お持ち帰りメニュー</h2>
      <p>サンマールの味を、ご自宅でも。容器代は別途50円です。</p>
    </div>
    <div class="takeout-grid">
      <div class="to-card reveal"><img src="images/131204_440.jpg" alt="あんかけ焼きそば"><div class="to-name">あんかけ焼きそば</div><div class="to-price">¥1,000</div></div>
      <div class="to-card reveal"><img src="images/131204_396.jpg" alt="チキン南蛮定食"><div class="to-name">チキン南蛮（モモ肉）</div><div class="to-price">¥1,000</div></div>
      <div class="to-card reveal"><img src="images/IMG_4822.jpg" alt="お弁当"><div class="to-name">お弁当</div><div class="to-price">¥1,000</div></div>
      <div class="to-card reveal"><img src="images/IMG_4822.jpg" alt="ごはん"><div class="to-name">ご飯</div><div class="to-price">¥200</div></div>
      <div class="to-card reveal"><img src="images/IMG_4807.jpg" alt="容器"><div class="to-name">お持ち帰り容器代</div><div class="to-price">¥50</div></div>
    </div>
  </div>
</section>

<!-- MASCOT -->
<section class="mascot-sec">
  <div class="mascot-inner">
    <img class="mascot-img" src="/mnt/user-data/uploads/あんかけくん2021.jpg" alt="あんかけくん" onerror="this.style.display='none'">
    <h2>あんかけくんが、<em>お待ちしています！</em></h2>
    <p>サンマール門川は、今日も皆さまのご来店をお待ちしております。<br>一部を除いて保存料・合成着色料は使用しておりません。<br>安心して、心ゆくまでお楽しみください。</p>
  </div>
</section>

<!-- INFO -->
<section id="access" class="info">
  <div class="container">
    <div class="section-title reveal">
      <div class="kicker">SHOP INFO</div>
      <h2>店舗情報</h2>
    </div>
    <div class="info-grid">
      <div class="info-card reveal">
        <div class="info-row"><strong>店名</strong><span>お食事処 サンマール 門川</span></div>
        <div class="info-row"><strong>住所</strong><span>宮崎県東臼杵郡門川町</span></div>
        <div class="info-row"><strong>電話番号</strong><span>お問い合わせください</span></div>
        <div class="info-row"><strong>営業時間</strong><span>お問い合わせください</span></div>
        <div class="info-row"><strong>定休日</strong><span>お問い合わせください</span></div>
        <div class="info-row"><strong>こだわり</strong><span>保存料・合成着色料不使用（一部除く）</span></div>
        <div style="margin-top:28px;">
          <a href="tel:0000-00-0000" class="btn btn-primary">電話でお問い合わせ</a>
        </div>
      </div>
      <div class="map-ph reveal">
        <div>
          <strong>📍 アクセスマップ</strong>
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d886.0487117799597!2d131.64961472182293!3d32.46894174082094!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x354717002f4cf217%3A0xc56b06deb770d6ec!2z44GK6aOf5LqL5YemIOOCteODs-ODnuODvOODq-mWgOW3nQ!5e1!3m2!1sja!2sjp!4v1777615681267!5m2!1sja!2sjp" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>
    </div>
  </div>
</section>
</main>

<footer>
  <strong>お食事処 サンマール 門川</strong>
  © サンマール門川 All Rights Reserved.
</footer>

<script>
const obs=new IntersectionObserver(es=>{
  es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('on');}});
},{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
</script>
</body>
</html>
