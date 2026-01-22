<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Delta Wealth Management</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

```
    :root {
        --navy: #1a3a52;
        --light-navy: #2c5f7f;
        --light-bg: #f8f9fa;
        --white: #ffffff;
        --text: #2c3e50;
        --text-light: #6c757d;
    }

    body {
        font-family: 'Montserrat', sans-serif;
        line-height: 1.8;
        color: var(--text);
        overflow-x: hidden;
    }

    /* Header */
    header {
        background: var(--white);
        padding: 1.5rem 0;
        position: fixed;
        width: 100%;
        top: 0;
        z-index: 1000;
        border-bottom: 1px solid #e9ecef;
    }

    nav {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 4rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        height: 45px;
        width: auto;
    }

    .nav-links {
        display: flex;
        gap: 3rem;
        list-style: none;
        align-items: center;
    }

    .nav-links a {
        text-decoration: none;
        color: var(--text);
        font-weight: 400;
        font-size: 0.95rem;
        letter-spacing: 0.5px;
        transition: color 0.3s;
    }

    .nav-links a:hover {
        color: var(--navy);
    }

    .contact-btn {
        background: var(--navy);
        color: var(--white);
        padding: 0.75rem 2rem;
        text-decoration: none;
        font-weight: 500;
        letter-spacing: 1px;
        font-size: 0.9rem;
        transition: opacity 0.3s;
    }

    .contact-btn:hover {
        opacity: 0.85;
    }

    /* Hero */
    .hero {
        margin-top: 85px;
        min-height: 75vh;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        background: linear-gradient(135deg, rgba(26, 58, 82, 0.95) 0%, rgba(44, 95, 127, 0.9) 100%), 
                    url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800"><rect fill="%23f8f9fa" width="1200" height="800"/><path d="M0 400 Q300 300 600 400 T1200 400" stroke="%23e9ecef" stroke-width="2" fill="none"/><path d="M0 500 Q300 400 600 500 T1200 500" stroke="%23e9ecef" stroke-width="2" fill="none"/></svg>');
        background-size: cover;
        background-position: center;
        padding: 8rem 2rem;
        position: relative;
    }

    .hero-content {
        max-width: 900px;
        position: relative;
        z-index: 1;
    }

    .hero h1 {
        font-size: 3.5rem;
        font-weight: 300;
        color: var(--white);
        line-height: 1.3;
        margin-bottom: 1.5rem;
        letter-spacing: -1px;
    }

    .hero p {
        font-size: 1.3rem;
        color: rgba(255, 255, 255, 0.95);
        font-weight: 300;
        line-height: 1.8;
        max-width: 750px;
        margin: 0 auto 3rem;
    }

    .hero-badges {
        display: flex;
        justify-content: center;
        gap: 3rem;
        flex-wrap: wrap;
        margin-top: 3rem;
    }

    .badge {
        color: rgba(255, 255, 255, 0.9);
        font-size: 0.95rem;
        font-weight: 400;
        letter-spacing: 0.5px;
    }

    .hero-btn {
        background: var(--white);
        color: var(--navy);
        padding: 1.1rem 3rem;
        text-decoration: none;
        font-weight: 500;
        letter-spacing: 1px;
        font-size: 1rem;
        display: inline-block;
        transition: all 0.3s;
    }

    .hero-btn:hover {
        transform: translateY(-2px);
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    }

    /* Sections */
    section {
        padding: 7rem 4rem;
        max-width: 1400px;
        margin: 0 auto;
    }

    .section-title {
        font-size: 2.5rem;
        font-weight: 300;
        color: var(--navy);
        margin-bottom: 1rem;
        letter-spacing: -0.5px;
        text-align: center;
    }

    .section-subtitle {
        font-size: 1.2rem;
        color: var(--text-light);
        font-weight: 300;
        line-height: 1.9;
        max-width: 800px;
        margin: 0 auto 4rem;
        text-align: center;
    }

    /* Who We Work With */
    .clients-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 3rem;
        margin-top: 4rem;
    }

    .client-card {
        text-align: center;
        padding: 3rem 2rem;
        background: var(--white);
        border: 1px solid #e9ecef;
        transition: all 0.3s;
    }

    .client-card:hover {
        border-color: var(--navy);
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
    }

    .client-icon {
        font-size: 3rem;
        margin-bottom: 1.5rem;
    }

    .client-card h3 {
        font-size: 1.4rem;
        font-weight: 500;
        color: var(--navy);
        margin-bottom: 1rem;
    }

    .client-card p {
        font-size: 1rem;
        color: var(--text-light);
        font-weight: 300;
        line-height: 1.8;
    }

    /* Process Section */
    .process-section {
        background: var(--light-bg);
    }

    .process-steps {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        gap: 3rem;
        margin-top: 4rem;
    }

    .step {
        background: var(--white);
        padding: 3rem;
        border-left: 3px solid var(--navy);
        position: relative;
    }

    .step-number {
        position: absolute;
        top: -15px;
        left: 20px;
        background: var(--navy);
        color: var(--white);
        width: 50px;
        height: 50px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: 600;
        font-size: 1.3rem;
    }

    .step h3 {
        font-size: 1.4rem;
        font-weight: 500;
        color: var(--navy);
        margin: 2rem 0 1rem;
    }

    .step p {
        font-size: 1rem;
        color: var(--text-light);
        font-weight: 300;
        line-height: 1.8;
    }

    /* Services */
    .services-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 4rem;
        margin-top: 4rem;
    }

    .service-item {
        padding: 2.5rem 0;
        border-top: 1px solid #e9ecef;
    }

    .service-item h3 {
        font-size: 1.4rem;
        font-weight: 500;
        color: var(--navy);
        margin-bottom: 1rem;
    }

    .service-item p {
        font-size: 1rem;
        color: var(--text-light);
        font-weight: 300;
        line-height: 1.8;
    }

    /* About Section */
    .about {
        background: var(--white);
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 5rem;
        align-items: center;
    }

    .about-image {
        width: 100%;
        height: 500px;
        background: #d9e2ec;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text-light);
        font-size: 1rem;
        font-weight: 300;
    }

    .credentials {
        font-size: 1.1rem;
        color: var(--light-navy);
        font-weight: 500;
        margin-bottom: 1.5rem;
        letter-spacing: 0.5px;
    }

    .about-text {
        font-size: 1rem;
        color: var(--text-light);
        font-weight: 300;
        line-height: 1.9;
        margin-bottom: 1.5rem;
    }

    /* FAQ Section */
    .faq-section {
        background: var(--light-bg);
    }

    .faq-grid {
        display: grid;
        gap: 1.5rem;
        margin-top: 3rem;
        max-width: 900px;
        margin-left: auto;
        margin-right: auto;
    }

    .faq-item {
        background: var(--white);
        padding: 2rem;
        cursor: pointer;
        transition: all 0.3s;
        border-left: 3px solid transparent;
    }

    .faq-item:hover {
        border-left-color: var(--navy);
    }

    .faq-question {
        font-size: 1.1rem;
        font-weight: 500;
        color: var(--navy);
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .faq-answer {
        margin-top: 1rem;
        font-size: 1rem;
        color: var(--text-light);
        font-weight: 300;
        line-height: 1.8;
        display: none;
    }

    .faq-item.active .faq-answer {
        display: block;
    }

    /* CTA Section */
    .cta-section {
        background: var(--navy);
        color: var(--white);
        text-align: center;
        padding: 7rem 4rem;
    }

    .cta-section h2 {
        font-size: 3rem;
        font-weight: 300;
        margin-bottom: 1.5rem;
        letter-spacing: -0.5px;
        color: var(--white);
    }

    .cta-section p {
        font-size: 1.2rem;
        font-weight: 300;
        margin-bottom: 3rem;
        max-width: 700px;
        margin-left: auto;
        margin-right: auto;
        opacity: 0.95;
    }

    .cta-btn {
        background: var(--white);
        color: var(--navy);
        padding: 1.1rem 3rem;
        text-decoration: none;
        font-weight: 500;
        letter-spacing: 1px;
        font-size: 1rem;
        display: inline-block;
        transition: all 0.3s;
    }

    .cta-btn:hover {
        transform: translateY(-2px);
        box-shadow: 0 10px 30px rgba(255, 255, 255, 0.2);
    }

    /* Footer */
    footer {
        background: var(--white);
        padding: 4rem;
        border-top: 1px solid #e9ecef;
    }

    .footer-content {
        max-width: 1400px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: 2fr 1fr 1fr;
        gap: 4rem;
    }

    .footer-section h3 {
        font-size: 1rem;
        font-weight: 600;
        color: var(--navy);
        margin-bottom: 1.5rem;
        letter-spacing: 1px;
        text-transform: uppercase;
    }

    .footer-section p,
    .footer-section a {
        color: var(--text-light);
        text-decoration: none;
        display: block;
        margin-bottom: 0.75rem;
        font-size: 0.95rem;
        font-weight: 300;
    }

    .footer-section a:hover {
        color: var(--navy);
    }

    .footer-bottom {
        max-width: 1400px;
        margin: 3rem auto 0;
        padding-top: 3rem;
        border-top: 1px solid #e9ecef;
        color: var(--text-light);
        font-size: 0.85rem;
        font-weight: 300;
        line-height: 1.6;
    }

    /* Responsive */
    @media (max-width: 1024px) {
        nav, section, .footer-content {
            padding-left: 2rem;
            padding-right: 2rem;
        }

        .hero h1 {
            font-size: 2.5rem;
        }

        .about {
            grid-template-columns: 1fr;
        }

        .services-grid {
            grid-template-columns: 1fr;
        }

        .footer-content {
            grid-template-columns: 1fr;
        }

        .nav-links {
            display: none;
        }
    }

    @media (max-width: 768px) {
        section {
            padding: 4rem 2rem;
        }

        .clients-grid, .process-steps {
            grid-template-columns: 1fr;
        }
    }
</style>
```

