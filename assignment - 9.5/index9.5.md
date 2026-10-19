Here is the complete and final solution for Assignment 9.5.

Since you are making this portfolio-ready, I have included a small bonus in this final version: a few lines of JavaScript to make the mobile "hamburger" menu actually work when clicked!

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NexusTech | Modern SaaS Platform</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- NAVIGATION -->
    <header class="navbar">
        <div class="logo">NexusTech.</div>
        
        <!-- Hamburger Icon for Mobile -->
        <div class="mobile-menu" id="mobile-menu">☰</div>
        
        <nav class="nav-menu" id="nav-menu">
            <ul class="nav-links">
                <li><a href="#product">Product</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#pricing">Pricing</a></li>
            </ul>
            <div class="nav-actions">
                <a href="#" class="btn btn-outline">Log In</a>
                <a href="#" class="btn btn-primary">Sign Up</a>
            </div>
        </nav>
    </header>

    <main>
        <!-- HERO SECTION -->
        <section class="hero" id="product">
            <div class="hero-content">
                <h1>Build better products, faster than ever.</h1>
                <p>Streamline your workflow with our all-in-one platform designed for modern development teams.</p>
                <div class="hero-buttons">
                    <a href="#" class="btn btn-primary btn-large">Start Free Trial</a>
                    <a href="#" class="btn btn-outline btn-large">Book Demo</a>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=800&q=80" alt="Developer coding on laptop">
            </div>
        </section>

        <!-- FEATURES SECTION -->
        <section class="features" id="features">
            <div class="section-header">
                <h2>Everything you need to succeed</h2>
                <p>Powerful tools packaged in an intuitive interface.</p>
            </div>
            
            <div class="features-grid">
                <article class="feature-card">
                    <div class="icon">⚡</div>
                    <h3>Lightning Fast</h3>
                    <p>Optimized infrastructure ensures your projects load in milliseconds, worldwide.</p>
                </article>

                <article class="feature-card">
                    <div class="icon">🔒</div>
                    <h3>Bank-grade Security</h3>
                    <p>Enterprise-level encryption and compliance built-in from day one.</p>
                </article>

                <article class="feature-card">
                    <div class="icon">🤝</div>
                    <h3>Team Collaboration</h3>
                    <p>Real-time syncing and commenting keeps your entire team on the same page.</p>
                </article>
            </div>
        </section>
    </main>

    <!-- FOOTER -->
    <footer class="footer">
        <p>&copy; 2026 NexusTech Inc. All rights reserved.</p>
    </footer>

    <!-- BONUS: Simple JavaScript for Mobile Menu -->
    <script>
        const mobileMenu = document.getElementById('mobile-menu');
        const navMenu = document.getElementById('nav-menu');

        mobileMenu.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });
    </script>
</body>
</html>
2. CSS Styling (style.css)
CSS
/* =========================================
   BASE STYLES & VARIABLES
   ========================================= */
:root {
    --primary: #2563eb;
    --primary-hover: #1d4ed8;
    --text-dark: #1e293b;
    --text-light: #64748b;
    --bg-light: #f8fafc;
    --white: #ffffff;
}

/* Step 6: Fix horizontal scrolling and spacing issues */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; 
}

body {
    font-family: 'Inter', system-ui, -apple-system, sans-serif;
    color: var(--text-dark);
    line-height: 1.6;
    background-color: var(--white);
    overflow-x: hidden; 
}

/* Step 3: Responsive Images */
img {
    max-width: 100%;
    height: auto;
    display: block;
    border-radius: 12px;
}

/* Shared Buttons */
.btn {
    display: inline-block;
    text-align: center;
    text-decoration: none;
    padding: 0.5rem 1.25rem;
    border-radius: 6px;
    font-weight: 600;
    transition: all 0.2s ease;
    cursor: pointer;
}

