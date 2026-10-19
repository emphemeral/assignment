Here is the complete solution for Assignment 9.4. Since a specific reference design wasn't provided, I have simulated a modern, professional "SaaS (Software as a Service)" reference design.

Step 1: Reference Design Analysis (Simulated)
Colors: Primary Blue (#2563eb), Dark Slate for text (#1e293b), Light Gray background (#f8fafc).

Typography: Modern Sans-Serif (system-ui, sans-serif).

Layout: Flexbox for the Navbar and Hero (side-by-side on desktop); CSS Grid for the 3-column Features section.

2. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern SaaS Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 3 & 4: Semantic tags and Navbar structure -->
    <header class="navbar">
        <div class="logo">NexusTech.</div>
        <nav>
            <ul class="nav-links">
                <li><a href="#product">Product</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#pricing">Pricing</a></li>
            </ul>
        </nav>
        <div class="nav-actions">
            <a href="#" class="btn btn-outline">Log In</a>
            <a href="#" class="btn btn-primary">Sign Up</a>
        </div>
    </header>

    <main>
        <!-- Step 3 & 4: Hero Section -->
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

        <!-- Step 3 & 4: Features Section -->
        <section class="features" id="features">
            <div class="section-header">
                <h2>Everything you need to succeed</h2>
                <p>Powerful tools packaged in an intuitive interface.</p>
            </div>
            
            <div class="features-grid">
                <!-- Feature Card 1 -->
                <article class="feature-card">
                    <div class="icon">⚡</div>
                    <h3>Lightning Fast</h3>
                    <p>Optimized infrastructure ensures your projects load in milliseconds, worldwide.</p>
                </article>

                <!-- Feature Card 2 -->
                <article class="feature-card">
                    <div class="icon">🔒</div>
                    <h3>Bank-grade Security</h3>
                    <p>Enterprise-level encryption and compliance built-in from day one.</p>
                </article>

                <!-- Feature Card 3 -->
                <article class="feature-card">
                    <div class="icon">🤝</div>
                    <h3>Team Collaboration</h3>
                    <p>Real-time syncing and commenting keeps your entire team on the same page.</p>
                </article>
            </div>
        </section>
    </main>

    <!-- Semantic Footer -->
    <footer class="footer">
        <p>&copy; 2026 NexusTech Inc. All rights reserved.</p>
    </footer>

</body>
</html>
3. CSS Styling (style.css)
CSS
/* =========================================
   BASE STYLES & VARIABLES (Step 7)
   ========================================= */
:root {
    --primary: #2563eb;
    --primary-hover: #1d4ed8;
    --text-dark: #1e293b;
    --text-light: #64748b;
    --bg-light: #f8fafc;
    --white: #ffffff;
}

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
}

img {
    max-width: 100%;
    height: auto;
    display: block;
    border-radius: 12px;
}

/* Shared Button Styles */
.btn {
    display: inline-block;
    text-decoration: none;
    padding: 0.5rem 1.25rem;
    border-radius: 6px;
    font-weight: 600;
    transition: all 0.2s ease;
    cursor: pointer;
}

.btn-large {
    padding: 0.75rem 1.5rem;
    font-size: 1.1rem;
}

.btn-primary {
    background-color: var(--primary);
    color: var(--white);
    border: 2px solid var(--primary);
}

.btn-primary:hover {
    background-color: var(--primary-hover);
    border-color: var(--primary-hover);
}

.btn-outline {
    background-color: transparent;
    color: var(--text-dark);
    border: 2px solid #e2e8f0;
}

.btn-outline:hover {
    border-color: var(--text-light);
}

/* =========================================
   NAVIGATION (Step 5 & 6: Flexbox Desktop)
   ========================================= */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.25rem 5%;
    background-color: var(--white);
    border-bottom: 1px solid #f1f5f9;
}

.logo {
    font-size: 1.5rem;
    font-weight: 800;
    color: var(--primary);
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 2.5rem;
}

.nav-links a {
    text-decoration: none;
    color: var(--text-light);
    font-weight: 500;
    transition: color 0.2s;
}

.nav-links a:hover {
    color: var(--primary);
}

.nav-actions {
    display: flex;
    gap: 1rem;
}

/* =========================================
   HERO SECTION (Step 5 & 6: Flexbox Desktop)
   ========================================= */
.hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 4rem;
    padding: 6rem 5%;
    max-width: 1400px;
    margin: 0 auto;
}

.hero-content {
    flex: 1; /* Takes up 50% width */
}

.hero-content h1 {
    font-size: 3.5rem;
    line-height: 1.1;
    margin-bottom: 1.5rem;
    letter-spacing: -0.02em;
}

.hero-content p {
    font-size: 1.25rem;
    color: var(--text-light);
    margin-bottom: 2.5rem;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
}

.hero-image {
    flex: 1; /* Takes up 50% width */
}

.hero-image img {
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

/* =========================================
   FEATURES SECTION (Step 5 & 6: Grid Desktop)
   ========================================= */
.features {
    background-color: var(--bg-light);
    padding: 6rem 5%;
}

.section-header {
    text-align: center;
    max-width: 600px;
    margin: 0 auto 4rem auto;
}

.section-header h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.section-header p {
    font-size: 1.125rem;
    color: var(--text-light);
}

.features-grid {
    display: grid;
    /* Explicitly 3 columns for this initial Desktop version */
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.feature-card {
    background-color: var(--white);
    padding: 2.5rem;
    border-radius: 12px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    border: 1px solid #f1f5f9;
}

.icon {
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
}

.feature-card h3 {
    font-size: 1.25rem;
    margin-bottom: 0.75rem;
}

.feature-card p {
    color: var(--text-light);
    font-size: 1rem;
}

/* =========================================
   FOOTER
   ========================================= */
.footer {
    text-align: center;
    padding: 2rem;
    background-color: var(--white);
    color: var(--text-light);
    border-top: 1px solid #f1f5f9;
}
Step 8: Submission Instructions
To submit your assignment:

Create a new folder on your computer named landing-page-project.

Inside that folder, create an images folder (even if you are linking to web images, it's good practice for the assignment requirement).

Save the HTML code as index.html and the CSS code as style.css in the root of the folder.

Open your terminal or GitHub Desktop, commit the initial version, and push it to a new GitHub repository.

Copy your GitHub repository URL and submit it!