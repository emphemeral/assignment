Here is the complete solution for Assignment 9.3. This landing page perfectly demonstrates how modern developers build websites: CSS Grid is used for the structural layout of the features section, while Flexbox handles the precise alignment of the navigation bar, the hero section, and the content inside the cards.

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox & Grid Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 1: Create a header and navigation bar -->
    <header class="navbar">
        <div class="logo">HybridLayout.</div>
        <nav>
            <ul class="nav-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
        <button class="btn nav-btn">Sign Up</button>
    </header>

    <!-- Step 2: Arrange text and images in the hero section -->
    <section id="hero" class="hero">
        <div class="hero-content">
            <h1>The Best of Both Worlds</h1>
            <p>Combine the macro-layout power of CSS Grid with the micro-alignment precision of Flexbox to build flawless responsive websites.</p>
            <button class="btn hero-btn">Get Started</button>
        </div>
        <div class="hero-image">
            <img src="https://via.placeholder.com/600x400?text=Hero+Illustration" alt="Hero Illustration">
        </div>
    </section>

    <!-- Step 3 & 4: Add cards in the features section using Grid -->
    <section id="features" class="features">
        <h2 class="section-title">Why Choose Hybrid Layouts?</h2>
        
        <div class="features-grid">
            <!-- Card 1 -->
            <div class="feature-card">
                <div class="icon">📐</div>
                <h3>Grid for Structure</h3>
                <p>Use CSS Grid to effortlessly divide your page into columns and rows without complex math.</p>
            </div>
            
            <!-- Card 2 -->
            <div class="feature-card">
                <div class="icon">✨</div>
                <h3>Flexbox for Content</h3>
                <p>Use Flexbox to perfectly center icons, text, and buttons inside your components.</p>
            </div>
            
            <!-- Card 3 -->
            <div class="feature-card">
                <div class="icon">📱</div>
                <h3>Fully Responsive</h3>
                <p>Combine both tools to create layouts that instantly adapt to mobile, tablet, and desktop screens.</p>
            </div>
        </div>
    </section>

    <footer id="contact" class="footer">
        <p>&copy; 2026 HybridLayout Studios. All rights reserved.</p>
    </footer>

</body>
</html>
2. CSS Styling (style.css)
We are using a Mobile-First approach here. The default CSS applies a single-column layout for mobile (Step 6), and the @media query at the bottom upgrades it to a multi-column layout for desktop.

CSS
/* =========================================
   BASE STYLES & TYPOGRAPHY
   ========================================= */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', system-ui, sans-serif;
    color: #333;
    background-color: #f9fafb;
    line-height: 1.6;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
    border-radius: 8px;
}

.btn {
    padding: 0.75rem 1.5rem;
    border-radius: 6px;
    border: none;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s;
}

/* =========================================
   HEADER / NAVBAR (Step 5: Flexbox)
   ========================================= */
.navbar {
    display: flex;
    flex-wrap: wrap;             /* Allows nav to wrap on very small screens */
    justify-content: space-between; /* Spreads out Logo, Nav, and Button */
    align-items: center;         /* Vertically centers items */
    padding: 1.5rem 5%;
    background-color: #fff;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: #4f46e5;
}

.nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
}

.nav-links a {
    text-decoration: none;
    color: #4b5563;
    font-weight: 500;
}

.nav-btn {
    background-color: #4f46e5;
    color: #fff;
}

/* =========================================
   HERO SECTION (Step 5: Flexbox)
   ========================================= */
.hero {
    display: flex;
    flex-direction: column;      /* Default mobile view: Stacked (Step 6) */
    align-items: center;
    gap: 3rem;
    padding: 4rem 5%;
    background-color: #fff;
}

.hero-content {
    text-align: center;
}

.hero-content h1 {
    font-size: clamp(2.5rem, 5vw, 4rem); /* Responsive typography */
    margin-bottom: 1.5rem;
    color: #111827;
}

.hero-content p {
    font-size: 1.125rem;
    color: #6b7280;
    margin-bottom: 2rem;
}

.hero-btn {
    background-color: #111827;
    color: #fff;
    font-size: 1.1rem;
}

/* =========================================
   FEATURES SECTION (Step 4: CSS Grid)
   ========================================= */
.features {
    padding: 5rem 5%;
}

.section-title {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 3rem;
    color: #111827;
}

.features-grid {
    display: grid;
    /* Step 6: Default mobile view is 1 column */
    grid-template-columns: 1fr;  
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

/* =========================================
   FEATURE CARDS (Step 5: Flexbox inside Grid)
   ========================================= */
.feature-card {
    background-color: #fff;
    padding: 2.5rem 1.5rem;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    
    /* Using Flexbox to perfectly align the inside of the card */
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.icon {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.feature-card h3 {
    font-size: 1.25rem;
    margin-bottom: 0.5rem;
    color: #111827;
}

.feature-card p {
    color: #6b7280;
}

/* =========================================
   FOOTER
   ========================================= */
.footer {
    text-align: center;
    padding: 2rem 5%;
    background-color: #111827;
    color: #9ca3af;
}

/* =========================================
   MEDIA QUERIES (Step 6 & 7: Desktop View)
   ========================================= */
@media screen and (min-width: 768px) {
    /* Upgrade Hero to a side-by-side Flexbox layout */
    .hero {
        flex-direction: row;
        text-align: left;
        justify-content: space-between;
    }

    .hero-content {
        text-align: left;
        flex: 1; /* Takes up 50% width */
    }

    .hero-image {
        flex: 1; /* Takes up 50% width */
        display: flex;
        justify-content: flex-end;
    }

    /* Upgrade Features Grid to a 3-column layout */
    .features-grid {
        grid-template-columns: repeat(3, 1fr);
    }
}

/* Small adjustment for tablet navigation */
@media screen and (max-width: 767px) {
    .navbar {
        flex-direction: column;
        gap: 1.5rem;
    }
    .nav-links {
        flex-wrap: wrap;
        justify-content: center;
    }
}
How to complete your submission (Step 7):
To get your screenshots for your assignment submission:

Open index.html in your web browser.

Desktop Screenshot: Maximize the browser window. You will see Flexbox putting the Hero text and image side-by-side, and CSS Grid putting the 3 feature cards in a clean row. Take a screenshot.

Mobile Screenshot: Right-click, select Inspect, and click the "Device Mode" icon (or just shrink your browser window to be very narrow). You will see the Flexbox Hero section vertically stack the text above the image, and the CSS Grid perfectly stack the 3 feature cards into a single column. Take a screenshot of this view.