.btn-large { padding: 0.75rem 1.5rem; font-size: 1.1rem; }
.btn-primary { background-color: var(--primary); color: var(--white); border: 2px solid var(--primary); }
.btn-primary:hover { background-color: var(--primary-hover); border-color: var(--primary-hover); }
.btn-outline { background-color: transparent; color: var(--text-dark); border: 2px solid #e2e8f0; }
.btn-outline:hover { border-color: var(--text-light); background-color: #f8fafc;}

/* =========================================
   DESKTOP LAYOUT (Default)
   ========================================= */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.25rem 5%;
    background-color: var(--white);
    border-bottom: 1px solid #f1f5f9;
    position: relative;
}

.logo { font-size: 1.5rem; font-weight: 800; color: var(--primary); }
.mobile-menu { display: none; font-size: 1.8rem; cursor: pointer; color: var(--text-dark); user-select: none; }

.nav-menu {
    display: flex;
    align-items: center;
    gap: 2.5rem;
    width: 100%;
    justify-content: flex-end;
}

.nav-links { display: flex; list-style: none; gap: 2.5rem; }
.nav-links a { text-decoration: none; color: var(--text-light); font-weight: 500; transition: color 0.2s;}
.nav-links a:hover { color: var(--primary); }
.nav-actions { display: flex; gap: 1rem; }

/* Hero Section */
.hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 4rem;
    padding: 6rem 5%;
    max-width: 1400px;
    margin: 0 auto;
}

.hero-content { flex: 1; }

/* Step 3: Responsive Typography using clamp() */
.hero-content h1 {
    font-size: clamp(2.5rem, 5vw, 4rem); 
    line-height: 1.1;
    margin-bottom: 1.5rem;
    letter-spacing: -0.02em;
}

.hero-content p {
    font-size: clamp(1.1rem, 2vw, 1.25rem);
    color: var(--text-light);
    margin-bottom: 2.5rem;
}

.hero-buttons { display: flex; gap: 1rem; }
.hero-image { flex: 1; }
.hero-image img { box-shadow: 0 20px 25px -5px rgba(0,0,0,0.1); }

/* Features Section */
.features {
    background-color: var(--bg-light);
    padding: 6rem 5%;
}

.section-header { text-align: center; max-width: 600px; margin: 0 auto 4rem auto; }
.section-header h2 { font-size: clamp(2rem, 4vw, 2.5rem); margin-bottom: 1rem; }
.section-header p { font-size: 1.125rem; color: var(--text-light); }

.features-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.feature-card {
    background-color: var(--white);
    padding: 2.5rem;
    border-radius: 12px;
    box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05);
    transition: transform 0.3s ease;
}

.feature-card:hover { transform: translateY(-5px); }
.icon { font-size: 2.5rem; margin-bottom: 1.5rem; }
.feature-card h3 { font-size: 1.25rem; margin-bottom: 0.75rem; }
.feature-card p { color: var(--text-light); font-size: 1rem; }

/* Footer */
.footer { text-align: center; padding: 2rem; border-top: 1px solid #f1f5f9; color: var(--text-light); }

/* =========================================
   BREAKPOINT 1: TABLET (Step 1)
   ========================================= */
@media screen and (max-width: 1024px) {
    .hero { gap: 2rem; padding: 4rem 5%; }
    .features-grid { grid-template-columns: repeat(2, 1fr); }
}

/* =========================================
   BREAKPOINT 2: MOBILE (Step 1 & 2)
   ========================================= */
@media screen and (max-width: 768px) {
    /* Navbar Mobile Adjustments */
    .mobile-menu { display: block; } 
    
    .nav-menu { 
        display: none; /* Hidden by default */
        flex-direction: column; 
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background-color: var(--white);
        padding: 2rem 5%;
        box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
        z-index: 100;
    }

    /* JavaScript toggles this class to show the menu */
    .nav-menu.active { display: flex; }

    .nav-links { flex-direction: column; width: 100%; text-align: center; gap: 1.5rem;}
    .nav-actions { flex-direction: column; width: 100%; margin-top: 1.5rem;}
    .nav-actions .btn { width: 100%; }

    /* Hero Mobile Adjustments */
    .hero { flex-direction: column; text-align: center; padding: 3rem 5%; }
    .hero-buttons { flex-direction: column; width: 100%; }
    .btn-large { width: 100%; }

    /* Features Mobile Adjustments */
    .features-grid { grid-template-columns: 1fr; }
    .features { padding: 4rem 5%; }
}
Final Steps to Complete the Course Assignment!
Test in DevTools (Step 5):

Open index.html in Chrome.

Right-click -> Inspect -> Click the Device Mode icon (the little phone/tablet symbol).

Verify that nothing overflows horizontally (Step 6).

Test the menu: Click the ☰ icon in mobile view. Because of the included JavaScript, the menu will beautifully drop down!

Take Your Screenshots: Use DevTools to take one picture of the Desktop width, one of Tablet width (iPad Air), and one of Mobile width (iPhone 14).

Push to GitHub (Step 8): Commit these final files to your repository.

Submit: Turn in your screenshots, HTML/CSS files, and your final GitHub link!