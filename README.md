# houseofkhushibeauty<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!-- EDIT: Brand name (page title + description). The visible brand name is set in the SITE SETTINGS block just below <body>. -->
<title>Khushi Beauty | Makeup Artist &amp; Beauty Services</title>
<meta name="description" content="Bridal, party and everyday beauty services, personalised for you. Book a discovery call with Khushi Beauty.">
<meta name="theme-color" content="#fff5f8">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">

<script>document.documentElement.classList.add('js');</script>

<style>
/* =====================================================================
   1. BASE + DESIGN TOKENS
   ===================================================================== */
:root{
  --white:#ffffff;
  --pink-50:#fff6f9;
  --pink-100:#fdedf2;
  --pink-200:#f9dbe5;
  --pink-300:#f2c3d3;
  --pink-400:#e8a9be;
  --mauve:#94566f;            /* small labels only */
  --accent:#b87a93;           /* italic accent words (large text) */
  --ink:#3a2530;              /* headings + body */
  --ink-soft:#6b5560;         /* secondary text */
  --line:#f3e0e7;
  --radius:24px;
  --shadow:0 18px 40px -22px rgba(190,110,140,.45);
  --shadow-lg:0 30px 60px -30px rgba(190,110,140,.55);
  --serif:'Cormorant Garamond',Georgia,'Times New Roman',serif;
  --sans:'Jost',system-ui,-apple-system,'Segoe UI',Roboto,Arial,sans-serif;
  color-scheme:light;
}
*,*::before,*::after{box-sizing:border-box}
html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
body{
  margin:0;font-family:var(--sans);font-size:1.0625rem;line-height:1.65;
  color:var(--ink);background:var(--white);-webkit-font-smoothing:antialiased;
  -webkit-tap-highlight-color:transparent;
}
img,svg{max-width:100%}
h1,h2,h3{font-family:var(--serif);font-weight:500;line-height:1.12;letter-spacing:-.01em;margin:0}
h1{font-size:clamp(2.6rem,7.2vw,4.5rem)}
h2{font-size:clamp(2.1rem,5vw,3.2rem)}
h3{font-size:1.55rem}
p{margin:0}
ul{margin:0;padding:0;list-style:none}
a{color:inherit;text-decoration:none}
button,input,select,textarea{font:inherit;color:inherit}
em{font-style:italic;color:var(--accent)}
:focus-visible{outline:3px solid #c97a98;outline-offset:3px;border-radius:8px}

.container{width:100%;max-width:1140px;margin-inline:auto;padding-inline:clamp(20px,5vw,40px)}
.section{position:relative;padding-block:clamp(64px,10vw,112px)}
section[id]{scroll-margin-top:76px}
.section-tint{background:linear-gradient(180deg,var(--pink-50),#fff 130%)}
.section-head{text-align:center;max-width:660px;margin:0 auto clamp(36px,6vw,60px)}
.section-head p{color:var(--ink-soft);margin-top:16px}

.eyebrow{
  display:inline-flex;align-items:center;gap:.7rem;margin-bottom:16px;
  font-size:.78rem;letter-spacing:.22em;text-transform:uppercase;font-weight:500;color:var(--mauve);
}
.eyebrow::before{content:"";width:24px;height:1px;background:currentColor;opacity:.55}
.section-head .eyebrow::after{content:"";width:24px;height:1px;background:currentColor;opacity:.55}

.icon{width:1.3em;height:1.3em;flex:none;fill:none;stroke:currentColor;stroke-width:1.6;stroke-linecap:round;stroke-linejoin:round}

.skip-link{position:absolute;left:12px;top:-60px;background:#fff;padding:10px 16px;border-radius:12px;z-index:200;box-shadow:var(--shadow)}
.skip-link:focus{top:12px}

/* =====================================================================
   2. BUTTONS
   ===================================================================== */
.btn{
  display:inline-flex;align-items:center;justify-content:center;gap:.6rem;
  min-height:50px;padding:.85rem 1.75rem;border-radius:999px;border:1px solid transparent;
  font-weight:500;letter-spacing:.02em;line-height:1.2;text-align:center;cursor:pointer;
  transition:transform .3s ease,box-shadow .3s ease,background .3s ease,border-color .3s ease;
}
.btn .icon{width:1.1em;height:1.1em}
.btn:hover{transform:translateY(-2px)}
.btn-primary{background:linear-gradient(135deg,#f9d9e4,#f1b9cc);border-color:#eeb1c5;color:var(--ink);box-shadow:0 12px 26px -14px rgba(214,120,157,.7)}
.btn-primary:hover{box-shadow:0 18px 32px -14px rgba(214,120,157,.8);background:linear-gradient(135deg,#fbe0e9,#f4c1d2)}
.btn-ghost{background:#fff;border-color:var(--pink-300);color:var(--ink)}
.btn-ghost:hover{background:var(--pink-50);border-color:var(--pink-400)}
.btn-sm{min-height:44px;padding:.65rem 1.3rem;font-size:.95rem}
.btn-block{width:100%}

/* =====================================================================
   3. NAVIGATION
   ===================================================================== */
.site-header{
  position:sticky;top:0;z-index:60;background:rgba(255,255,255,.9);
  -webkit-backdrop-filter:blur(14px);backdrop-filter:blur(14px);border-bottom:1px solid var(--line);
}
.nav{display:flex;align-items:center;justify-content:space-between;height:68px}
.brand{display:inline-flex;align-items:center;gap:.6rem;font-family:var(--serif);font-size:1.6rem;font-weight:600;letter-spacing:.01em}
.brand .icon{color:var(--pink-400);width:1.1rem;height:1.1rem}
.nav-toggle{display:inline-grid;place-items:center;width:46px;height:46px;border-radius:50%;border:1px solid var(--line);background:#fff;cursor:pointer}
.nav-toggle .i-close{display:none}
.nav-toggle[aria-expanded="true"] .i-open{display:none}
.nav-toggle[aria-expanded="true"] .i-close{display:block}

.nav-links{
  position:absolute;top:100%;left:0;right:0;background:#fff;border-bottom:1px solid var(--line);
  box-shadow:0 26px 30px -24px rgba(150,80,110,.35);padding:6px clamp(20px,5vw,40px) 22px;
  opacity:0;visibility:hidden;transform:translateY(-8px);transition:opacity .25s ease,transform .25s ease,visibility .25s;
}
.nav-links.open{opacity:1;visibility:visible;transform:none}
.nav-links ul{display:flex;flex-direction:column}
.nav-links a:not(.btn){display:block;padding:15px 4px;border-bottom:1px solid var(--pink-100)}
.nav-links a[aria-current="true"]:not(.btn){color:var(--mauve)}
.nav-cta{margin-top:18px}
.nav-cta .btn{width:100%}

@media (min-width:1040px){
  .nav-toggle{display:none}
  .nav-links{position:static;opacity:1;visibility:visible;transform:none;background:none;border:0;box-shadow:none;padding:0}
  .nav-links ul{flex-direction:row;align-items:center;gap:4px}
  .nav-links a:not(.btn){padding:8px 14px;border:0;border-radius:999px;font-size:.95rem;transition:background .25s}
  .nav-links a:not(.btn):hover,.nav-links a[aria-current="true"]:not(.btn){background:var(--pink-100)}
  .nav-cta{margin:0 0 0 10px}
  .nav-cta .btn{width:auto}
}

/* =====================================================================
   4. PHOTO PLACEHOLDERS (replaced automatically when you add a photo URL)
   ===================================================================== */
.photo{position:relative;overflow:hidden;background:linear-gradient(160deg,#fff2f6,#f8d6e3)}
.photo .ph{
  position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:10px;
  padding:14px;text-align:center;color:#8a5169;font-size:.85rem;letter-spacing:.06em;
}
.photo .ph .icon{width:34px;height:34px;opacity:.75}
.photo img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;opacity:0;transition:opacity .6s ease}
.photo.has-img img{opacity:1}
.photo.has-img .ph{display:none}

/* =====================================================================
   5. HERO
   ===================================================================== */
.hero{
  overflow:hidden;padding-block:clamp(40px,7vw,90px) clamp(64px,9vw,112px);
  background:
    radial-gradient(900px 480px at 90% -10%,var(--pink-100),transparent 62%),
    radial-gradient(700px 420px at -10% 60%,var(--pink-50),transparent 60%),#fff;
}
.hero-grid{display:grid;gap:clamp(40px,6vw,72px);align-items:center}
@media (min-width:900px){.hero-grid{grid-template-columns:1.05fr .95fr}}
.hero .lead{font-size:1.18rem;color:var(--ink-soft);max-width:34rem;margin-top:22px}
.hero-actions{display:flex;flex-wrap:wrap;gap:14px;margin-top:34px}
.hero-actions .btn{flex:0 1 auto}
@media (max-width:480px){.hero-actions .btn{width:100%}}

.hero-visual{position:relative;isolation:isolate;width:100%;max-width:420px;margin-inline:auto}
.hero-visual::before{content:"";position:absolute;inset:-14px;z-index:-1;border:1px solid var(--pink-300);border-radius:999px 999px 40px 40px}
.arch{position:relative;aspect-ratio:4/5;border-radius:999px 999px 28px 28px;box-shadow:var(--shadow-lg)}
.hero-chip{
  position:absolute;left:-10px;bottom:38px;display:flex;align-items:center;gap:10px;background:#fff;
  padding:12px 18px;border-radius:18px;box-shadow:var(--shadow);font-size:.92rem;animation:float 6s ease-in-out infinite;
}
.hero-chip .icon{color:var(--pink-400)}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-8px)}}

/* =====================================================================
   6. ABOUT
   ===================================================================== */
.split{display:grid;gap:clamp(36px,6vw,72px);align-items:center}
@media (min-width:900px){.about-grid{grid-template-columns:.9fr 1.1fr}}
.about-photo-wrap{position:relative;isolation:isolate;max-width:460px;width:100%;margin-inline:auto}
.about-photo-wrap::before{content:"";position:absolute;inset:26px -18px -18px 26px;border-radius:32px;background:var(--pink-100);z-index:-1}
.about-photo{aspect-ratio:4/5;border-radius:28px;box-shadow:var(--shadow-lg)}
.about-copy p{color:var(--ink-soft);margin-top:18px}
.about-copy h2{margin-bottom:6px}
.about-points{display:grid;gap:14px;margin-top:28px}
.about-points li{display:flex;align-items:center;gap:14px}
.about-points .dot{display:grid;place-items:center;width:42px;height:42px;border-radius:50%;background:var(--pink-100);color:var(--mauve);flex:none}

/* =====================================================================
   7. CARDS + SERVICES
   ===================================================================== */
.card{
  background:#fff;border:1px solid var(--line);border-radius:var(--radius);padding:30px 28px;
  box-shadow:0 10px 26px -20px rgba(190,110,140,.5);
}
.card:hover{transform:translateY(-4px);box-shadow:var(--shadow);border-color:var(--pink-300)}
.services-grid{display:grid;gap:22px;grid-template-columns:1fr}
@media (min-width:600px){.services-grid{grid-template-columns:repeat(2,1fr)}}
@media (min-width:960px){.services-grid{grid-template-columns:repeat(3,1fr)}}
.card-icon{display:grid;place-items:center;width:56px;height:56px;border-radius:50%;background:var(--pink-100);color:var(--mauve);margin-bottom:20px}
.card-icon .icon{width:26px;height:26px}
.card h3{margin-bottom:10px}
.card p{color:var(--ink-soft);font-size:1rem}
.card-custom{background:linear-gradient(160deg,var(--pink-50),var(--pink-100));border-style:dashed;border-color:var(--pink-300)}
.card-link{display:inline-flex;align-items:center;gap:.5rem;margin-top:16px;font-weight:500;color:var(--mauve)}
.card-link .icon{width:1.1em;height:1.1em;transition:transform .3s}
.card-link:hover .icon{transform:translateX(4px)}
.cta-strip{text-align:center;margin-top:clamp(40px,6vw,64px)}
.cta-strip h3{font-size:clamp(1.6rem,4vw,2.1rem);margin-bottom:20px}

/* =====================================================================
   8. PORTFOLIO
   ===================================================================== */
.gallery{display:grid;gap:12px;grid-template-columns:repeat(2,1fr)}
.tile{
  position:relative;display:block;width:100%;padding:0;border:0;background:none;cursor:pointer;border-radius:20px;overflow:hidden;
  aspect-ratio:4/5;box-shadow:0 12px 28px -20px rgba(190,110,140,.6);transition:transform .35s ease,box-shadow .35s ease;
}
.tile .photo{position:absolute;inset:0}
.tile .photo img{transition:opacity .6s ease,transform .6s ease}
.tile:hover{transform:translateY(-3px);box-shadow:var(--shadow)}
.tile:hover .photo img{transform:scale(1.04)}
.tile::after{content:"";position:absolute;inset:0;border-radius:inherit;box-shadow:inset 0 0 0 1px rgba(255,255,255,.55);pointer-events:none}
.tile:first-child{grid-column:1/-1;aspect-ratio:1/1}
@media (min-width:700px){
  .gallery{gap:16px}
  .tile:first-child{aspect-ratio:4/5}
}
@media (min-width:900px){
  .gallery{grid-template-columns:repeat(4,1fr);grid-auto-rows:250px;gap:18px}
  .tile{aspect-ratio:auto}
  .tile:first-child{grid-column:1/3;grid-row:1/4;aspect-ratio:auto}
}

/* lightbox */
.lightbox{position:fixed;inset:0;z-index:100;display:flex;align-items:center;justify-content:center;padding:64px 16px;background:rgba(58,37,48,.88);animation:fade .25s ease}
.lightbox[hidden]{display:none}
@keyframes fade{from{opacity:0}to{opacity:1}}
.lb-stage{margin:0;max-width:min(92vw,900px);text-align:center}
.lb-stage img{max-height:76vh;width:auto;margin-inline:auto;border-radius:18px;object-fit:contain;box-shadow:0 30px 60px -20px rgba(0,0,0,.5)}
.lb-ph{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:12px;width:min(80vw,340px);aspect-ratio:4/5;border-radius:18px;background:linear-gradient(160deg,#fff2f6,#f8d6e3);color:#8a5169;padding:20px;font-size:.95rem}
.lb-ph .icon{width:40px;height:40px}
.lb-count{color:#fff;opacity:.85;margin-top:14px;font-size:.9rem;letter-spacing:.1em}
.lb-btn{position:absolute;display:grid;place-items:center;width:46px;height:46px;border-radius:50%;border:0;background:#fff;color:var(--ink);cursor:pointer;box-shadow:var(--shadow);transition:transform .25s}
.lb-btn:hover{transform:scale(1.08)}
.lb-close{top:14px;right:14px}
.lb-prev{left:10px;top:50%;margin-top:-23px}
.lb-next{right:10px;top:50%;margin-top:-23px}
@media (max-width:600px){.lb-prev,.lb-next{top:auto;bottom:14px;margin-top:0}.lb-prev{left:calc(50% - 56px)}.lb-next{right:calc(50% - 56px)}.lightbox{padding:64px 12px 76px}}

/* =====================================================================
   9. TRUST
   ===================================================================== */
.trust{padding-block:clamp(8px,3vw,24px) clamp(56px,8vw,96px)}
.trust-card{
  display:flex;align-items:center;justify-content:center;gap:clamp(14px,3vw,28px);text-align:center;
  max-width:560px;margin-inline:auto;padding:clamp(28px,5vw,44px) 24px;border-radius:999px;
  background:linear-gradient(135deg,var(--pink-50),var(--pink-100));border:1px solid var(--pink-200);
}
.trust-card .icon{color:var(--pink-400);width:1.6rem;height:1.6rem}
.trust-stat{display:flex;align-items:baseline;gap:.6rem;flex-wrap:wrap;justify-content:center}
.trust-stat .num{font-family:var(--serif);font-size:clamp(3rem,9vw,4.4rem);font-weight:500;line-height:1}
.trust-stat .lbl{font-size:.9rem;letter-spacing:.24em;text-transform:uppercase;color:var(--mauve);font-weight:500}
@media (max-width:420px){.trust-card{border-radius:36px}}

/* =====================================================================
   10. BOOKING
   ===================================================================== */
@media (min-width:900px){.book-grid{grid-template-columns:1.05fr .95fr}}
.book-copy p{color:var(--ink-soft);margin-top:18px;max-width:34rem}
.book-copy .btn{margin-top:30px}
.note{display:flex;gap:10px;align-items:flex-start;margin-top:22px;font-size:.95rem;color:var(--ink-soft)}
.note .icon{color:var(--mauve);margin-top:3px}
.checks{display:grid;gap:14px;margin-top:22px}
.checks li{display:flex;gap:14px;align-items:center}
.checks .tick{display:grid;place-items:center;width:30px;height:30px;border-radius:50%;background:var(--pink-100);color:var(--mauve);flex:none}
.checks .icon{width:16px;height:16px;stroke-width:2.2}

/* =====================================================================
   11. PROCESS
   ===================================================================== */
.steps{display:grid;gap:22px;grid-template-columns:1fr}
@media (min-width:640px){.steps{grid-template-columns:repeat(2,1fr)}}
@media (min-width:1000px){.steps{grid-template-columns:repeat(4,1fr)}}
.step{text-align:left}
.step-num{display:grid;place-items:center;width:54px;height:54px;border-radius:50%;margin-bottom:20px;font-family:var(--serif);font-size:1.7rem;font-weight:600;background:linear-gradient(135deg,#fbe3ea,#f3c3d3);color:var(--ink)}
.step h3{font-size:1.4rem}

/* =====================================================================
   12. CUSTOM SERVICE
   ===================================================================== */
.custom-panel{
  position:relative;overflow:hidden;text-align:center;max-width:860px;margin-inline:auto;
  padding:clamp(40px,7vw,72px) clamp(24px,6vw,64px);border-radius:36px;
  background:radial-gradient(500px 240px at 15% 0%,#fff,transparent 70%),linear-gradient(160deg,var(--pink-100),var(--pink-200));
  border:1px solid var(--pink-200);
}
.custom-panel p{max-width:38rem;margin:18px auto 30px;color:var(--ink-soft)}

/* =====================================================================
   13. CONTACT + FORM
   ===================================================================== */
.contact-grid{display:grid;gap:28px}
@media (min-width:960px){.contact-grid{grid-template-columns:.85fr 1.15fr;align-items:start}}
.contact-list{display:grid;gap:14px}
.contact-item{
  display:flex;align-items:center;gap:16px;padding:16px 18px;border-radius:20px;background:#fff;border:1px solid var(--line);
  transition:transform .3s,border-color .3s,box-shadow .3s;min-width:0;
}
.contact-item:hover{transform:translateY(-2px);border-color:var(--pink-300);box-shadow:var(--shadow)}
.ci-icon{display:grid;place-items:center;width:46px;height:46px;border-radius:50%;background:var(--pink-100);color:var(--mauve);flex:none}
.contact-item span:last-child{min-width:0}
.contact-item strong{display:block;font-weight:500;line-height:1.3}
.contact-item small{display:block;color:var(--ink-soft);font-size:.92rem;overflow-wrap:anywhere}
.contact-cta{margin-top:22px}

.form-card{padding:clamp(24px,4vw,40px)}
.form-card:hover{transform:none;box-shadow:0 10px 26px -20px rgba(190,110,140,.5);border-color:var(--line)}
.form-card h3{font-size:1.9rem;margin-bottom:6px}
.form-card .sub{color:var(--ink-soft);font-size:.98rem;margin-bottom:22px}
.form-grid{display:grid;gap:16px}
@media (min-width:560px){.form-grid{grid-template-columns:1fr 1fr}.form-grid .full{grid-column:1/-1}}
.field{display:flex;flex-direction:column;gap:6px;min-width:0}
.field label{font-size:.9rem;font-weight:500}
.field .opt{color:var(--ink-soft);font-weight:400}
.field input,.field select,.field textarea{
  width:100%;min-height:52px;padding:13px 16px;background:#fff;border:1px solid #ecd3dc;border-radius:16px;
  transition:border-color .25s,box-shadow .25s;
}
.field textarea{min-height:130px;resize:vertical}
.field select{
  -webkit-appearance:none;appearance:none;padding-right:44px;
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' fill='none' stroke='%23946073' stroke-width='1.6' stroke-linecap='round'/%3E%3C/svg%3E");
  background-repeat:no-repeat;background-position:right 18px center;
}
.field input:focus,.field select:focus,.field textarea:focus{outline:none;border-color:var(--pink-400);box-shadow:0 0 0 4px rgba(242,195,211,.45)}
.form-actions{margin-top:22px}
.form-hint{margin-top:14px;font-size:.88rem;color:var(--ink-soft);text-align:center}
.form-status{margin-top:14px;padding:0;border-radius:14px;font-size:.95rem;text-align:center}
.form-status:not(:empty){padding:12px 16px;background:var(--pink-50);border:1px solid var(--pink-200)}

/* =====================================================================
   14. SOCIAL + FOOTER
   ===================================================================== */
.social{padding-block:clamp(40px,6vw,64px);background:var(--pink-50);border-top:1px solid var(--line)}
.social-inner{display:flex;flex-direction:column;align-items:center;gap:20px;text-align:center}
.social-title{font-family:var(--serif);font-size:1.8rem}
.social-icons{display:flex;gap:16px}
.social-btn{display:grid;place-items:center;width:56px;height:56px;border-radius:50%;background:#fff;border:1px solid var(--pink-200);color:var(--mauve);transition:transform .3s,background .3s,box-shadow .3s}
.social-btn .icon{width:24px;height:24px}
.social-btn:hover{transform:translateY(-3px);background:var(--pink-100);box-shadow:var(--shadow)}

.site-footer{padding-block:clamp(44px,7vw,72px) 28px;background:#fff;border-top:1px solid var(--line)}
.footer-grid{display:grid;gap:34px}
@media (min-width:760px){.footer-grid{grid-template-columns:1.4fr 1fr 1fr}}
.footer-brand p{color:var(--ink-soft);margin-top:12px;max-width:22rem}
.site-footer h4{font-size:.78rem;letter-spacing:.22em;text-transform:uppercase;color:var(--mauve);margin:0 0 14px;font-weight:500}
.footer-links{display:grid;gap:10px}
.footer-links a{color:var(--ink-soft);transition:color .25s}
.footer-links a:hover{color:var(--ink)}
.copyright{margin-top:40px;padding-top:22px;border-top:1px solid var(--line);font-size:.9rem;color:var(--ink-soft);text-align:center}

/* =====================================================================
   15. REVEAL ANIMATION (only active when JavaScript is available)
   ===================================================================== */
.reveal{--rd:0s}
.card,.reveal{transition:opacity .7s ease var(--rd),translate .7s ease var(--rd),transform .35s ease,box-shadow .35s ease,border-color .35s ease}
.js .reveal{opacity:0;translate:0 22px}
.js .reveal.in{opacity:1;translate:0 0}

@media (prefers-reduced-motion:reduce){
  html{scroll-behavior:auto}
  *,*::before,*::after{animation:none!important;transition-duration:.01ms!important}
  .js .reveal{opacity:1;translate:none}
}
</style>
</head>

<body>

<!-- =====================================================================
     SITE SETTINGS  ←  START HERE. Everything you need to edit is in this block.
     Keep the quotation marks. Only change the text between them.
     ===================================================================== -->
<script id="site-settings">
var SITE = {
  // EDIT: Brand name (shown in the menu and footer)
  brandName: "Khushi Beauty",

  // EDIT: Makeup artist name (shown in the About Me heading)
  artistName: "Khushi",

  // EDIT: Phone number. "phoneText" is what people see, "phoneTel" is what the call button dials.
  phoneText: "+91 00000 00000",
  phoneTel: "+910000000000",

  // EDIT: WhatsApp number with country code, digits only (no + and no spaces). Example: 919876543210
  whatsapp: "910000000000",

  // EDIT: Email address
  email: "hello@example.com",

  // EDIT: Instagram page link
  instagram: "https://www.instagram.com/your_handle",

  // EDIT: Facebook page link
  facebook: "https://www.facebook.com/your_page",

  // EDIT: Discovery call booking link (for example a Calendly / Google Calendar booking page link).
  // Leave it as "" (empty) and every "Book a Discovery Call" button will take people to the contact form instead.
  bookingLink: "",

  // EDIT: Photo links. Leave "" to keep the pink placeholder.
  // Tip: a Google Drive share link works (set the file to "Anyone with the link can view").
  photos: {
    hero:  "",            // main photo at the top of the page
    about: "",            // photo in the About Me section
    gallery: [            // your 7 portfolio photos, in order (first one is shown largest)
      "", "", "", "", "", "", ""
    ]
  }
};
</script>

<!-- Icon library (no editing needed) -->
<svg width="0" height="0" style="position:absolute" aria-hidden="true" focusable="false">
  <defs>
    <symbol id="i-sparkle" viewBox="0 0 24 24"><path d="M12 3l1.9 5.1L19 10l-5.1 1.9L12 17l-1.9-5.1L5 10l5.1-1.9z"/><path d="M19 15l.8 2.2L22 18l-2.2.8L19 21l-.8-2.2L16 18l2.2-.8z"/></symbol>
    <symbol id="i-menu" viewBox="0 0 24 24"><path d="M3 6h18M3 12h18M3 18h18"/></symbol>
    <symbol id="i-close" viewBox="0 0 24 24"><path d="M18 6L6 18M6 6l12 12"/></symbol>
    <symbol id="i-arrow" viewBox="0 0 24 24"><path d="M5 12h14M13 6l6 6-6 6"/></symbol>
    <symbol id="i-left" viewBox="0 0 24 24"><path d="M15 6l-6 6 6 6"/></symbol>
    <symbol id="i-right" viewBox="0 0 24 24"><path d="M9 6l6 6-6 6"/></symbol>
    <symbol id="i-camera" viewBox="0 0 24 24"><path d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2z"/><circle cx="12" cy="13" r="4"/></symbol>
    <symbol id="i-check" viewBox="0 0 24 24"><path d="M20 6L9 17l-5-5"/></symbol>
    <symbol id="i-phone" viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></symbol>
    <symbol id="i-mail" viewBox="0 0 24 24"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><path d="M22 6l-10 7L2 6"/></symbol>
    <symbol id="i-whatsapp" viewBox="0 0 24 24"><path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8z"/></symbol>
    <symbol id="i-instagram" viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><path d="M17.5 6.5h.01"/></symbol>
    <symbol id="i-facebook" viewBox="0 0 24 24"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></symbol>
    <symbol id="i-gem" viewBox="0 0 24 24"><path d="M6 3h12l4 6-10 12L2 9z"/><path d="M2 9h20M9 3l3 6 3-6M12 21L9 9M12 21l3-12"/></symbol>
    <symbol id="i-lipstick" viewBox="0 0 24 24"><rect x="6" y="14" width="12" height="7" rx="1.5"/><path d="M8 14v-3h8v3M9 11V6l4-3 2 2v6"/></symbol>
    <symbol id="i-scissors" viewBox="0 0 24 24"><circle cx="6" cy="6" r="3"/><circle cx="6" cy="18" r="3"/><path d="M20 4L8.12 15.88M14.47 14.48L20 20M8.12 8.12L12 12"/></symbol>
    <symbol id="i-drape" viewBox="0 0 24 24"><path d="M3 7c3-3 6 3 9 0s6 3 9 0M3 13c3-3 6 3 9 0s6 3 9 0M3 19c3-3 6 3 9 0s6 3 9 0"/></symbol>
    <symbol id="i-eye" viewBox="0 0 24 24"><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/></symbol>
    <symbol id="i-drop" viewBox="0 0 24 24"><path d="M12 2.69l5.66 5.66a8 8 0 1 1-11.31 0z"/></symbol>
    <symbol id="i-leaf" viewBox="0 0 24 24"><path d="M5 19c0-8 5-14 15-14 0 10-6 15-14 15"/><path d="M5 19l8-8"/></symbol>
    <symbol id="i-polish" viewBox="0 0 24 24"><rect x="7" y="12" width="10" height="9" rx="2"/><path d="M9.5 12V8h5v4M11 8V3.5h2V8"/></symbol>
    <symbol id="i-lotus" viewBox="0 0 24 24"><path d="M12 20c-4 0-7-3-7-7 3 0 5.5 1.5 7 4 1.5-2.5 4-4 7-4 0 4-3 7-7 7z"/><path d="M12 17c-2-2-2-8 0-12 2 4 2 10 0 12z"/></symbol>
    <symbol id="i-heart" viewBox="0 0 24 24"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></symbol>
    <symbol id="i-plus" viewBox="0 0 24 24"><path d="M12 5v14M5 12h14"/></symbol>
    <symbol id="i-chat" viewBox="0 0 24 24"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></symbol>
  </defs>
</svg>

<a class="skip-link" href="#main">Skip to content</a>

<!-- =====================================================================
     NAVIGATION
     ===================================================================== -->
<header class="site-header">
  <div class="container nav">
    <a class="brand" href="#home" aria-label="Home">
      <svg class="icon"><use href="#i-sparkle"/></svg>
      <!-- Brand name is set in SITE SETTINGS at the top. The text below is only a fallback. -->
      <span data-brand>Khushi Beauty</span>
    </a>

    <button class="nav-toggle" id="navToggle" type="button" aria-expanded="false" aria-controls="primaryNav" aria-label="Open menu">
      <svg class="icon i-open"><use href="#i-menu"/></svg>
      <svg class="icon i-close"><use href="#i-close"/></svg>
    </button>

    <nav id="primaryNav" class="nav-links" aria-label="Main navigation">
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About Me</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#process">Process</a></li>
        <li><a href="#contact">Contact</a></li>
        <li class="nav-cta"><a class="btn btn-primary btn-sm js-book" href="#contact">Book a Discovery Call</a></li>
      </ul>
    </nav>
  </div>
</header>

<main id="main">

<!-- =====================================================================
     1. HERO
     ===================================================================== -->
<section class="hero" id="home" aria-labelledby="hero-title">
  <div class="container hero-grid">
    <div class="hero-copy reveal">
      <span class="eyebrow">Makeup &amp; Beauty Services</span>
      <!-- EDIT: Hero headline -->
      <h1 id="hero-title">Beauty made <em>personal</em>, confidence made yours.</h1>
      <!-- EDIT: Hero description -->
      <p class="lead">Bridal, party and everyday beauty services, thoughtfully tailored to you, your occasion and the way you want to feel.</p>
      <div class="hero-actions">
        <a class="btn btn-primary js-book" href="#contact">Book a Discovery Call</a>
        <a class="btn btn-ghost" href="#services">Explore Services</a>
      </div>
    </div>

    <div class="hero-visual reveal" style="--rd:.15s">
      <!-- EDIT: Hero photo — set the link in SITE SETTINGS → photos → hero -->
      <div class="arch photo" data-photo="hero" data-alt="Portrait of the makeup artist">
        <div class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Your photo here</span></div>
      </div>
      <div class="hero-chip"><svg class="icon"><use href="#i-sparkle"/></svg><span>Personalised for every client</span></div>
    </div>
  </div>
</section>

<!-- =====================================================================
     2. ABOUT ME
     ===================================================================== -->
<section class="section" id="about" aria-labelledby="about-title">
  <div class="container split about-grid">
    <div class="about-photo-wrap reveal">
      <!-- EDIT: About Me photo — set the link in SITE SETTINGS → photos → about -->
      <div class="about-photo photo" data-photo="about" data-alt="The makeup artist at work">
        <div class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Your photo here</span></div>
      </div>
    </div>

    <div class="about-copy reveal" style="--rd:.12s">
      <span class="eyebrow">About Me</span>
      <!-- EDIT: About Me content — rewrite these paragraphs in your own words.
           Ideas to add: your training, how long you've been doing makeup, what you love most about it. -->
      <h2 id="about-title">Hi, I'm <em data-artist>Khushi</em></h2>
      <p>Makeup and beauty are more than a passion for me. They are a way of helping people feel like the most confident version of themselves. I love the moment a client looks in the mirror and simply smiles.</p>
      <p>My approach is personal. Every look begins with a conversation about your occasion, your outfit, your skin and your style, and then I shape the service around you. Nothing is one-size-fits-all.</p>
      <p>I've had the pleasure of working with many clients, each with their own story and their own vision, and I bring the same care and attention to every one of them.</p>

      <ul class="about-points">
        <li><span class="dot"><svg class="icon"><use href="#i-heart"/></svg></span>Looks personalised to you</li>
        <li><span class="dot"><svg class="icon"><use href="#i-chat"/></svg></span>Listening always comes first</li>
        <li><span class="dot"><svg class="icon"><use href="#i-sparkle"/></svg></span>A relaxed, comfortable experience</li>
      </ul>
    </div>
  </div>
</section>

<!-- =====================================================================
     3. SERVICES  (no prices, on purpose)
     ===================================================================== -->
<section class="section section-tint" id="services" aria-labelledby="services-title">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Services</span>
      <h2 id="services-title">Beauty services, made for you</h2>
      <p>From your big day to your everyday, choose what you need and we'll tailor it together.</p>
    </div>

    <ul class="services-grid">
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-gem"/></svg></span>
        <h3>Bridal Makeup</h3>
        <p>A soft, polished bridal look planned around your outfit, your venue and how you want to feel on the day.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-sparkle"/></svg></span>
        <h3>Party Makeup</h3>
        <p>Fresh, glowing looks for parties, functions and celebrations, styled to match your outfit and mood.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-lipstick"/></svg></span>
        <h3>HD Makeup</h3>
        <p>A smooth, camera-ready finish designed to look flawless in person, in photos and on video.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-scissors"/></svg></span>
        <h3>Hair Styling &amp; Hairdo</h3>
        <p>Elegant hairdos and styling, from soft waves to polished updos, to complete your look.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-drape"/></svg></span>
        <h3>Saree Draping</h3>
        <p>Neat, graceful saree draping tailored to your style, your occasion and your comfort.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-eye"/></svg></span>
        <h3>Eyebrow &amp; Threading</h3>
        <p>Clean, well-shaped brows and precise threading for a fresh, defined look.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-drop"/></svg></span>
        <h3>Waxing</h3>
        <p>Smooth, tidy results with a comfortable and considerate approach.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-leaf"/></svg></span>
        <h3>Facial &amp; Cleanup</h3>
        <p>Refreshing facial and cleanup services to help your skin look bright and feel cared for.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-polish"/></svg></span>
        <h3>Manicure</h3>
        <p>Neat, well-groomed hands with careful nail shaping and care.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-lotus"/></svg></span>
        <h3>Pedicure</h3>
        <p>Relaxing foot care and tidy nail finishing for polished, comfortable feet.</p>
      </li>
      <li class="card reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-heart"/></svg></span>
        <h3>Basic Beauty Services</h3>
        <p>Everyday essentials and quick touch-ups for whenever you want to feel put together.</p>
      </li>
      <li class="card card-custom reveal">
        <span class="card-icon"><svg class="icon"><use href="#i-plus"/></svg></span>
        <h3>Custom Beauty Service</h3>
        <p>Looking for something specific? Get in touch and tell us what you need. We can discuss a customized beauty service based on your requirements.</p>
        <a class="card-link js-custom" href="#contact">Get in touch <svg class="icon"><use href="#i-arrow"/></svg></a>
      </li>
    </ul>

    <div class="cta-strip reveal">
      <h3>Have Something Specific in Mind?</h3>
      <a class="btn btn-primary js-book" href="#contact">Book a Discovery Call</a>
    </div>
  </div>
</section>

<!-- =====================================================================
     4. PORTFOLIO
     Add your 7 photos in SITE SETTINGS → photos → gallery.
     ===================================================================== -->
<section class="section" id="portfolio" aria-labelledby="portfolio-title">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Portfolio</span>
      <h2 id="portfolio-title">Real Work. Real Clients. Real Results.</h2>
      <p>A glimpse of the looks created for my clients. Tap any photo to view it larger.</p>
    </div>

    <div class="gallery reveal" role="list">
      <button class="tile" type="button" role="listitem" aria-label="View photo 1"><span class="photo" data-gallery="0"><span class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Client photo 1</span></span></span></button>
      <button class="tile" type="button" role="listitem" aria-label="View photo 2"><span class="photo" data-gallery="1"><span class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Client photo 2</span></span></span></button>
      <button class="tile" type="button" role="listitem" aria-label="View photo 3"><span class="photo" data-gallery="2"><span class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Client photo 3</span></span></span></button>
      <button class="tile" type="button" role="listitem" aria-label="View photo 4"><span class="photo" data-gallery="3"><span class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Client photo 4</span></span></span></button>
      <button class="tile" type="button" role="listitem" aria-label="View photo 5"><span class="photo" data-gallery="4"><span class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Client photo 5</span></span></span></button>
      <button class="tile" type="button" role="listitem" aria-label="View photo 6"><span class="photo" data-gallery="5"><span class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Client photo 6</span></span></span></button>
      <button class="tile" type="button" role="listitem" aria-label="View photo 7"><span class="photo" data-gallery="6"><span class="ph"><svg class="icon"><use href="#i-camera"/></svg><span>Client photo 7</span></span></span></button>
    </div>
  </div>
</section>

<!-- =====================================================================
     5. TRUST
     ===================================================================== -->
<section class="trust" aria-label="Experience">
  <div class="container">
    <div class="trust-card reveal">
      <svg class="icon"><use href="#i-sparkle"/></svg>
      <p class="trust-stat"><span class="num">20+</span> <span class="lbl">Clients</span></p>
      <svg class="icon"><use href="#i-sparkle"/></svg>
    </div>
  </div>
</section>

<!-- =====================================================================
     6. BOOKING / DISCOVERY CALL
     ===================================================================== -->
<section class="section section-tint" id="book" aria-labelledby="book-title">
  <div class="container split book-grid">
    <div class="book-copy reveal">
      <span class="eyebrow">Discovery Call</span>
      <h2 id="book-title">Let's Talk About Your Beauty Goals</h2>
      <p>Book a short, friendly discovery call and tell me what you have in mind. There's no pressure. It's simply a chance to talk things through and make sure the service is right for you.</p>
      <a class="btn btn-primary js-book" href="#contact">Book a Discovery Call</a>
      <p class="note"><svg class="icon"><use href="#i-heart"/></svg><span>No payment is taken on this website. Payment is discussed with you during the call.</span></p>
    </div>

    <div class="card reveal" style="--rd:.12s">
      <h3>On the call, we can talk about</h3>
      <ul class="checks">
        <li><span class="tick"><svg class="icon"><use href="#i-check"/></svg></span>Your requirements</li>
        <li><span class="tick"><svg class="icon"><use href="#i-check"/></svg></span>The service you'd like</li>
        <li><span class="tick"><svg class="icon"><use href="#i-check"/></svg></span>Your event or occasion</li>
        <li><span class="tick"><svg class="icon"><use href="#i-check"/></svg></span>Custom requests</li>
        <li><span class="tick"><svg class="icon"><use href="#i-check"/></svg></span>Availability</li>
        <li><span class="tick"><svg class="icon"><use href="#i-check"/></svg></span>Service details</li>
        <li><span class="tick"><svg class="icon"><use href="#i-check"/></svg></span>Payment discussion</li>
      </ul>
    </div>
  </div>
</section>

<!-- =====================================================================
     7. PROCESS
     ===================================================================== -->
<section class="section" id="process" aria-labelledby="process-title">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Process</span>
      <h2 id="process-title">How it works</h2>
      <p>Four simple steps, from your first hello to a confirmed appointment.</p>
    </div>

    <ol class="steps" style="list-style:none;margin:0;padding:0">
      <li class="card step reveal">
        <span class="step-num" aria-hidden="true">1</span>
        <h3>Book a Discovery Call</h3>
        <p>Tap any Book a Discovery Call button or send a message to get started.</p>
      </li>
      <li class="card step reveal" style="--rd:.08s">
        <span class="step-num" aria-hidden="true">2</span>
        <h3>Short Consultation Call</h3>
        <p>Discuss your requirements, desired service, occasion, and any custom requests.</p>
      </li>
      <li class="card step reveal" style="--rd:.16s">
        <span class="step-num" aria-hidden="true">3</span>
        <h3>Service Discussion</h3>
        <p>Discuss the suitable service, availability, and other relevant details, including payment.</p>
      </li>
      <li class="card step reveal" style="--rd:.24s">
        <span class="step-num" aria-hidden="true">4</span>
        <h3>Appointment Confirmation</h3>
        <p>Once everything is agreed upon, your appointment is confirmed.</p>
      </li>
    </ol>
  </div>
</section>

<!-- =====================================================================
     8. CUSTOM SERVICE
     ===================================================================== -->
<section class="section" id="custom" style="padding-top:0" aria-labelledby="custom-title">
  <div class="container">
    <div class="custom-panel reveal">
      <span class="eyebrow">Custom</span>
      <h2 id="custom-title">Need Something Custom?</h2>
      <p>Every client is different. If you have a specific beauty requirement that isn't listed above, get in touch with us. We'll discuss your requirements and see how we can customize the service for you.</p>
      <a class="btn btn-primary js-custom" href="#contact">Discuss Your Requirement</a>
    </div>
  </div>
</section>

<!-- =====================================================================
     9. CONTACT + BOOKING FORM
     ===================================================================== -->
<section class="section section-tint" id="contact" aria-labelledby="contact-title">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Contact</span>
      <h2 id="contact-title">Get in touch</h2>
      <p>Reach out in whichever way is easiest for you, or send a request using the form.</p>
    </div>

    <div class="contact-grid">
      <div class="reveal">
        <div class="contact-list">
          <!-- Phone, WhatsApp, Email, Instagram and Facebook are set in SITE SETTINGS at the top. -->
          <a class="contact-item" data-link="phone"><span class="ci-icon"><svg class="icon"><use href="#i-phone"/></svg></span><span><strong>Phone</strong><small data-text="phone">+91 00000 00000</small></span></a>
          <a class="contact-item" data-link="whatsapp"><span class="ci-icon"><svg class="icon"><use href="#i-whatsapp"/></svg></span><span><strong>WhatsApp</strong><small>Send a message</small></span></a>
          <a class="contact-item" data-link="email"><span class="ci-icon"><svg class="icon"><use href="#i-mail"/></svg></span><span><strong>Email</strong><small data-text="email">hello@example.com</small></span></a>
          <a class="contact-item" data-link="instagram"><span class="ci-icon"><svg class="icon"><use href="#i-instagram"/></svg></span><span><strong>Instagram</strong><small data-text="instagram">@your_handle</small></span></a>
          <a class="contact-item" data-link="facebook"><span class="ci-icon"><svg class="icon"><use href="#i-facebook"/></svg></span><span><strong>Facebook</strong><small>Visit our page</small></span></a>
        </div>
        <div class="contact-cta">
          <a class="btn btn-primary btn-block js-book" href="#contact">Book a Discovery Call</a>
        </div>
      </div>

      <div class="card form-card reveal" style="--rd:.12s">
        <h3>Book a Discovery Call</h3>
        <p class="sub">Share a few details and I'll get back to you to arrange a time to talk.</p>

        <form id="bookingForm" novalidate>
          <div class="form-grid">
            <div class="field">
              <label for="f-name">Name</label>
              <input id="f-name" name="name" type="text" autocomplete="name" required>
            </div>
            <div class="field">
              <label for="f-phone">Phone Number</label>
              <input id="f-phone" name="phone" type="tel" inputmode="tel" autocomplete="tel" required>
            </div>
            <div class="field">
              <label for="f-email">Email <span class="opt">(optional)</span></label>
              <input id="f-email" name="email" type="email" autocomplete="email">
            </div>
            <div class="field">
              <label for="f-service">Service Interested In</label>
              <select id="f-service" name="service">
                <option value="">Select a service</option>
                <option>Bridal Makeup</option>
                <option>Party Makeup</option>
                <option>HD Makeup</option>
                <option>Hair Styling &amp; Hairdo</option>
                <option>Saree Draping</option>
                <option>Eyebrow &amp; Threading</option>
                <option>Waxing</option>
                <option>Facial &amp; Cleanup</option>
                <option>Manicure</option>
                <option>Pedicure</option>
                <option>Basic Beauty Services</option>
                <option>Custom Beauty Service</option>
                <option>Not sure yet</option>
              </select>
            </div>
            <div class="field full">
              <label for="f-date">Preferred Date <span class="opt">(optional)</span></label>
              <input id="f-date" name="date" type="date">
            </div>
            <div class="field full">
              <label for="f-message">Message / Custom Requirement <span class="opt">(optional)</span></label>
              <textarea id="f-message" name="message" placeholder="Tell me about your occasion or what you have in mind"></textarea>
            </div>
          </div>

          <div class="form-actions">
            <button class="btn btn-primary btn-block" type="submit">Send My Request</button>
          </div>
          <p class="form-hint">Sending opens WhatsApp (or your email app) with your details filled in. Nothing is charged here.</p>
          <div class="form-status" id="formStatus" role="status" aria-live="polite"></div>
        </form>
      </div>
    </div>
  </div>
</section>

<!-- =====================================================================
     10. SOCIAL MEDIA
     ===================================================================== -->
<section class="social" id="social" aria-label="Social media">
  <div class="container social-inner">
    <p class="social-title">Follow along</p>
    <div class="social-icons">
      <a class="social-btn" data-link="instagram" aria-label="Instagram"><svg class="icon"><use href="#i-instagram"/></svg></a>
      <a class="social-btn" data-link="facebook" aria-label="Facebook"><svg class="icon"><use href="#i-facebook"/></svg></a>
    </div>
  </div>
</section>

</main>

<!-- =====================================================================
     11. FOOTER
     ===================================================================== -->
<footer class="site-footer">
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <a class="brand" href="#home"><svg class="icon"><use href="#i-sparkle"/></svg><span data-brand>Khushi Beauty</span></a>
        <!-- EDIT: Tagline -->
        <p>Beauty that feels like you.</p>
      </div>
      <div>
        <h4>Quick Links</h4>
        <ul class="footer-links">
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About Me</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#process">Process</a></li>
        </ul>
      </div>
      <div>
        <h4>Connect</h4>
        <ul class="footer-links">
          <li><a data-link="instagram">Instagram</a></li>
          <li><a data-link="facebook">Facebook</a></li>
          <li><a data-link="whatsapp">WhatsApp</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
    </div>
    <p class="copyright">&copy; <span id="year">2026</span> <span data-brand>Khushi Beauty</span>. All rights reserved.</p>
  </div>
</footer>

<!-- Photo preview (lightbox) -->
<div class="lightbox" id="lightbox" role="dialog" aria-modal="true" aria-label="Photo preview" hidden>
  <button class="lb-btn lb-close" id="lbClose" type="button" aria-label="Close preview"><svg class="icon"><use href="#i-close"/></svg></button>
  <button class="lb-btn lb-prev" id="lbPrev" type="button" aria-label="Previous photo"><svg class="icon"><use href="#i-left"/></svg></button>
  <figure class="lb-stage">
    <div id="lbContent"></div>
    <figcaption class="lb-count" id="lbCount"></figcaption>
  </figure>
  <button class="lb-btn lb-next" id="lbNext" type="button" aria-label="Next photo"><svg class="icon"><use href="#i-right"/></svg></button>
</div>

<!-- =====================================================================
     SCRIPT (no editing needed below this line)
     ===================================================================== -->
<script>
(function () {
  'use strict';

  var $  = function (s, c) { return (c || document).querySelector(s); };
  var $$ = function (s, c) { return Array.prototype.slice.call((c || document).querySelectorAll(s)); };

  // Treat empty values and the sample placeholders as "not set yet"
  function isPlaceholder(v) {
    return !v || /0{5,}|example\.com|your_handle|your_page/i.test(v);
  }

  /* ---------- Icons are decorative ---------- */
  $$('svg.icon').forEach(function (s) {
    s.setAttribute('aria-hidden', 'true');
    s.setAttribute('focusable', 'false');
  });

  /* ---------- Fill in brand, name and contact details ---------- */
  $$('[data-brand]').forEach(function (el) { el.textContent = SITE.brandName; });
  $$('[data-artist]').forEach(function (el) { el.textContent = SITE.artistName; });
  document.title = SITE.brandName + ' | Makeup Artist & Beauty Services';

  function handleFrom(url) {
    var parts = String(url || '').replace(/[?#].*$/, '').replace(/\/+$/, '').split('/');
    return '@' + (parts[parts.length - 1] || '');
  }
  function waLink(text) {
    var num = String(SITE.whatsapp || '').replace(/\D/g, '');
    return 'https://wa.me/' + num + (text ? '?text=' + encodeURIComponent(text) : '');
  }

  var LINKS = {
    phone:     'tel:' + String(SITE.phoneTel || '').replace(/\s/g, ''),
    whatsapp:  waLink('Hi! I would like to book a discovery call.'),
    email:     'mailto:' + SITE.email,
    instagram: SITE.instagram,
    facebook:  SITE.facebook
  };
  $$('[data-link]').forEach(function (a) {
    a.href = LINKS[a.getAttribute('data-link')] || '#contact';
    a.target = '_blank';
    a.rel = 'noopener noreferrer';
  });
  $$('[data-text="phone"]').forEach(function (el) { el.textContent = SITE.phoneText; });
  $$('[data-text="email"]').forEach(function (el) { el.textContent = SITE.email; });
  $$('[data-text="instagram"]').forEach(function (el) { el.textContent = handleFrom(SITE.instagram); });

  /* ---------- "Book a Discovery Call" buttons ---------- */
  var bookingLink = String(SITE.bookingLink || '').trim();
  if (bookingLink) {
    $$('.js-book').forEach(function (a) {
      a.href = bookingLink;
      a.target = '_blank';
      a.rel = 'noopener noreferrer';
    });
  }

  /* ---------- "Custom" buttons pre-select the custom service in the form ---------- */
  $$('.js-custom').forEach(function (a) {
    a.addEventListener('click', function () {
      var sel = $('#f-service');
      if (sel) { sel.value = 'Custom Beauty Service'; }
    });
  });

  /* ---------- Photos (with Google Drive link support) ---------- */
  function normalizeUrl(url) {
    url = String(url || '').trim();
    var m = url.match(/drive\.google\.com\/file\/d\/([^\/?#]+)/) ||
            url.match(/drive\.google\.com\/(?:open|uc)\?[^#]*id=([^&#]+)/);
    return m ? 'https://drive.google.com/thumbnail?id=' + m[1] + '&sz=w1600' : url;
  }
  function setPhoto(box, url, alt) {
    if (!box || !url) { return; }
    var img = new Image();
    img.alt = alt || '';
    img.decoding = 'async';
    img.onload = function () { box.classList.add('has-img'); };
    img.onerror = function () { if (img.parentNode) { img.parentNode.removeChild(img); } };
    img.src = normalizeUrl(url);
    box.appendChild(img);
  }
  var photos = SITE.photos || {};
  $$('[data-photo]').forEach(function (box) {
    setPhoto(box, photos[box.getAttribute('data-photo')], box.getAttribute('data-alt'));
  });
  var gallery = photos.gallery || [];
  $$('[data-gallery]').forEach(function (box) {
    var i = parseInt(box.getAttribute('data-gallery'), 10);
    setPhoto(box, gallery[i], 'Client work photo ' + (i + 1));
  });

  /* ---------- Mobile menu ---------- */
  var toggle = $('#navToggle');
  var nav = $('#primaryNav');
  function setMenu(open) {
    nav.classList.toggle('open', open);
    toggle.setAttribute('aria-expanded', String(open));
    toggle.setAttribute('aria-label', open ? 'Close menu' : 'Open menu');
  }
  toggle.addEventListener('click', function () { setMenu(!nav.classList.contains('open')); });
  $$('a', nav).forEach(function (a) { a.addEventListener('click', function () { setMenu(false); }); });
  document.addEventListener('click', function (e) {
    if (nav.classList.contains('open') && !nav.contains(e.target) && !toggle.contains(e.target)) { setMenu(false); }
  });
  window.addEventListener('resize', function () { if (window.innerWidth >= 1040) { setMenu(false); } });

  /* ---------- Highlight the current section in the menu ---------- */
  if ('IntersectionObserver' in window) {
    var navLinks = $$('a[href^="#"]', nav).filter(function (a) { return !a.classList.contains('btn'); });
    var spy = new IntersectionObserver(function (entries) {
      entries.forEach(function (en) {
        if (!en.isIntersecting) { return; }
        navLinks.forEach(function (a) {
          if (a.getAttribute('href') === '#' + en.target.id) { a.setAttribute('aria-current', 'true'); }
          else { a.removeAttribute('aria-current'); }
        });
      });
    }, { rootMargin: '-45% 0px -50% 0px' });
    navLinks.forEach(function (a) {
      var t = $(a.getAttribute('href'));
      if (t) { spy.observe(t); }
    });
  }

  /* ---------- Scroll reveal ---------- */
  var reveals = $$('.reveal');
  if ('IntersectionObserver' in window) {
    var io = new IntersectionObserver(function (entries) {
      entries.forEach(function (en) {
        if (en.isIntersecting) { en.target.classList.add('in'); io.unobserve(en.target); }
      });
    }, { threshold: 0.12 });
    reveals.forEach(function (el) { io.observe(el); });
  } else {
    reveals.forEach(function (el) { el.classList.add('in'); });
  }

  /* ---------- Lightbox ---------- */
  var lb = $('#lightbox'), lbContent = $('#lbContent'), lbCount = $('#lbCount');
  var lbClose = $('#lbClose'), lbPrev = $('#lbPrev'), lbNext = $('#lbNext');
  var tiles = $$('.tile');
  var current = 0, opener = null, startX = null;

  function renderLightbox() {
    var box = $('.photo', tiles[current]);
    var img = $('img', box);
    lbContent.innerHTML = '';
    if (img && box.classList.contains('has-img')) {
      var big = new Image();
      big.src = img.currentSrc || img.src;
      big.alt = img.alt;
      lbContent.appendChild(big);
    } else {
      var ph = document.createElement('div');
      ph.className = 'lb-ph';
      ph.innerHTML = '<svg class="icon" aria-hidden="true" focusable="false"><use href="#i-camera"/></svg><span>Client photo ' + (current + 1) + ' will appear here</span>';
      lbContent.appendChild(ph);
    }
    lbCount.textContent = (current + 1) + ' / ' + tiles.length;
  }
  function openLightbox(i, from) {
    current = i; opener = from;
    renderLightbox();
    lb.hidden = false;
    document.body.style.overflow = 'hidden';
    lbClose.focus();
  }
  function closeLightbox() {
    lb.hidden = true;
    document.body.style.overflow = '';
    if (opener) { opener.focus(); }
  }
  function step(d) {
    current = (current + d + tiles.length) % tiles.length;
    renderLightbox();
  }
  tiles.forEach(function (t, i) { t.addEventListener('click', function () { openLightbox(i, t); }); });
  lbClose.addEventListener('click', closeLightbox);
  lbPrev.addEventListener('click', function () { step(-1); });
  lbNext.addEventListener('click', function () { step(1); });
  lb.addEventListener('click', function (e) { if (e.target === lb) { closeLightbox(); } });
  document.addEventListener('keydown', function (e) {
    if (lb.hidden) { if (e.key === 'Escape') { setMenu(false); } return; }
    if (e.key === 'Escape') { closeLightbox(); }
    else if (e.key === 'ArrowLeft') { step(-1); }
    else if (e.key === 'ArrowRight') { step(1); }
    else if (e.key === 'Tab') {
      var f = [lbClose, lbPrev, lbNext];
      var idx = f.indexOf(document.activeElement);
      e.preventDefault();
      f[(idx + (e.shiftKey ? -1 : 1) + f.length) % f.length].focus();
    }
  });
  lb.addEventListener('touchstart', function (e) { startX = e.changedTouches[0].clientX; }, { passive: true });
  lb.addEventListener('touchend', function (e) {
    if (startX === null) { return; }
    var dx = e.changedTouches[0].clientX - startX;
    startX = null;
    if (Math.abs(dx) > 50) { step(dx < 0 ? 1 : -1); }
  }, { passive: true });

  /* ---------- Booking form ---------- */
  var form = $('#bookingForm');
  var statusBox = $('#formStatus');
  var dateInput = $('#f-date');
  if (dateInput) {
    var t = new Date();
    dateInput.min = t.getFullYear() + '-' + ('0' + (t.getMonth() + 1)).slice(-2) + '-' + ('0' + t.getDate()).slice(-2);
  }
  function openExternal(url) {
    var a = document.createElement('a');
    a.href = url; a.target = '_blank'; a.rel = 'noopener noreferrer';
    document.body.appendChild(a); a.click(); document.body.removeChild(a);
  }
  function prettyDate(v) {
    var p = v.split('-');
    if (p.length !== 3) { return v; }
    return new Date(+p[0], +p[1] - 1, +p[2]).toLocaleDateString('en-IN', { day: 'numeric', month: 'long', year: 'numeric' });
  }
  form.addEventListener('submit', function (e) {
    e.preventDefault();
    statusBox.textContent = '';
    var els = form.elements;
    var fName = els.namedItem('name'), fPhone = els.namedItem('phone'), fEmail = els.namedItem('email');
    var fService = els.namedItem('service'), fDate = els.namedItem('date'), fMessage = els.namedItem('message');
    var name = fName.value.trim();
    var phone = fPhone.value.trim();
    if (!name) { statusBox.textContent = 'Please enter your name.'; fName.focus(); return; }
    if (phone.replace(/\D/g, '').length < 7) { statusBox.textContent = 'Please enter a valid phone number.'; fPhone.focus(); return; }
    if (fEmail.value && !fEmail.checkValidity()) { statusBox.textContent = 'Please check your email address.'; fEmail.focus(); return; }

    var lines = ['Hi! I would like to book a discovery call.', '', 'Name: ' + name, 'Phone: ' + phone];
    if (fEmail.value.trim())   { lines.push('Email: ' + fEmail.value.trim()); }
    if (fService.value)        { lines.push('Service: ' + fService.value); }
    if (fDate.value)           { lines.push('Preferred date: ' + prettyDate(fDate.value)); }
    if (fMessage.value.trim()) { lines.push('Message: ' + fMessage.value.trim()); }
    var text = lines.join('\n');

    if (!isPlaceholder(SITE.whatsapp)) {
      openExternal(waLink(text));
      statusBox.textContent = 'Opening WhatsApp. Please press send there to share your request.';
    } else if (!isPlaceholder(SITE.email)) {
      openExternal('mailto:' + SITE.email + '?subject=' + encodeURIComponent('Discovery call request') + '&body=' + encodeURIComponent(text));
      statusBox.textContent = 'Opening your email app. Please press send to share your request.';
    } else {
      statusBox.textContent = 'Almost there! Add your WhatsApp number or email in SITE SETTINGS to switch this form on.';
    }
  });

  /* ---------- Footer year ---------- */
  var y = $('#year');
  if (y) { y.textContent = new Date().getFullYear(); }
})();
</script>
</body>
</html>