</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <svg class="logo" viewBox="0 0 640 200" xmlns="http://www.w3.org/2000/svg">
                <defs>
                    <linearGradient id="deltaGrad" x1="0%" y1="0%" x2="0%" y2="100%">
                        <stop offset="0%" style="stop-color:#1a3a52;stop-opacity:1" />
                        <stop offset="100%" style="stop-color:#2c5f7f;stop-opacity:1" />
                    </linearGradient>
                </defs>
                <path d="M105 25 L35 155 C29 166 38 173 51 168 L135 125 C150 118 145 103 133 90 L105 25 Z" fill="url(#deltaGrad)"/>
                <path d="M103 60 L70 125 L115 108 C121 106 120 99 114 95 Z" fill="#FFFFFF"/>
                <text x="180" y="95" font-family="Montserrat, sans-serif" font-size="52" font-weight="600" letter-spacing="2.5" fill="#1a3a52">DELTA</text>
                <text x="180" y="140" font-family="Montserrat, sans-serif" font-size="32" font-weight="500" letter-spacing="4.5" fill="#1a3a52">WEALTH</text>
            </svg>
            <ul class="nav-links">
                <li><a href="#who-we-serve">Who We Serve</a></li>
                <li><a href="#process">Process</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="mailto:info@deltawealthmgt.com" class="contact-btn">START YOUR JOURNEY</a></li>
            </ul>
        </nav>
    </header>

