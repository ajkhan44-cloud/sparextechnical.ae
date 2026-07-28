[index.html](https://github.com/user-attachments/files/30473704/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Spare X Technical Supplies — Defence & Energy Spare Parts</title>
<meta name="description" content="Spare X Technical Supplies — Trusted supplier of critical spare parts for the defence sector and oil & gas industry.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800&family=Inter:wght@400;500;600&family=Roboto+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
/* ===================== TOKENS ===================== */
:root{
  --void:#0B0F14;
  --deep:#131B24;
  --panel:#1A2534;
  --rule:#253040;
  --amber:#E8A230;
  --amber-dim:#B07820;
  --steel:#8FA0B0;
  --fog:#C5D0D8;
  --white:#F0F4F7;
  --danger:#C0392B;
  --font-display:'Barlow Condensed',sans-serif;
  --font-body:'Inter',sans-serif;
  --font-mono:'Roboto Mono',monospace;
}
*{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{
  background:var(--void);
  color:var(--fog);
  font-family:var(--font-body);
  font-size:16px;
  line-height:1.6;
}
a{color:inherit;text-decoration:none;}
img{display:block;max-width:100%;}

/* ===================== NAV ===================== */
nav{
  position:fixed;top:0;left:0;right:0;z-index:100;
  background:rgba(11,15,20,0.92);
  backdrop-filter:blur(8px);
  border-bottom:1px solid var(--rule);
  display:flex;align-items:center;justify-content:space-between;
  padding:0 40px;
  height:64px;
}
.nav-logo{
  font-family:var(--font-display);
  font-size:22px;
  font-weight:800;
  letter-spacing:1px;
  color:var(--white);
}
.nav-logo span{color:var(--amber);}
.nav-links{display:flex;gap:32px;align-items:center;}
.nav-links a{
  font-size:13px;font-weight:500;letter-spacing:0.5px;
  color:var(--steel);text-transform:uppercase;
  transition:color 0.2s;
}
.nav-links a:hover{color:var(--amber);}
.nav-cta{
  background:var(--amber);color:var(--void)!important;
  padding:9px 20px;font-weight:600!important;
  letter-spacing:0.5px;
}
.nav-cta:hover{background:#f0b840!important;color:var(--void)!important;}
.nav-hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;background:none;border:none;padding:4px;}
.nav-hamburger span{display:block;width:24px;height:2px;background:var(--fog);}
@media(max-width:768px){
  .nav-links{display:none;position:absolute;top:64px;left:0;right:0;background:var(--deep);flex-direction:column;padding:24px 32px;gap:20px;border-bottom:1px solid var(--rule);}
  .nav-links.open{display:flex;}
  .nav-hamburger{display:flex;}
  nav{padding:0 24px;}
}

/* ===================== HERO ===================== */
#hero{
  min-height:100vh;
  padding-top:64px;
  display:flex;align-items:center;
  position:relative;overflow:hidden;
  background:var(--void);
}
.hero-grid-bg{
  position:absolute;inset:0;
  background-image:
    linear-gradient(var(--rule) 1px, transparent 1px),
    linear-gradient(90deg, var(--rule) 1px, transparent 1px);
  background-size:60px 60px;
  opacity:0.35;
}
.hero-glow{
  position:absolute;
  width:600px;height:600px;
  background:radial-gradient(circle, rgba(232,162,48,0.12) 0%, transparent 70%);
  top:-100px;right:-100px;
  pointer-events:none;
}
.hero-inner{
  position:relative;z-index:2;
  max-width:1100px;margin:0 auto;
  padding:80px 40px;
  display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:center;
}
.hero-eyebrow{
  font-family:var(--font-mono);
  font-size:12px;letter-spacing:3px;
  color:var(--amber);text-transform:uppercase;
  margin-bottom:18px;
  display:flex;align-items:center;gap:10px;
}
.hero-eyebrow::before{content:"";display:block;width:32px;height:1px;background:var(--amber);}
.hero-h1{
  font-family:var(--font-display);
  font-size:clamp(48px,6vw,80px);
  font-weight:800;
  line-height:0.95;
  letter-spacing:1px;
  color:var(--white);
  text-transform:uppercase;
  margin-bottom:24px;
}
.hero-h1 em{color:var(--amber);font-style:normal;}
.hero-p{
  font-size:17px;color:var(--steel);
  max-width:440px;margin-bottom:36px;line-height:1.7;
}
.hero-actions{display:flex;gap:16px;flex-wrap:wrap;}
.btn-primary{
  background:var(--amber);color:var(--void);
  font-family:var(--font-display);font-size:16px;font-weight:700;
  letter-spacing:1px;text-transform:uppercase;
  padding:14px 32px;border:none;cursor:pointer;
  transition:background 0.2s,transform 0.15s;display:inline-block;
}
.btn-primary:hover{background:#f0b840;transform:translateY(-1px);}
.btn-ghost{
  border:1px solid var(--rule);color:var(--fog);
  font-family:var(--font-display);font-size:16px;font-weight:600;
  letter-spacing:1px;text-transform:uppercase;
  padding:14px 32px;cursor:pointer;
  transition:border-color 0.2s,color 0.2s;display:inline-block;
}
.btn-ghost:hover{border-color:var(--amber);color:var(--amber);}
.hero-specs{
  display:grid;grid-template-columns:1fr 1fr;gap:2px;
}
.spec-card{
  background:var(--panel);
  border:1px solid var(--rule);
  padding:28px 24px;
  position:relative;
}
.spec-card::before{
  content:"";position:absolute;top:0;left:0;right:0;height:2px;
  background:var(--amber);opacity:0;transition:opacity 0.2s;
}
.spec-card:hover::before{opacity:1;}
.spec-icon{
  font-size:28px;margin-bottom:12px;
}
.spec-label{
  font-family:var(--font-mono);font-size:10px;letter-spacing:2px;
  color:var(--steel);text-transform:uppercase;margin-bottom:6px;
}
.spec-val{
  font-family:var(--font-display);font-size:26px;font-weight:700;
  color:var(--white);
}
@media(max-width:900px){
  .hero-inner{grid-template-columns:1fr;gap:48px;}
  .hero-specs{grid-template-columns:1fr 1fr;}
}
@media(max-width:480px){
  .hero-inner{padding:60px 24px;}
  .hero-specs{grid-template-columns:1fr 1fr;}
}

/* ===================== SECTORS ===================== */
#sectors{background:var(--deep);padding:100px 40px;}
.section-wrap{max-width:1100px;margin:0 auto;}
.section-tag{
  font-family:var(--font-mono);font-size:11px;letter-spacing:3px;
  color:var(--amber);text-transform:uppercase;margin-bottom:12px;
}
.section-h2{
  font-family:var(--font-display);font-size:clamp(36px,5vw,56px);
  font-weight:800;color:var(--white);text-transform:uppercase;
  line-height:1;margin-bottom:16px;
}
.section-sub{color:var(--steel);max-width:520px;margin-bottom:56px;font-size:16px;}
.sectors-grid{
  display:grid;grid-template-columns:1fr 1fr;gap:2px;
}
.sector-card{
  background:var(--panel);
  padding:48px 40px;
  position:relative;overflow:hidden;
  cursor:default;
}
.sector-card::after{
  content:"";position:absolute;
  bottom:0;left:0;right:0;height:3px;
  background:linear-gradient(90deg, var(--amber), transparent);
  transform:scaleX(0);transform-origin:left;
  transition:transform 0.4s ease;
}
.sector-card:hover::after{transform:scaleX(1);}
.sector-bg-text{
  position:absolute;right:-10px;top:50%;transform:translateY(-50%);
  font-family:var(--font-display);font-size:110px;font-weight:800;
  color:var(--rule);line-height:1;pointer-events:none;user-select:none;
  letter-spacing:-2px;
}
.sector-icon-wrap{
  width:56px;height:56px;
  background:var(--rule);
  display:flex;align-items:center;justify-content:center;
  font-size:26px;margin-bottom:24px;
}
.sector-h3{
  font-family:var(--font-display);font-size:28px;font-weight:700;
  color:var(--white);text-transform:uppercase;margin-bottom:12px;
}
.sector-p{color:var(--steel);font-size:15px;line-height:1.7;margin-bottom:24px;}
.sector-tags{display:flex;flex-wrap:wrap;gap:8px;}
.sector-tag-pill{
  font-family:var(--font-mono);font-size:10px;letter-spacing:1px;
  background:var(--rule);color:var(--steel);
  padding:4px 10px;text-transform:uppercase;
}
@media(max-width:700px){.sectors-grid{grid-template-columns:1fr;}}

/* ===================== CATALOGUE ===================== */
#catalogue{padding:100px 40px;background:var(--void);}
.cat-controls{
  display:flex;gap:12px;flex-wrap:wrap;margin-bottom:40px;
}
.cat-filter{
  font-family:var(--font-mono);font-size:11px;letter-spacing:1.5px;
  text-transform:uppercase;padding:8px 18px;
  background:var(--panel);border:1px solid var(--rule);
  color:var(--steel);cursor:pointer;transition:all 0.2s;
}
.cat-filter.active,.cat-filter:hover{
  background:var(--amber);border-color:var(--amber);color:var(--void);
}
.cat-grid{
  display:grid;grid-template-columns:repeat(auto-fill,minmax(270px,1fr));
  gap:16px;
}
.cat-card{
  background:var(--panel);border:1px solid var(--rule);
  padding:24px;transition:border-color 0.2s;
  display:flex;flex-direction:column;
}
.cat-card:hover{border-color:var(--amber);}
.cat-card-sector{
  font-family:var(--font-mono);font-size:10px;letter-spacing:2px;
  color:var(--amber);text-transform:uppercase;margin-bottom:8px;
}
.cat-card h4{
  font-family:var(--font-display);font-size:20px;font-weight:700;
  color:var(--white);text-transform:uppercase;margin-bottom:8px;
}
.cat-card p{font-size:13px;color:var(--steel);flex:1;margin-bottom:16px;}
.cat-card-ref{
  font-family:var(--font-mono);font-size:10px;color:var(--rule);
  border-top:1px solid var(--rule);padding-top:10px;margin-top:auto;
}
.enquire-btn{
  display:inline-block;margin-top:12px;
  font-family:var(--font-mono);font-size:11px;letter-spacing:1px;
  text-transform:uppercase;color:var(--amber);
  border:1px solid var(--amber);padding:7px 14px;
  transition:background 0.2s,color 0.2s;cursor:pointer;background:none;
  text-align:center;
}
.enquire-btn:hover{background:var(--amber);color:var(--void);}

/* ===================== WHY US ===================== */
#why{background:var(--deep);padding:100px 40px;}
.why-grid{
  display:grid;grid-template-columns:1fr 1fr 1fr;
  gap:2px;margin-top:56px;
}
.why-card{
  background:var(--panel);padding:36px 28px;
  border-top:2px solid transparent;transition:border-color 0.2s;
}
.why-card:hover{border-color:var(--amber);}
.why-num{
  font-family:var(--font-display);font-size:48px;font-weight:800;
  color:var(--rule);margin-bottom:12px;
}
.why-h3{
  font-family:var(--font-display);font-size:22px;font-weight:700;
  color:var(--white);text-transform:uppercase;margin-bottom:10px;
}
.why-p{font-size:14px;color:var(--steel);line-height:1.7;}
@media(max-width:700px){.why-grid{grid-template-columns:1fr;}}

/* ===================== CONTACT ===================== */
#contact{padding:100px 40px;background:var(--void);}
.contact-grid{
  display:grid;grid-template-columns:1fr 1fr;gap:60px;margin-top:56px;
}
.contact-info h3{
  font-family:var(--font-display);font-size:28px;font-weight:700;
  color:var(--white);text-transform:uppercase;margin-bottom:20px;
}
.contact-info p{color:var(--steel);font-size:15px;line-height:1.7;margin-bottom:28px;}
.contact-detail{
  display:flex;align-items:flex-start;gap:14px;
  margin-bottom:20px;
}
.contact-detail-icon{
  font-size:18px;min-width:28px;padding-top:2px;
}
.contact-detail-text{
  font-size:14px;color:var(--fog);
}
.contact-detail-text strong{display:block;color:var(--white);font-family:var(--font-mono);font-size:11px;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:3px;}
/* FORM */
.contact-form{background:var(--panel);border:1px solid var(--rule);padding:36px;}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:16px;}
.form-group{display:flex;flex-direction:column;margin-bottom:16px;}
.form-group label{
  font-family:var(--font-mono);font-size:10px;letter-spacing:2px;
  text-transform:uppercase;color:var(--steel);margin-bottom:7px;
}
.form-group input,.form-group select,.form-group textarea{
  background:var(--deep);border:1px solid var(--rule);
  color:var(--fog);font-family:var(--font-body);font-size:14px;
  padding:11px 14px;outline:none;
  transition:border-color 0.2s;
}
.form-group input:focus,.form-group select:focus,.form-group textarea:focus{
  border-color:var(--amber);
}
.form-group textarea{resize:vertical;min-height:120px;}
.form-group select option{background:var(--deep);}
.form-notice{font-size:12px;color:var(--steel);margin-bottom:20px;}
.form-success{
  display:none;text-align:center;padding:28px;
  background:rgba(76,122,93,0.15);border:1px solid #4C7A5D;
  color:#7dba95;font-family:var(--font-mono);font-size:13px;
  letter-spacing:0.5px;margin-top:16px;
}
@media(max-width:700px){
  .contact-grid{grid-template-columns:1fr;}
  .form-row{grid-template-columns:1fr;}
}

/* ===================== FOOTER ===================== */
footer{
  background:var(--deep);
  border-top:1px solid var(--rule);
  padding:40px;
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:20px;
}
.footer-logo{
  font-family:var(--font-display);font-size:20px;font-weight:800;
  color:var(--white);letter-spacing:1px;
}
.footer-logo span{color:var(--amber);}
.footer-copy{
  font-family:var(--font-mono);font-size:11px;color:var(--steel);
}
.footer-links{display:flex;gap:24px;}
.footer-links a{
  font-family:var(--font-mono);font-size:11px;letter-spacing:1px;
  text-transform:uppercase;color:var(--steel);
  transition:color 0.2s;
}
.footer-links a:hover{color:var(--amber);}

/* ===================== SCROLL REVEAL ===================== */
.reveal{opacity:0;transform:translateY(24px);transition:opacity 0.5s ease, transform 0.5s ease;}
.reveal.visible{opacity:1;transform:none;}
@media(prefers-reduced-motion:reduce){
  .reveal{opacity:1;transform:none;}
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo"><span>X</span> SPARE X</div>
  <button class="nav-hamburger" id="hamburger" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
  <div class="nav-links" id="nav-links">
    <a href="#sectors">Sectors</a>
    <a href="#catalogue">Catalogue</a>
    <a href="#why">About</a>
    <a href="#contact" class="nav-cta">Request a Quote</a>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-grid-bg"></div>
  <div class="hero-glow"></div>
  <div class="hero-inner">
    <div>
      <div class="hero-eyebrow">Critical Supply Chain Solutions</div>
      <h1 class="hero-h1">Parts That<br>Keep <em>Critical</em><br>Systems Running</h1>
      <p class="hero-p">Spare X Technical Supplies delivers verified spare parts to defence operators and oil & gas facilities worldwide — where failure is not an option.</p>
      <div class="hero-actions">
        <a href="#catalogue" class="btn-primary">Browse Catalogue</a>
        <a href="#contact" class="btn-ghost">Request a Quote</a>
      </div>
    </div>
    <div class="hero-specs">
      <div class="spec-card">
        <div class="spec-icon">🛡️</div>
        <div class="spec-label">Defence Clients</div>
        <div class="spec-val">Mil-Spec</div>
      </div>
      <div class="spec-card">
        <div class="spec-icon">🛢️</div>
        <div class="spec-label">Oil & Gas</div>
        <div class="spec-val">Upstream &amp; Down</div>
      </div>
      <div class="spec-card">
        <div class="spec-icon">⚙️</div>
        <div class="spec-label">Parts Available</div>
        <div class="spec-val">10,000+</div>
      </div>
      <div class="spec-card">
        <div class="spec-icon">📦</div>
        <div class="spec-label">Fulfillment</div>
        <div class="spec-val">Global</div>
      </div>
    </div>
  </div>
</section>

<!-- SECTORS -->
<section id="sectors">
  <div class="section-wrap">
    <div class="section-tag reveal">Sectors We Serve</div>
    <h2 class="section-h2 reveal">Two Industries.<br>One Trusted Partner.</h2>
    <p class="section-sub reveal">We specialise exclusively in two mission-critical verticals — so our procurement, compliance, and logistics processes are built around their specific demands.</p>
    <div class="sectors-grid reveal">
      <div class="sector-card">
        <div class="sector-bg-text">DEF</div>
        <div class="sector-icon-wrap">🛡️</div>
        <h3 class="sector-h3">Defence Sector</h3>
        <p class="sector-p">We supply spare parts for military ground vehicles, naval platforms, airfield equipment, and communication systems. All components meet relevant mil-spec standards and are sourced through verified channels.</p>
        <div class="sector-tags">
          <span class="sector-tag-pill">Land Systems</span>
          <span class="sector-tag-pill">Naval Equipment</span>
          <span class="sector-tag-pill">Airfield GSE</span>
          <span class="sector-tag-pill">Communications</span>
          <span class="sector-tag-pill">Power Generation</span>
        </div>
      </div>
      <div class="sector-card">
        <div class="sector-bg-text">O&G</div>
        <div class="sector-icon-wrap">🛢️</div>
        <h3 class="sector-h3">Oil &amp; Gas</h3>
        <p class="sector-p">From upstream drilling operations to downstream refineries, we stock and source OEM and equivalent parts for rotating equipment, valves, instrumentation, and safety systems.</p>
        <div class="sector-tags">
          <span class="sector-tag-pill">Rotating Equipment</span>
          <span class="sector-tag-pill">Valves &amp; Actuators</span>
          <span class="sector-tag-pill">Instrumentation</span>
          <span class="sector-tag-pill">Safety Systems</span>
          <span class="sector-tag-pill">Drilling Components</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CATALOGUE -->
<section id="catalogue">
  <div class="section-wrap">
    <div class="section-tag reveal">Product Catalogue</div>
    <h2 class="section-h2 reveal">What We Supply</h2>
    <p class="section-sub reveal">A selection of our most commonly requested categories. Can't find what you need? Send us a part number — our procurement team will source it.</p>
    <div class="cat-controls reveal">
      <button class="cat-filter active" data-filter="all">All Categories</button>
      <button class="cat-filter" data-filter="defence">Defence</button>
      <button class="cat-filter" data-filter="oilgas">Oil &amp; Gas</button>
      <button class="cat-filter" data-filter="shared">Cross-Sector</button>
    </div>
    <div class="cat-grid" id="cat-grid"></div>
  </div>
</section>

<!-- WHY US -->
<section id="why">
  <div class="section-wrap">
    <div class="section-tag reveal">Why Spare X</div>
    <h2 class="section-h2 reveal">Built for Industries<br>Where Parts Can't Fail</h2>
    <div class="why-grid">
      <div class="why-card reveal">
        <div class="why-num">01</div>
        <h3 class="why-h3">Verified Sourcing</h3>
        <p class="why-p">Every part is procured through approved and auditable supply chains. We maintain full traceability from manufacturer to delivery, so you get exactly what's specified.</p>
      </div>
      <div class="why-card reveal">
        <div class="why-num">02</div>
        <h3 class="why-h3">Sector Expertise</h3>
        <p class="why-p">Our team has deep experience in defence procurement and oil & gas MRO. We understand regulatory requirements, export compliance, and the urgency of operational downtime.</p>
      </div>
      <div class="why-card reveal">
        <div class="why-num">03</div>
        <h3 class="why-h3">Fast Turnaround</h3>
        <p class="why-p">We maintain strategic stock of high-demand items and have established relationships with OEMs to reduce lead times when you need parts quickly.</p>
      </div>
      <div class="why-card reveal">
        <div class="why-num">04</div>
        <h3 class="why-h3">Global Logistics</h3>
        <p class="why-p">From the Gulf to international defence installations, we handle export documentation, customs clearance, and last-mile delivery to site or base.</p>
      </div>
      <div class="why-card reveal">
        <div class="why-num">05</div>
        <h3 class="why-h3">Confidential Enquiries</h3>
        <p class="why-p">We understand the sensitivity of defence procurement. All enquiries and supplier relationships are handled with full discretion and NDAs available on request.</p>
      </div>
      <div class="why-card reveal">
        <div class="why-num">06</div>
        <h3 class="why-h3">Quality Assurance</h3>
        <p class="why-p">Parts are inspected and documented before dispatch. We provide full material certificates, test reports, and compliance paperwork as required.</p>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-wrap">
    <div class="section-tag reveal">Get in Touch</div>
    <h2 class="section-h2 reveal">Request a Quote<br>or Send a Part Number</h2>
    <div class="contact-grid">
      <div class="contact-info reveal">
        <h3>Talk to Our Supply Team</h3>
        <p>Whether you have a part number ready or need help identifying the right component, our team responds to all enquiries within 24 hours.</p>
        <div class="contact-detail">
          <div class="contact-detail-icon">📧</div>
          <div class="contact-detail-text">
            <strong>Email</strong>
            sales@sparextechnical.ae
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-detail-icon">📞</div>
          <div class="contact-detail-text">
            <strong>Phone / WhatsApp</strong>
            +971 50 772 5348
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-detail-icon">📍</div>
          <div class="contact-detail-text">
            <strong>Location</strong>
            Abu Dhabi, United Arab Emirates<br><a href="https://sparextechnical.com" style="color:var(--amber);">sparextechnical.com</a>
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-detail-icon">⏱️</div>
          <div class="contact-detail-text">
            <strong>Response Time</strong>
            Within 24 hours — business days
          </div>
        </div>
      </div>
      <div class="reveal">
        <div class="contact-form">
          <!-- 
            FORMSPREE SETUP (one-time, 2 minutes):
            1. Go to https://formspree.io and sign up free
            2. Create a new form → enter sales@sparextechnical.ae as the email
            3. Copy your form endpoint (looks like https://formspree.io/f/xxxxxxxx)
            4. Replace "YOUR_FORMSPREE_ID" below with just the ID part (e.g. xbjvkpqz)
          -->
          <form id="enquiry-form" action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST">
          <div class="form-row">
            <div class="form-group">
              <label for="f-name">Full Name</label>
              <input type="text" id="f-name" name="name" placeholder="Your name" required>
            </div>
            <div class="form-group">
              <label for="f-company">Company</label>
              <input type="text" id="f-company" name="company" placeholder="Organisation name">
            </div>
          </div>
          <div class="form-row">
            <div class="form-group">
              <label for="f-email">Email Address</label>
              <input type="email" id="f-email" name="email" placeholder="you@company.com" required>
            </div>
            <div class="form-group">
              <label for="f-phone">Phone / WhatsApp</label>
              <input type="tel" id="f-phone" name="phone" placeholder="+971...">
            </div>
          </div>
          <div class="form-group">
            <label for="f-sector">Sector</label>
            <select id="f-sector" name="sector">
              <option value="">Select sector</option>
              <option>Defence</option>
              <option>Oil &amp; Gas</option>
              <option>Other / Mixed</option>
            </select>
          </div>
          <div class="form-group">
            <label for="f-message">Part Numbers / Description / Requirements</label>
            <textarea id="f-message" name="message" placeholder="Paste part numbers, describe your requirement, or ask a general question..."></textarea>
          </div>
          <p class="form-notice">All enquiries are treated with full confidentiality.</p>
          <button type="submit" class="btn-primary" id="submit-enquiry" style="width:100%;text-align:center;">Send Enquiry</button>
          <div class="form-success" id="form-success">
            ✔ Enquiry received — our team will respond within 24 hours.
          </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo"><span>X</span> SPARE X TECHNICAL SUPPLIES</div>
  <div class="footer-copy">© 2025 Spare X Technical Supplies. All rights reserved.</div>
  <div class="footer-links">
    <a href="#sectors">Sectors</a>
    <a href="#catalogue">Catalogue</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

<script>
// NAV TOGGLE
document.getElementById('hamburger').addEventListener('click', () => {
  document.getElementById('nav-links').classList.toggle('open');
});
document.querySelectorAll('.nav-links a').forEach(a => {
  a.addEventListener('click', () => document.getElementById('nav-links').classList.remove('open'));
});

// CATALOGUE DATA
const products = [
  {sector:'defence', name:'Engine Gasket Sets', desc:'Full gasket kits for military diesel engines. Manufactured to OEM specifications for common land system powerplants.', ref:'SX-DEF-0021'},
  {sector:'defence', name:'Hydraulic Actuators', desc:'Linear and rotary actuators for armoured vehicle turret systems. Heat and dust-resistant sealing.', ref:'SX-DEF-0034'},
  {sector:'defence', name:'Military-Grade Connectors', desc:'MIL-DTL rated circular and rectangular connectors for comms and control systems in harsh field environments.', ref:'SX-DEF-0058'},
  {sector:'defence', name:'Power Distribution Panels', desc:'24V/28V DC distribution units used in tactical vehicles and mobile command units.', ref:'SX-DEF-0072'},
  {sector:'oilgas', name:'Gate & Ball Valves', desc:'API 6A / 6D rated gate and ball valves for wellhead, pipeline, and process plant applications.', ref:'SX-OG-0011'},
  {sector:'oilgas', name:'Pump Mechanical Seals', desc:'Single and double mechanical seals for centrifugal and progressive cavity pumps in upstream operations.', ref:'SX-OG-0029'},
  {sector:'oilgas', name:'Pressure Transmitters', desc:'HART-compatible pressure transmitters for process monitoring in refinery and upstream applications.', ref:'SX-OG-0047'},
  {sector:'oilgas', name:'Safety Relief Valves', desc:'Spring-loaded and pilot-operated pressure relief valves for ASME and API 526 compliant installations.', ref:'SX-OG-0063'},
  {sector:'shared', name:'Bearing Assemblies', desc:'SKF, NSK, and OEM-equivalent bearing sets for rotating equipment across both defence and industrial applications.', ref:'SX-GEN-0009'},
  {sector:'shared', name:'V-Belts & Drive Chains', desc:'Industrial-grade power transmission components. Available in standard and reinforced profiles for high-load environments.', ref:'SX-GEN-0017'},
  {sector:'shared', name:'Diesel Generator Parts', desc:'Fuel injectors, filters, cooling system components, and control boards for Cummins, Perkins, and Caterpillar gensets.', ref:'SX-GEN-0033'},
  {sector:'shared', name:'Cable Glands & Conduit Fittings', desc:'IP66/68 rated cable glands and armoured conduit fittings for classified and industrial enclosures.', ref:'SX-GEN-0044'},
];

const sectorLabel = {defence:'Defence', oilgas:'Oil & Gas', shared:'Cross-Sector'};
const grid = document.getElementById('cat-grid');

function renderCatalogue(filter){
  const list = filter === 'all' ? products : products.filter(p => p.sector === filter);
  grid.innerHTML = list.map(p => `
    <div class="cat-card">
      <div class="cat-card-sector">${sectorLabel[p.sector]}</div>
      <h4>${p.name}</h4>
      <p>${p.desc}</p>
      <div class="cat-card-ref">REF: ${p.ref}</div>
      <a href="#contact" class="enquire-btn">Enquire Now</a>
    </div>
  `).join('');
}
renderCatalogue('all');

document.querySelectorAll('.cat-filter').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.cat-filter').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    renderCatalogue(btn.dataset.filter);
  });
});

// CONTACT FORM — Formspree
const form = document.getElementById('enquiry-form');
form.addEventListener('submit', async (e) => {
  e.preventDefault();
  const btn = document.getElementById('submit-enquiry');
  btn.disabled = true;
  btn.textContent = 'Sending…';
  try {
    const res = await fetch(form.action, {
      method: 'POST',
      body: new FormData(form),
      headers: { 'Accept': 'application/json' }
    });
    if(res.ok){
      document.getElementById('form-success').style.display = 'block';
      btn.textContent = 'Enquiry Sent ✔';
      form.reset();
    } else {
      btn.disabled = false;
      btn.textContent = 'Send Enquiry';
      alert('There was a problem sending your enquiry. Please email us directly at sales@sparextechnical.ae');
    }
  } catch(err) {
    btn.disabled = false;
    btn.textContent = 'Send Enquiry';
    alert('Network error. Please email us directly at sales@sparextechnical.ae');
  }
});

// SCROLL REVEAL
const revealEls = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting){ e.target.classList.add('visible'); observer.unobserve(e.target); } });
}, {threshold:0.1});
revealEls.forEach(el => observer.observe(el));
</script>
</body>
</html>
