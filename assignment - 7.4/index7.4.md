Here is the complete code for Assignment 7.4. It includes the HTML structure and CSS styling to build a modern landing page with a responsive header, a side-by-side hero section using Flexbox, and a styled footer.

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 1: Add a logo, navigation links, and a CTA button in the header -->
    <header class="header">
        <div class="logo">FlexLanding.</div>
        <nav>
            <ul class="nav-links">
                <li><a href="#">Features</a></li>
                <li><a href="#">Testimonials</a></li>
                <li><a href="#">Pricing</a></li>
            </ul>
        </nav>
        <a href="#" class="btn cta-btn">Get Started</a>
    </header>

    <!-- Step 2 & 3: Hero section with text content and an illustration/image -->
    <section class="hero">
        <div class="hero-content">
            <!-- Text Content -->
            <div class="hero-text">
                <h1>Build modern layouts faster than ever.</h1>
                <p>Master Flexbox and create stunning, responsive websites with ease. Join thousands of developers who are streamlining their workflow today.</p>
                <a href="#" class="btn hero-btn">Start Your Free Trial</a>
            </div>
            
            <!-- Illustration / Image -->
            <div class="hero-image">
                <img src="https://via.placeholder.com/500x350?text=Modern+Illustration" alt="Modern Layout Illustration">
            </div>
        </div>
    </section>

    <!-- Step 6: Style the footer or sticky section using earlier CSS concepts -->
    <footer class="footer">
        <p>&copy; 2026 FlexLanding. All rights reserved.</p>
        <div class="footer-links">
            <a href="#">Privacy Policy</a>
            <a href="#">Terms of Service</a>
        </div>
    </footer>

</body>
</html>
2. CSS Styling (style.css)
CSS
/* Basic Reset & Typography */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #fcfcfc;
    color: #333;
    display: flex;
    flex-direction: column;
    min-height: 100vh; /* Ensures footer stays at bottom if content is short */
}

/* =========================================
   HEADER (Step 1)
   ========================================= */
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 5%;
    background-color: #ffffff;
    box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    position: sticky; /* Step 6: Sticky section concept */
    top: 0;
    z-index: 100;
}

.logo {
    font-size: 1.8rem;
    font-weight: 800;
    color: #6c5ce7;
    cursor: pointer;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-links a {
    text-decoration: none;
    color: #555;
    font-weight: 500;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: #6c5ce7;
}

/* Shared Button Styles */
.btn {
    text-decoration: none;
    padding: 0.8rem 1.5rem;
    border-radius: 6px;
    font-weight: bold;
    transition: all 0.3s ease;
    display: inline-block;
}

.cta-btn {
    background-color: #f1f2f6;
    color: #6c5ce7;
    border: 2px solid transparent;
}

.cta-btn:hover {
    background-color: #e2e4ec;
}

/* =========================================
   HERO SECTION (Steps 4 & 5)
   ========================================= */
.hero {
    padding: 5rem 5%;
    flex-grow: 1; /* Pushes footer down */
}

.hero-content {
    display: flex; /* Step 4: Arrange text and image side-by-side */
    justify-content: space-between;
    align-items: center; /* Step 5: Properly align hero content vertically */
    gap: 4rem;
    max-width: 1200px;
    margin: 0 auto;
}

.hero-text {
    flex: 1; /* Takes up half the space */
}

.hero-text h1 {
    font-size: 3.5rem;
    line-height: 1.2;
    color: #2d3436;
    margin-bottom: 1.5rem;
}

.hero-text p {
    font-size: 1.1rem;
    line-height: 1.6;
    color: #636e72;
    margin-bottom: 2rem;
}

.hero-btn {
    background-color: #6c5ce7;
    color: #fff;
    box-shadow: 0 4px 15px rgba(108, 92, 231, 0.3);
}

.hero-btn:hover {
    background-color: #5b4bc4;
    transform: translateY(-2px);
}

.hero-image {
    flex: 1; /* Takes up the other half of the space */
    display: flex;
    justify-content: flex-end;
}

.hero-image img {
    max-width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}

/* =========================================
   FOOTER (Step 6)
   ========================================= */
.footer {
    background-color: #2d3436;
    color: #dfe6e9;
    padding: 2rem 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: auto;
}

.footer-links a {
    color: #dfe6e9;
    text-decoration: none;
    margin-left: 1.5rem;
    font-size: 0.9rem;
}

.footer-links a:hover {
    text-decoration: underline;
}

/* =========================================
   RESPONSIVE DESIGN (Step 7)
   ========================================= */
@media screen and (max-width: 900px) {
    /* Stack hero section vertically on tablets */
    .hero-content {
        flex-direction: column;
        text-align: center;
        gap: 3rem;
    }
    
    .hero-image {
        justify-content: center;
    }

    .hero-text h1 {
        font-size: 2.8rem;
    }
}

@media screen and (max-width: 768px) {
    /* Stack header elements on mobile */
    .header {
        flex-direction: column;
        gap: 1.5rem;
    }
    
    .nav-links {
        gap: 1rem;
        flex-wrap: wrap;
        justify-content: center;
    }

    /* Stack footer elements */
    .footer {
        flex-direction: column;
        gap: 1rem;
        text-align: center;
    }
    
    .footer-links a {
        margin: 0 0.5rem;
    }
}
How to complete Step 7 (Check Layout):
To ensure your assignment meets the final step, open the index.html file in your browser and do the following:

Desktop View: View the page fullscreen. The header elements should be spread across the top, and the hero text and image should sit perfectly side-by-side in a 50/50 split.

Tablet/Mobile View: Slowly drag the browser window to make it narrower. Once it hits 900px (tablet width), the image will drop below the text, and the text will center itself. Below 768px (mobile width), the navigation bar and footer will also stack to ensure nothing overflows the screen.