```
<!-- Hero -->
<section class="hero">
    <div class="hero-content">
        <h1>When Life Changes, Your Wealth Strategy Should Too</h1>
        <p>We guide high-earning professionals through major life transitions with tax-efficient planning and intelligent investment strategy.</p>
        <a href="mailto:info@deltawealthmgt.com" class="hero-btn">SCHEDULE A CONVERSATION</a>
        <div class="hero-badges">
            <div class="badge">Tax-Optimized Planning</div>
            <div class="badge">Alternative Investments</div>
            <div class="badge">Transition Expertise</div>
        </div>
    </div>
</section>

<!-- Who We Work With -->
<section id="who-we-serve">
    <h2 class="section-title">Who We Work With</h2>
    <p class="section-subtitle">We specialize in serving busy professionals in their 30s and 40s navigating pivotal life and career transitions.</p>
    
    <div class="clients-grid">
        <div class="client-card">
            <div class="client-icon">📈</div>
            <h3>The Rapid Riser</h3>
            <p>Recently promoted or joined a high-paying role with complex compensation (RSUs, bonuses, deferred comp). Ready for tax strategies and real planning.</p>
        </div>
        
        <div class="client-card">
            <div class="client-icon">👨‍👩‍👧‍👦</div>
            <h3>The Family Builder</h3>
            <p>High income, young kids, limited time. Needs help with organization, insurance, tax optimization, and college planning.</p>
        </div>
        
        <div class="client-card">
            <div class="client-icon">🎯</div>
            <h3>The New Steward</h3>
            <p>Recently inherited assets or family business. Feeling overwhelmed and wants help understanding what to keep, sell, or restructure.</p>
        </div>
        
        <div class="client-card">
            <div class="client-icon">💡</div>
            <h3>The Practical Investor</h3>
            <p>Analytical professional (engineer, healthcare, business operator) who is time-poor but wants vetted opportunities in alternatives.</p>
        </div>
    </div>
</section>

<!-- Process -->
<section id="process" class="process-section">
    <h2 class="section-title">Our Process</h2>
    <p class="section-subtitle">A structured 4-step approach to help you navigate transitions and build long-term momentum.</p>
    
    <div class="process-steps">
        <div class="step">
            <div class="step-number">1</div>
            <h3>Discovery Call</h3>
            <p>We start with an introductory conversation about where you are now and where you want to be. No sales pitch—just a genuine discussion about your goals and challenges.</p>
        </div>
        
        <div class="step">
            <div class="step-number">2</div>
            <h3>Deep Dive Analysis</h3>
            <p>We analyze your complete financial picture: income, taxes, investments, and opportunities. We identify what's working and where you can optimize.</p>
        </div>
        
        <div class="step">
            <div class="step-number">3</div>
            <h3>Strategic Recommendations</h3>
            <p>We present a personalized plan addressing your immediate transitions and long-term wealth goals. Clear recommendations in plain language, no jargon.</p>
        </div>
        
        <div class="step">
            <div class="step-number">4</div>
            <h3>Implementation & Support</h3>
            <p>We help execute the plan, coordinating with your other advisors and handling details so you can focus on what matters most to you.</p>
        </div>
    </div>
</section>

<!-- Services: Make, Protect, Teach -->
<section id="services">
    <h2 class="section-title">Make, Protect, Teach</h2>
    <p class="section-subtitle">Our fiduciary commitment as stewards of your wealth, built on three foundational principles.</p>
    
    <div class="services-grid">
        <div class="service-item">
            <h3>Make</h3>
            <p>We help you build wealth through intelligent investment strategies and access to opportunities beyond traditional markets. From tax-efficient planning to alternative investments in real estate and private businesses, we structure your capital to grow and compound over time.</p>
        </div>
        
        <div class="service-item">
            <h3>Protect</h3>
            <p>As your fiduciary, we act as stewards and protectors of what you've built. We safeguard your wealth through comprehensive risk management, tax optimization, and strategic guidance through life's transitions—ensuring your financial security for generations.</p>
        </div>
        
        <div class="service-item">
            <h3>Teach</h3>
            <p>We believe in empowering you with knowledge and clarity. Through ongoing education and transparent communication, we help you understand the "why" behind every strategy, ensuring you make informed decisions aligned with your values and goals.</p>
        </div>
    </div>
</section>

<!-- About -->
<section id="about" class="about">
    <div class="about-image">
        [Professional Photo]
    </div>
    <div>
        <h2 class="section-title" style="text-align: left;">Meet Your Advisor</h2>
        <p class="credentials">James Ouderkirk, CFA, CAIA</p>
        <p class="about-text">Life in your 30s and 40s moves fast. Promotions happen. Income jumps. Equity vests. Kids arrive. Inheritances surface. And suddenly, financial decisions that once felt simple become layered with complexity—and opportunity.</p>
        <p class="about-text">Delta Wealth was built for exactly these moments. I work with professionals who are smart and capable, but who don't have the time or desire to manage increasing financial complexity alone.</p>
        <p class="about-text">As a CFA and CAIA charterholder, I bring tax-efficient strategies, structured thinking, and access to opportunities outside traditional public markets. At Delta Wealth, change isn't a disruption. It's fuel.</p>
    </div>
</section>

<!-- FAQ -->
<section class="faq-section">
    <h2 class="section-title">Common Questions</h2>
    
    <div class="faq-grid">
        <div class="faq-item" onclick="this.classList.toggle('active')">
            <div class="faq-question">
                Who is Delta Wealth designed for?
                <span>+</span>
            </div>
            <div class="faq-answer">
                We work with high-earning professionals in their 30s and 40s navigating major life transitions—promotions, new jobs, equity compensation, inheritance, marriage, or starting families. Our ideal clients value expert guidance but don't have time to manage financial complexity alone.
            </div>
        </div>
        
        <div class="faq-item" onclick="this.classList.toggle('active')">
            <div class="faq-question">
                How are you different from other advisors?
                <span>+</span>
            </div>
            <div class="faq-answer">
                We specialize in life transitions and tax-efficient planning for busy professionals. We provide access to alternative investments like real estate and private businesses, not just traditional portfolios. Our approach is structured, clear, and designed for people whose lives—and wealth—are evolving rapidly.
            </div>
        </div>
        
        <div class="faq-item" onclick="this.classList.toggle('active')">
            <div class="faq-question">
                What does the engagement process look like?
                <span>+</span>
            </div>
            <div class="faq-answer">
                We start with a no-pressure discovery call to understand your situation and goals. If it's a good fit, we conduct a comprehensive analysis and present tailored recommendations. From there, we implement the strategy together and provide ongoing support as your life evolves.
            </div>
        </div>
        
        <div class="faq-item" onclick="this.classList.toggle('active')">
            <div class="faq-question">
                How do you charge for your services?
                <span>+</span>
            </div>
            <div class="faq-answer">
                Our fee structure is transparent and aligned with your success. We'll discuss pricing during our initial conversation to ensure it makes sense for your situation. Our focus is on providing value that far exceeds the cost of working together.
            </div>
        </div>
    </div>
</section>

<!-- CTA -->
<section class="cta-section">
    <h2>Ready to Turn Transition Into Momentum?</h2>
    <p>Let's have a conversation about where you are and where you want to be. No pressure, no sales pitch—just a genuine discussion about your goals.</p>
    <a href="mailto:info@deltawealthmgt.com" class="cta-btn">SCHEDULE YOUR CALL</a>
</section>

<!-- Footer -->
<footer>
    <div class="footer-content">
        <div class="footer-section">
            <h3>Delta Wealth Management</h3>
            <p>Guiding high-earning professionals through major life transitions with tax-efficient planning and intelligent investment strategy.</p>
        </div>
        
        <div class="footer-section">
            <h3>Quick Links</h3>
            <a href="#who-we-serve">Who We Serve</a>
            <a href="#process">Process</a>
            <a href="#services">Services</a>
            <a href="#about">About</a>
        </div>
        
        <div class="footer-section">
            <h3>Contact</h3>
            <a href="mailto:info@deltawealthmgt.com">info@deltawealthmgt.com</a>
            <p style="margin-top: 1.5rem;">James Ouderkirk, CFA, CAIA<br>Principal Advisor</p>
        </div>
    </div>
    
    <div class="footer-bottom">
        <p>© 2025 Delta Wealth Management. All rights reserved.</p>
        <p style="margin-top: 1rem;">Delta Wealth Management is a registered investment adviser. Advisory services are only offered to clients or prospective clients where Delta Wealth Management and its representatives are properly licensed or exempt from licensure. This website is solely for informational purposes. Past performance is no guarantee of future returns. Investing involves risk and possible loss of principal capital.</p>
    </div>
</footer>

<script>
    // Smooth scrolling
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({ behavior: 'smooth', block: 'start' });
            }
        });
    });
</script>
```

</body>
</html>
