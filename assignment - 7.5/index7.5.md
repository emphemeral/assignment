Here is the complete solution for Assignment 7.5. This mini-project acts as a culmination of your Flexbox skills, combining a Navbar, Hero section, Feature cards, CTA, and Footer into one cohesive, responsive landing page.

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox Mini-Project</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- NAVIGATION BAR -->
    <nav class="navbar">
        <div class="logo">FlexPro.</div>
        <ul class="nav-links">
            <li><a href="#hero">Home</a></li>
            <li><a href="#features">Features</a></li>
            <li><a href="#cta">Pricing</a></li>
        </ul>
        <a href="#cta" class="btn nav-btn">Sign In</a>
    </nav>

    <!-- HERO SECTION -->
    <header id="hero" class="hero-section">
        <div class="hero-text">
            <h1>Master Flexbox Like a Pro</h1>
            <p>Build beautiful, responsive web layouts faster than ever. Say goodbye to float hacks and hello to clean, modern CSS alignments.</p>
            <a href="#features" class="btn primary-btn">Explore Features</a>
        </div>
        <div class="hero-image">
            <img src="https://via.placeholder.com/600x400?text=Hero+Illustration" alt="Hero Illustration">
        </div>
    </header>

    <!-- FEATURE CARDS SECTION -->
    <section id="features" class="features-section">
        <h2 class="section-title">Why Choose FlexPro?</h2>
        <div class="features-container">
            <!-- Feature Card 1 -->
            <div class="feature-card">
                <div class="icon">📱</div>
                <h3>Fully Responsive</h3>
                <p>Layouts that automatically adapt to mobile, tablet, and desktop screens without media query headaches.</p>
            </div>
            <!-- Feature Card 2 -->
            <div class="feature-card">
                <div class="icon">⚡</div>
                <h3>Lightning Fast</h3>
                <p>Clean code architecture ensures your pages load instantly and perform smoothly on all devices.</p>
            </div>
            <!-- Feature Card 3 -->
            <div class="feature-card">
                <div class="icon">🎨</div>
                <h3>Customizable</h3>
                <p>Easily tweak padding, margins, colors, and alignments to fit your unique brand identity perfectly.</p>
            </div>
        </div>
    </section>

    <!-- CALL-TO-ACTION (CTA) SECTION -->
    <section id="cta" class="cta-section">
        <div class="cta-content">
            <h2>Ready to build amazing layouts?</h2>
            <p>Join over 10,000 developers who are creating stunning websites with our tools today.</p>
            <a href="#" class="btn cta-btn">Get Started for Free</a>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
        <div class="footer-logo">FlexPro.</div>
        <p>&copy; 2026 FlexPro Inc. All rights reserved.</p>
        <ul class="footer-links">
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Terms of Service</a></li>
        </ul>
    </footer>

</body>
</html>
2. CSS Styling (style.css)
CSS
/* =========================================
   GLOBAL STYLES & VARIABLES
   ========================================= */
:root {
    --primary-color: #4f46e5;
    --primary-hover: #4338ca;
    --dark-bg: #1f2937;
    --light-bg: #f9fafb;
    --text-main: #111827;
    --text-muted: #4b5563;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Inter', system-ui, sans-serif;
}

body {
    color: var(--text-main);
    line-height: 1.6;
    overflow-x: hidden; /* Prevents horizontal scrolling */
}

a {
    text-decoration: none;
}

ul {
    list-style: none;
}

/* Base Button Styles */
.btn {
    padding: 0.75rem 1.5rem;
    border-radius: 6px;
    font-weight: 600;
    transition: all 0.3s ease;
    display: inline-block;
    cursor: pointer;
}

.primary-btn {
    background-color: var(--primary-color);
    color: white;
}

.primary-btn:hover {
    background-color: var(--primary-hover);
}

/* =========================================
   NAVIGATION BAR
   ========================================= */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 5%;
    background-color: white;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 1.5rem;
    font-weight: 800;
    color: var(--primary-color);
}

.nav-links {
    display: flex;
    gap: 2rem;
}

