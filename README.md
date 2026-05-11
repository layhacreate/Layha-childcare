[index-4.html](https://github.com/user-attachments/files/27420658/index-4.html)
# Layha-childcare<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>Layha the Familysitter</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Nunito:wght@400;500;600;700&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
:root{
  --pink:#E91E8C;--pink-light:#fce4f3;--pink-dark:#c0157a;
  --pink-soft:#fff0f9;--pink-mid:#f48ec8;
  --text:#1a1a1a;--text2:#555;--text3:#999;
  --bg:#fff;--bg2:#fafafa;
  --border:#f0e0eb;
  --radius:16px;--radius-sm:10px;
  --shadow:0 4px 24px rgba(233,30,140,0.10);
  --shadow-lg:0 8px 40px rgba(233,30,140,0.15);
}
html{scroll-behavior:smooth;}
body{font-family:'Nunito',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;}
h1,h2,h3{font-family:'Playfair Display',serif;font-weight:700;}

/* NAV */
nav{position:sticky;top:0;z-index:100;background:#fff;border-bottom:1px solid var(--border);padding:0 2rem;}
.nav-inner{max-width:1100px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;height:70px;}
.nav-logo{display:flex;align-items:center;gap:10px;text-decoration:none;}
.nav-logo-icon{font-size:28px;}
.nav-logo-text{font-family:'Playfair Display',serif;font-size:20px;color:var(--pink);line-height:1.2;}
.nav-logo-text span{color:var(--text);font-weight:400;font-style:italic;}
.nav-links{display:flex;gap:4px;align-items:center;}
.nav-links a{text-decoration:none;font-size:13px;font-weight:600;color:var(--text2);padding:8px 12px;border-radius:8px;transition:all .2s;white-space:nowrap;}
.nav-links a:hover,.nav-links a.active{color:var(--pink);background:var(--pink-light);}
.hamburger{display:none;background:none;border:none;cursor:pointer;padding:8px;flex-direction:column;gap:5px;}
.hamburger span{display:block;width:24px;height:2px;background:var(--text);border-radius:2px;transition:all .3s;}
.mobile-menu{display:none;position:fixed;top:70px;left:0;right:0;background:#fff;border-bottom:1px solid var(--border);padding:1rem 2rem;z-index:99;flex-direction:column;gap:4px;box-shadow:0 8px 24px rgba(0,0,0,0.08);}
.mobile-menu.open{display:flex;}
.mobile-menu a{text-decoration:none;font-size:15px;font-weight:600;color:var(--text2);padding:12px 16px;border-radius:8px;transition:all .2s;}
.mobile-menu a:hover,.mobile-menu a.active{color:var(--pink);background:var(--pink-light);}

/* PAGES */
.page{display:none;animation:fadeIn .4s ease;}
.page.active{display:block;}
@keyframes fadeIn{from{opacity:0;transform:translateY(12px);}to{opacity:1;transform:translateY(0);}}

/* HERO */
.hero{position:relative;min-height:520px;display:flex;align-items:center;justify-content:center;text-align:center;overflow:hidden;background:linear-gradient(135deg,#fff0f9 0%,#fce4f3 50%,#fff0f9 100%);}
.hero::before{content:'';position:absolute;inset:0;background:url('https://images.unsplash.com/photo-1587654780291-39c9404d746b?w=1400&q=80') center/cover no-repeat;opacity:.18;}
.hero-content{position:relative;z-index:1;max-width:700px;padding:4rem 2rem;}
.hero-badge{display:inline-block;background:var(--pink);color:#fff;font-size:12px;font-weight:700;padding:6px 16px;border-radius:20px;letter-spacing:.08em;text-transform:uppercase;margin-bottom:1.5rem;}
.hero h1{font-size:clamp(2rem,5vw,3.5rem);color:var(--text);line-height:1.15;margin-bottom:1rem;}
.hero h1 em{color:var(--pink);font-style:normal;}
.hero p{font-size:18px;color:var(--text2);margin-bottom:2rem;line-height:1.6;}
.btn-pink{display:inline-block;background:var(--pink);color:#fff;padding:14px 32px;border-radius:50px;font-size:15px;font-weight:700;text-decoration:none;border:none;cursor:pointer;transition:all .2s;font-family:'Nunito',sans-serif;box-shadow:0 4px 20px rgba(233,30,140,0.3);}
.btn-pink:hover{background:var(--pink-dark);transform:translateY(-2px);box-shadow:0 8px 28px rgba(233,30,140,0.4);}
.btn-outline-pink{display:inline-block;background:transparent;color:var(--pink);padding:13px 30px;border-radius:50px;font-size:15px;font-weight:700;text-decoration:none;border:2px solid var(--pink);cursor:pointer;transition:all .2s;font-family:'Nunito',sans-serif;}
.btn-outline-pink:hover{background:var(--pink);color:#fff;}

/* SECTIONS */
.section{padding:5rem 2rem;}
.section-inner{max-width:1000px;margin:0 auto;}
.section-alt{background:var(--pink-soft);}
.section-pink{background:var(--pink);color:#fff;}
.section-dark{background:#1a1a1a;color:#fff;}
.section-title{font-size:clamp(1.8rem,4vw,2.8rem);margin-bottom:1rem;}
.section-title.pink{color:var(--pink);}
.section-title.white{color:#fff;}
.section-sub{font-size:16px;color:var(--text2);max-width:600px;margin:0 auto 3rem;line-height:1.7;}
.section-sub.white{color:rgba(255,255,255,0.85);}
.text-center{text-align:center;}

/* CARDS */
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:1.5rem;margin-top:2rem;}
.card{background:#fff;border-radius:var(--radius);padding:2rem;border:1px solid var(--border);transition:all .3s;}
.card:hover{transform:translateY(-4px);box-shadow:var(--shadow-lg);}
.card-icon{font-size:2.5rem;margin-bottom:1rem;}
.card h3{font-size:1.2rem;margin-bottom:.5rem;color:var(--text);}
.card p{font-size:14px;color:var(--text2);line-height:1.7;}

/* TWO COL */
.two-col{display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:center;}
.two-col img{width:100%;border-radius:var(--radius);object-fit:cover;box-shadow:var(--shadow-lg);}
.two-col-text h2{font-size:clamp(1.6rem,3vw,2.2rem);margin-bottom:1rem;color:var(--text);}
.two-col-text h2 span{color:var(--pink);}
.two-col-text p{font-size:15px;color:var(--text2);line-height:1.8;margin-bottom:1rem;}

/* QUOTE */
.quote-section{padding:4rem 2rem;background:var(--pink);text-align:center;}
.quote-section blockquote{font-family:'Playfair Display',serif;font-size:clamp(1.3rem,3vw,2rem);color:#fff;font-style:italic;max-width:800px;margin:0 auto 1rem;line-height:1.5;}
.quote-section cite{font-size:14px;color:rgba(255,255,255,0.8);font-style:normal;font-weight:600;}

/* TABLE */
.price-table{width:100%;border-collapse:collapse;margin-top:1.5rem;border-radius:var(--radius);overflow:hidden;box-shadow:var(--shadow);}
.price-table th{background:var(--pink);color:#fff;padding:14px 20px;font-size:14px;font-weight:700;text-align:left;}
.price-table td{padding:13px 20px;font-size:15px;border-bottom:1px solid var(--border);}
.price-table tr:last-child td{border-bottom:none;}
.price-table tr:nth-child(even) td{background:var(--pink-soft);}

/* POLICY BOXES */
.policy-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1rem;margin-top:2rem;}
.policy-box{background:#fff;border:1px solid var(--border);border-radius:var(--radius-sm);padding:1.5rem;}
.policy-box h4{color:var(--pink);font-size:15px;margin-bottom:.5rem;font-family:'Playfair Display',serif;}
.policy-box p{font-size:13px;color:var(--text2);line-height:1.7;}

/* STEPS */
.steps{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1.5rem;margin-top:2rem;}
.step{text-align:center;padding:1.5rem;}
.step-num{width:52px;height:52px;border-radius:50%;background:var(--pink);color:#fff;font-size:20px;font-weight:700;display:flex;align-items:center;justify-content:center;margin:0 auto 1rem;font-family:'Playfair Display',serif;}
.step h4{font-size:15px;margin-bottom:.5rem;color:var(--text);}
.step p{font-size:13px;color:var(--text2);line-height:1.6;}

/* TESTIMONIALS */
.testimonials{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:1.5rem;margin-top:2rem;}
.testimonial{background:#fff;border:1px solid var(--border);border-radius:var(--radius);padding:2rem;position:relative;}
.testimonial::before{content:'"';font-family:'Playfair Display',serif;font-size:60px;color:var(--pink-light);position:absolute;top:10px;left:20px;line-height:1;}
.testimonial-text{font-size:15px;color:var(--text2);line-height:1.7;margin-bottom:1rem;padding-top:1.5rem;}
.testimonial-author{font-size:13px;font-weight:700;color:var(--pink);}

/* CONTACT */
.contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:start;}
.contact-info h3{font-size:1.5rem;margin-bottom:1.5rem;color:var(--text);}
.contact-item{display:flex;align-items:center;gap:12px;margin-bottom:1rem;font-size:15px;color:var(--text2);}
.contact-item a{color:var(--pink);text-decoration:none;font-weight:600;}
.contact-item a:hover{text-decoration:underline;}
.contact-icon{width:40px;height:40px;border-radius:50%;background:var(--pink-light);display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0;}

/* FOOTER */
footer{background:#1a1a1a;color:rgba(255,255,255,0.7);text-align:center;padding:2rem;font-size:13px;}
footer span{color:var(--pink);}

/* SERVICE TAGS */
.service-tags{display:flex;flex-wrap:wrap;gap:10px;margin-top:1.5rem;}
.tag{background:var(--pink-light);color:var(--pink);padding:8px 18px;border-radius:50px;font-size:13px;font-weight:700;}

/* HIGHLIGHT BOX */
.highlight-box{background:var(--pink);color:#fff;border-radius:var(--radius);padding:2rem;text-align:center;margin-top:2rem;}
.highlight-box h3{font-size:1.4rem;margin-bottom:.75rem;}
.highlight-box p{font-size:15px;opacity:.9;margin-bottom:1.5rem;}

/* FAMILIES BANNER */
.families-banner{background:linear-gradient(135deg,var(--pink) 0%,var(--pink-dark) 100%);border-radius:var(--radius);padding:3rem 2rem;text-align:center;color:#fff;margin-bottom:3rem;}
.families-banner h2{font-size:2rem;margin-bottom:1rem;}
.families-banner p{font-size:16px;opacity:.9;max-width:600px;margin:0 auto;}

@media(max-width:768px){
  nav{padding:0 1rem;}
  .nav-links{display:none;}
  .hamburger{display:flex;}
  .two-col{grid-template-columns:1fr;}
  .two-col img{max-height:280px;}
  .contact-grid{grid-template-columns:1fr;}
  .section{padding:3rem 1.25rem;}
}
</style>
</head>
<body>

<nav>
  <div class="nav-inner">
    <a class="nav-logo" href="#" onclick="showPage('home')">
      <img src= "https://www.image2url.com/r2/default/images/1778503990593-23681749-38c8-42f8-82ce-a881fe2ef283.png" style= "width: 40px ; height 40px:" />
      <div class="nav-logo-text">Layha <span>the familysitter</span></div>
    </a>
    <div class="nav-links">
      <a href="#" class="active" onclick="showPage('home',this)">Home</a>
      <a href="#" onclick="showPage('about',this)">About Me</a>
      <a href="#" onclick="showPage('services',this)">My Services</a>
      <a href="#" onclick="showPage('pricing',this)">Pricing & More</a>
      <a href="#" onclick="showPage('booking',this)">Booking & Availability</a>
      <a href="#" onclick="showPage('families',this)">Families</a>
    </div>
    <button class="hamburger" onclick="toggleMenu()" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<div class="mobile-menu" id="mobileMenu">
  <a href="#" class="active" onclick="showPage('home',this);toggleMenu()">Home</a>
  <a href="#" onclick="showPage('about',this);toggleMenu()">About Me</a>
  <a href="#" onclick="showPage('services',this);toggleMenu()">My Services</a>
  <a href="#" onclick="showPage('pricing',this);toggleMenu()">Pricing & More</a>
  <a href="#" onclick="showPage('booking',this);toggleMenu()">Booking & Availability</a>
  <a href="#" onclick="showPage('families',this);toggleMenu()">Families</a>
</div>

<!-- HOME PAGE -->
<div id="page-home" class="page active">
  <div class="hero">
    <div class="hero-content">
      <div class="hero-badge">Columbus, Ohio</div>
      <h1>Trusted care for the ones you <em>love the most</em></h1>
      <p>Book reliable and convenient childcare for families in the Columbus, Ohio area</p>
      <a href="https://layhachildcare.netlify.app/" class="btn-pink" target="_blank">Schedule Service</a>
    </div>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <h2 class="section-title pink">Flexible Care for Families</h2>
      <p class="section-sub">Are you a busy parent in need of reliable support? I am offering flexible care for families, whether it's for date nights or just some quiet time to get work done. It doesn't matter the reason — my service is convenient and easy to book. You can rest assured knowing your loved ones are in good hands while you take that much-needed break.</p>
      <div class="cards">
        <div class="card">
          <div class="card-icon">🌙</div> 
          <h3>Date Nights</h3>
          <p>Enjoy your evening out knowing your children are safe, happy, and well cared for at home.</p>
        </div>
        <div class="card">
          <div class="card-icon">📋</div>
          <h3>Appointments & Errands</h3>
          <p>Doctor's appointments, work meetings, or just some quiet time — book care that fits your schedule.</p>
        </div>
        <div class="card">
          <div class="card-icon"> <img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/23c2770a-e1e2-4966-a1f7-9ef30d13f89e" />
</div>
          <h3>Summer Days</h3>
          <p>Parks, libraries, Cosi trips, and ice cream — I make every day fun for your little ones.</p>
        </div>
      </div>
    </div>
  </div>

  <div class="section section-alt">
    <div class="section-inner">
      <div class="two-col">
        <img src="https://images.unsplash.com/photo-1516627145497-ae6968895b74?w=600&q=80" alt="Childcare" />
        <div class="two-col-text">
          <h2>About <span>me</span></h2>
          <p>Hello! My name is Delajha Jones, and I am completing an Integrated Language Arts Bachelor's Degree at Ohio State University to become a secondary education teacher.</p>
          <p>While completing my degree, I provide childcare for a few families as needed, and I also substitute teach in the Worthington and Whitehall school districts! My passion, dedication, and PATIENCE grow with each experience I have with my students and the children I sit for.</p>
          <a href="#" onclick="showPage('about')" class="btn-pink" style="margin-top:.5rem;">Continue reading</a>
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-inner">
      <div class="two-col">
        <div class="two-col-text">
          <h2>Easy <span>Scheduling</span></h2>
          <p>Scheduling made convenient, easy, and quick! Block off the time your family needs care — ranging from 3 hours to 6 or EVEN MORE — it's all based on what you need.</p>
          <p>No fixed durations, no confusing calendars. Just pick your date, your start time, and your end time. That's it.</p>
          <a href="https://layhachildcare.netlify.app/" class="btn-pink" target="_blank" style="margin-top:.5rem;">Learn more</a>
        </div>
        <img src="https://images.unsplash.com/photo-1506784983877-45594efa4cbe?w=600&q=80" alt="Calendar scheduling" />
      </div>
    </div>
  </div>

  <div class="section section-alt">
    <div class="section-inner text-center">
      <h2 class="section-title pink">New Families</h2>
      <p class="section-sub">Thank you for your interest in booking with me! I invite new families wishing to schedule a service to book either a phone call or an in-person meeting. This allows us to connect and get to know each other better before moving forward. Please feel free to reach out via phone or email to set up a convenient time for us to chat!</p>
      <a href="mailto:lay011318@gmail.com" class="btn-pink">Get in touch</a>
    </div>
  </div>

  <div class="quote-section">
    <blockquote>"We are so happy that you've been babysitting for us and feel like you do a wonderful job with the kids"</blockquote>
    <cite>— A family I have worked for since July 2025, Columbus, Ohio</cite>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <h2 class="section-title">Contact me</h2>
      <p class="section-sub">Serving Columbus, Ohio, and surrounding areas.</p>
      <div style="display:flex;flex-direction:column;gap:1rem;align-items:center;margin-top:1rem;">
        <div class="contact-item"><div class="contact-icon">📞</div><a href="tel:3302840675">(330) 284-0675</a></div>
        <div class="contact-item"><div class="contact-icon">✉️</div><a href="mailto:lay011318@gmail.com">lay011318@gmail.com</a></div>
        <div class="contact-item"><div class="contact-icon">📍</div><span>Columbus, Ohio & surrounding areas</span></div>
      </div>
    </div>
  </div>
</div>

<!-- ABOUT PAGE -->
<div id="page-about" class="page">
  <div class="hero" style="min-height:320px;">
    <div class="hero-content" style="padding:3rem 2rem;">
      <div class="hero-badge">Get to know me</div>
      <h1>About <em>me</em></h1>
    </div>
  </div>

  <div class="section">
    <div class="section-inner">
      <div class="two-col">
        <img src="https://images.unsplash.com/photo-1544717302-de2939b7ef71?w=600&q=80" alt="About Layha" style="max-height:480px;"/>
        <div class="two-col-text">
          <h2>Hi, I'm <span>Delajha</span></h2>
          <p>Hello! My name is Delajha Jones, and I am completing an Integrated Language Arts Bachelor's Degree at Ohio State University to become a secondary education teacher.</p>
          <p>While completing my degree, I provide childcare for a few families as needed, and I also substitute teach in the Worthington and Whitehall school districts! My passion, dedication, and PATIENCE grow with each experience I have with my students and the children I sit for.</p>
          <p>A few things about me are that I am the oldest sibling of six, I love to be creative — so hide all the markers — and I love to have some fun. Going on walks to the park or library and a trip to Cosi and ice cream are my favorite things to do, and the best ways to enjoy a hot summer day!</p>
          <p>As I begin summer break, I want to use this time to provide convenient care to families as needed. So if something comes up, like a doctor's appointment or a nice dinner date, all you have to do is book.</p>
        </div>
      </div>
    </div>
  </div>

  <div class="section section-alt">
    <div class="section-inner text-center">
      <h2 class="section-title pink">A little more about me</h2>
      <div class="cards" style="margin-top:2rem;">
        <div class="card">
          <div class="card-icon"> <img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/1e0783af-8b44-4506-886a-5a76db30a66f" />
</div>
          <h3> My resume </h3>
          <p> Take a look at my resume to see my certifications and previous work experince </p>
           <a href="https://www.image2url.com/r2/default/documents/1778506195126-bc8c0b00-cac8-438d-91bc-0e8ea1db28f7.pdf" class="btn-pink"> CLICK HERE TO VIEW </a>
        </div>
        <div class="card">
          <div class="card-icon"> <img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/1e3a0028-9c14-404f-afc1-5a4c1364b58a" />
</div>
          <h3> Background check </h3>
          <p> Ohio law requires all licensure candidates to have both Ohio Bureau of Criminal Investigation (BCI) and FBI criminal background checks that are no older than one year (365 days) at the time their first credential is issued. 
These are all the background checks I have on record. My current issue expires 11-13-2026 </p>
          <a href="https://www.image2url.com/r2/default/documents/1778507787318-d1d764e9-6783-4fce-a41b-3b12e38e4bec.pdf" class="btn-pink"> CLICK HERE TO VIEW </a>
        </div>
        <div class="card">
          <div class="card-icon"><img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/8199dc32-915d-47dc-8fd0-7d55ef7b050f" />
</div>
          <h3CPR/ AED / First aid </h3>
          <p> expires 03-35-2027 </p>
           <a href="https://www.image2url.com/r2/default/documents/1778508068690-56451f29-1243-42c7-bab4-d0befafec2c2.pdff" class="btn-pink"> CLICK HERE TO VIEW </a>
         
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <a href="https://layhachildcare.netlify.app/" class="btn-pink" target="_blank">Book with me today</a>
    </div>
  </div>
</div>

<!-- SERVICES PAGE -->
<div id="page-services" class="page">
  <div class="hero" style="min-height:320px;background:linear-gradient(135deg,var(--pink) 0%,var(--pink-dark) 100%);">
    <div class="hero-content" style="padding:3rem 2rem;">
      <div class="hero-badge" style="background:#fff;color:var(--pink);">What I offer</div>
      <h1 style="color:#fff;">Convenient &amp; reliable <em style="color:#ffe0f3;">childcare services</em></h1>
      <p style="color:rgba(255,255,255,0.9);">I am dedicated to providing a safe, fun, and engaging environment for your children, tailored to your unique needs.</p>
      <a href="https://layhachildcare.netlify.app/" class="btn-outline-pink" style="border-color:#fff;color:#fff;" target="_blank">Schedule care — click here</a>
    </div>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <h2 class="section-title pink">What do I offer?</h2>
      <p class="section-sub">I provide a variety of childcare solutions designed to fit your family's schedule and specific requirements. Please remember a 3-hour minimum is strictly enforced unless discussed otherwise for emergencies.</p>
      <div class="cards">
        <div class="card">
          <div class="card-icon">🌙</div>
          <h3>Date Night Care</h3>
          <p>Enjoy your evening out without worry. I'll keep the kids entertained, fed, and happy until you return.</p>
        </div>
        <div class="card">
          <div class="card-icon">🏥</div>
          <h3>Appointment Cover</h3>
          <p>Doctor's appointments, meetings, or errands — I've got the kids covered whenever you need.</p>
        </div>
        <div class="card">
          <div class="card-icon"> <img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/db127285-2c90-48d1-a907-a1a35051fc73" />
</div>
          <h3>Summer Care</h3>
          <p>Full summer availability with fun activities — parks, libraries, creative play, and more.</p>
        </div>
        <div class="card">
          <div class="card-icon"> <img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/b8a0bd37-6bdd-4040-b6dd-95b39f4c6213" />
</div>
          <h3>Work From Home Support</h3>
          <p>Need quiet time to focus? I'll keep the little ones engaged so you can get things done.</p>
        </div>
        <div class="card">
          <div class="card-icon"><img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/f1a6b0b5-f30e-4e9e-bdec-66484afcf876" />
</div>
          <h3>Special Occasions</h3>
          <p>Weddings, parties, or family events — flexible care for those special days.</p>
        </div>
        <div class="card">
          <div class="card-icon">🚨</div>
          <h3>Last-Minute Needs</h3>
          <p>Life happens! Reach out for same-day or short-notice bookings when something comes up.</p>
        </div>
      </div>
    </div>
  </div>

  <div class="section section-alt">
    <div class="section-inner text-center">
      <h2 class="section-title pink">What's included in every session</h2>
      <div class="service-tags" style="justify-content:center;margin-top:1.5rem;">
        <span class="tag">✅ Safe, attentive care</span>
        <span class="tag">✅ Age-appropriate activities</span>
        <span class="tag">✅ Snack & meal assistance</span>
        <span class="tag">✅ Homework help if needed</span>
        <span class="tag">✅ Bedtime routines followed</span>
        <span class="tag">✅ Updates available on request</span>
        <span class="tag">✅ Patient & fun energy</span>
        <span class="tag">✅ Up to 5 children per session</span>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <div class="highlight-box">
        <h3>Ready to book?</h3>
        <p>Check my availability and request your childcare session in just a few minutes.</p>
        <a href="https://layhachildcare.netlify.app/" class="btn-outline-pink" style="border-color:#fff;color:#fff;" target="_blank">View availability & book</a>
      </div>
    </div>
  </div>
</div>

<!-- PRICING PAGE -->
<div id="page-pricing" class="page">
  <div class="hero" style="min-height:320px;">
    <div class="hero-content" style="padding:3rem 2rem;">
      <div class="hero-badge">No surprises</div>
      <h1>Transparent pricing for <em>quality childcare</em></h1>
      <p>I believe in clear and straightforward pricing — explore my hourly rates and policies designed to provide flexible and reliable care for your little ones in Columbus, Ohio.</p>
    </div>
  </div>

  <div class="section">
    <div class="section-inner">
      <h2 class="section-title pink text-center">My hourly rates</h2>
      <p style="text-align:center;font-size:15px;color:var(--text2);margin-bottom:1.5rem;">The family pays the babysitter directly after service is completed. <strong>If family arrives before the scheduled time, the sitter must be compensated for a minimum of 3 hours — non-negotiable.</strong></p>
      <table class="price-table">
        <thead><tr><th>Number of children</th><th>Hourly rate</th></tr></thead>
        <tbody>
          <tr><td>1 child</td><td><strong>$19/hr</strong></td></tr>
          <tr><td>2 children</td><td><strong>$20/hr</strong></td></tr>
          <tr><td>3 children</td><td><strong>$23/hr</strong></td></tr>
          <tr><td>4 children</td><td><strong>$24/hr</strong></td></tr>
          <tr><td>5 children</td><td><strong>$26/hr</strong></td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="section section-alt">
    <div class="section-inner">
      <h2 class="section-title pink text-center">Policies &amp; extra fees</h2>
      <div class="policy-grid" style="margin-top:2rem;">
        <div class="policy-box">
          <h4>🕐 3-Hour Minimum</h4>
          <p>All bookings require a minimum of 3 hours unless discussed otherwise for emergencies. Non-negotiable.</p>
        </div>
        <div class="policy-box">
          <h4>⚡ Same-Day Booking</h4>
          <p>A $20 fee is added for same-day bookings. Life happens — I'll still be there for you!</p>
        </div>
        <div class="policy-box">
          <h4>⏰ Short Notice Fee</h4>
          <p>A $15 fee is added for bookings made with less than 24 hours notice.</p>
        </div>
        <div class="policy-box">
          <h4>🎄 Holiday Rate</h4>
          <p>+$7/hr added on NYE, New Year's Day, Thanksgiving, Christmas Eve, and Christmas Day.</p>
        </div>
        <div class="policy-box">
          <h4>👶 Child Limit</h4>
          <p>Maximum of 5 children per session, with up to 1 child under 12 months old.</p>
        </div>
        <div class="policy-box">
          <h4>💳 Payment Methods</h4>
          <p>Cash, Zelle, Apple Pay, or Cash App. Payment is made directly to the sitter after service.</p>
        </div>
        <div class="policy-box">
          <h4>💝 Tips</h4>
          <p>Families are welcome to add a tip or offer a higher hourly rate at their discretion — always appreciated!</p>
        </div>
        <div class="policy-box">
          <h4>🤝 Existing Families</h4>
          <p>For families I already sit for — your prices remain as we have already established together.</p>
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <h2 class="section-title pink">6+ children or special requests?</h2>
      <p style="font-size:16px;color:var(--text2);margin:1rem auto 2rem;max-width:500px;">Reach out directly and we'll work something out!</p>
      <div style="display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;">
        <a href="mailto:lay011318@gmail.com" class="btn-pink">Email me</a>
        <a href="tel:3302840675" class="btn-outline-pink">Call me</a>
      </div>
    </div>
  </div>
</div>

<!-- BOOKING PAGE -->
<div id="page-booking" class="page">
  <div class="hero" style="min-height:380px;background:linear-gradient(135deg,var(--pink) 0%,var(--pink-dark) 100%);">
    <div class="hero-content" style="padding:3rem 2rem;">
      <div class="hero-badge" style="background:#fff;color:var(--pink);">Easy booking</div>
      <h1 style="color:#fff;">Book your trusted <em style="color:#ffe0f3;">childcare</em></h1>
      <p style="color:rgba(255,255,255,0.9);">Ready to secure reliable and caring childcare? Check my availability and request your session in minutes.</p>
      <a href="https://layhachildcare.netlify.app/" class="btn-outline-pink" style="border-color:#fff;color:#fff;" target="_blank">Check availability</a>
    </div>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <h2 class="section-title pink">How to book with Layha?</h2>
      <p class="section-sub">Scheduling childcare with me is straightforward and designed for your convenience. Follow these simple steps to ensure your children receive the best care when you need it most.</p>
      <div class="steps">
        <div class="step">
          <div class="step-num">1</div>
          <h4>Check the calendar</h4>
          <p>Visit my booking page and tap any green day on the calendar to see available time slots.</p>
        </div>
        <div class="step">
          <div class="step-num">2</div>
          <h4>Pick your time</h4>
          <p>Tap an available time block and fill in your details — name, address, children's ages, and your preferred start and end time.</p>
        </div>
        <div class="step">
          <div class="step-num">3</div>
          <h4>Send your request</h4>
          <p>Submit your booking request. You'll see an estimated total right on the page before you submit.</p>
        </div>
        <div class="step">
          <div class="step-num">4</div>
          <h4>Get confirmed</h4>
          <p>I'll review your request and send you a confirmation email. That time is then yours!</p>
        </div>
      </div>
    </div>
  </div>

  <div class="section section-alt">
    <div class="section-inner text-center">
      <h2 class="section-title pink">New families</h2>
      <p class="section-sub">If this is your first time booking with me, I'd love to set up a quick phone call or in-person meeting first so we can connect before your first session. Just reach out!</p>
      <div style="display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;margin-top:1rem;">
        <a href="mailto:lay011318@gmail.com" class="btn-pink">Email me</a>
        <a href="tel:3302840675" class="btn-outline-pink">Call me</a>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-inner text-center">
      <div class="highlight-box">
        <h3>Ready to go? ? </h3>
        <p>Head to my booking page to view my real-time availability and submit your request.</p>
        <a href="https://layhachildcare.netlify.app/" class="btn-outline-pink" style="border-color:#fff;color:#fff;" target="_blank">Open booking page</a>
      </div>
    </div>
  </div>
</div>

<!-- FAMILIES PAGE -->
<div id="page-families" class="page">
  <div class="hero" style="min-height:320px;">
    <div class="hero-content" style="padding:3rem 2rem;">
      <div class="hero-badge">My families</div>
      <h1>The families I <em>serve</em></h1>
    </div>
  </div>

  <div class="section">
    <div class="section-inner">
      <div class="families-banner">
        <h2>A reminder 💗</h2>
        <p>This is a solo business, so the relationships I have with my families and their children mean a lot! I appreciate them for trusting me and inviting me into their homes to care for the ones they love most. I assure you that I am dedicated to keeping your children safe, comfortable, and well attended to during every service. I believe in creating lasting positive experiences, and nothing makes me happier than hearing how much my services mean to the families I serve.</p>
      </div>

      <div class="text-center" style="margin-bottom:2rem;">
        <h2 class="section-title pink">What parents are saying</h2>
        <p class="section-sub">Read what parents are saying about my patient, independent, and fun-loving approach to childcare.</p>
      </div>

      <div class="testimonials">
        <div class="testimonial">
          <p class="testimonial-text">We are so happy that you've been babysitting for us and feel like you do a wonderful job with the kids.</p>
          <div class="testimonial-author">— A Columbus family, since July 2025</div>
        </div>
        <div class="testimonial">
          <p class="testimonial-text">Layha is incredibly patient and the kids absolutely love her. We always feel comfortable leaving them in her care.</p>
          <div class="testimonial-author">— Columbus, Ohio family</div>
        </div>
        <div class="testimonial">
          <p class="testimonial-text">Booking is so easy and she always shows up on time. She's become such an important part of our routine!</p>
          <div class="testimonial-author">— Columbus, Ohio family</div>
        </div>
      </div>
    </div>
  </div>

  <div class="section section-alt">
    <div class="section-inner text-center">
      <h2 class="section-title pink">Want to become a Layha family?</h2>
      <p class="section-sub">I'd love to meet you and your children! New families are welcome to reach out for a quick call or in-person meeting before booking their first session.</p>
      <div style="display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;margin-top:1rem;">
        <a href="https://layhachildcare.netlify.app/" class="btn-pink" target="_blank">Book now</a>
        <a href="mailto:lay011318@gmail.com" class="btn-outline-pink">Say hello</a>
      </div>
    </div>
  </div>
</div>

<footer>
  <p>© 2026 <span>lillybug's childcare services</span> · Layha the Familysitter · Columbus, Ohio</p>
  <p style="margin-top:.5rem;"><a href="tel:3302840675" style="color:var(--pink);text-decoration:none;">(330) 284-0675</a> · <a href="mailto:lay011318@gmail.com" style="color:var(--pink);text-decoration:none;">lay011318@gmail.com</a></p>
</footer>

<script>
function showPage(id, clickedLink) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + id).classList.add('active');
  document.querySelectorAll('.nav-links a, .mobile-menu a').forEach(a => a.classList.remove('active'));
  if (clickedLink) {
    document.querySelectorAll('.nav-links a, .mobile-menu a').forEach(a => {
      if (a.textContent.trim() === clickedLink.textContent.trim()) a.classList.add('active');
    });
  }
  window.scrollTo({top: 0, behavior: 'smooth'});
}
function toggleMenu() {
  document.getElementById('mobileMenu').classList.toggle('open');
}
</script>
</body>
</html>