.nav-links a {
    color: var(--text-main);
    font-weight: 500;
}

.nav-links a:hover {
    color: var(--primary-color);
}

.nav-btn {
    background-color: var(--light-bg);
    color: var(--text-main);
    border: 1px solid #e5e7eb;
}

.nav-btn:hover {
    background-color: #e5e7eb;
}

/* =========================================
   HERO SECTION
   ========================================= */
.hero-section {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 4rem;
    padding: 6rem 5%;
    background-color: var(--light-bg);
}

.hero-text {
    flex: 1;
}

.hero-text h1 {
    font-size: 3.5rem;
    line-height: 1.2;
    margin-bottom: 1.5rem;
}

.hero-text p {
    font-size: 1.125rem;
    color: var(--text-muted);
    margin-bottom: 2rem;
}

.hero-image {
    flex: 1;
    display: flex;
    justify-content: flex-end;
}

.hero-image img {
    max-width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 20px 25px -5px rgba(0,0,0,0.1);
}

/* =========================================
   FEATURES SECTION
   ========================================= */
.features-section {
    padding: 5rem 5%;
    background-color: white;
}

.section-title {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 3rem;
}

.features-container {
    display: flex;
    flex-wrap: wrap;       /* Rule 3: Use flex-wrap */
    gap: 2rem;             /* Rule 3: Use gap */
    justify-content: center; /* Rule 3: Use justify-content */
}

.feature-card {
    flex: 1 1 300px;       /* Rule 2: Arranged in responsive row */
    display: flex;
    flex-direction: column;
    align-items: center;   /* Rule 3: Use align-items */
    text-align: center;
    padding: 2.5rem 1.5rem;
    background-color: var(--light-bg);
    border-radius: 12px;
    transition: transform 0.3s ease;
}

.feature-card:hover {
    transform: translateY(-10px);
}

.icon {
    font-size: 3rem;
    margin-bottom: 1.5rem;
}

.feature-card h3 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
}

.feature-card p {
    color: var(--text-muted);
}

/* =========================================
   CALL TO ACTION (CTA) SECTION
   ========================================= */
.cta-section {
    background-color: var(--primary-color);
    color: white;
    padding: 5rem 5%;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.cta-content h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.cta-content p {
    font-size: 1.125rem;
    margin-bottom: 2rem;
    opacity: 0.9;
}

.cta-btn {
    background-color: white;
    color: var(--primary-color);
    font-size: 1.1rem;
    padding: 1rem 2rem;
}

.cta-btn:hover {
    background-color: #f3f4f6;
}

/* =========================================
   FOOTER
   ========================================= */
.footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1.5rem;
    padding: 2rem 5%;
    background-color: var(--dark-bg);
    color: #9ca3af;
}

.footer-logo {
    color: white;
    font-size: 1.25rem;
    font-weight: 700;
}

.footer-links {
    display: flex;
    gap: 1.5rem;
}

.footer-links a {
    color: #9ca3af;
}

.footer-links a:hover {
    color: white;
}

/* =========================================
   RESPONSIVE MEDIA QUERIES (Rule 5: No overflow)
   ========================================= */
@media screen and (max-width: 900px) {
    .hero-section {
        flex-direction: column;
        text-align: center;
        padding-top: 4rem;
    }

    .hero-image {
        justify-content: center;
    }
}

@media screen and (max-width: 768px) {
    .navbar {
        flex-direction: column;
        gap: 1.5rem;
    }

    .nav-links {
        flex-wrap: wrap;
        justify-content: center;
    }

    .hero-text h1 {
        font-size: 2.5rem;
    }
    
    .footer {
        flex-direction: column;
        text-align: center;
        justify-content: center;
    }
}
Final Submission Instructions:
To complete the final step of your assignment ("Submission: Complete landing page, HTML/CSS files, and a GitHub repository link"):

Save the HTML code above into an index.html file.

Save the CSS code into a style.css file.

Open your terminal or GitHub Desktop, commit both files, and push them to a new public repository on your GitHub account.

Submit the URL of that GitHub repository to your instructor!