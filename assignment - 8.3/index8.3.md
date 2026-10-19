Here is the complete solution for Assignment 8.3. This assignment focuses on grid-template-areas, which is one of the most visual and intuitive ways to construct page layouts in CSS.

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Magazine Grid Layout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 2: Define a grid container -->
    <div class="magazine-layout">

        <!-- Step 1: Create header, navigation, main article, sidebar, and footer sections -->
        <header class="header">
            <h1>The Daily Grid</h1>
            <p>Your source for modern web design news</p>
        </header>

        <nav class="nav">
            <ul>
                <li><a href="#">World</a></li>
                <li><a href="#">Technology</a></li>
                <li><a href="#">Design</a></li>
                <li><a href="#">Culture</a></li>
            </ul>
        </nav>

        <main class="main-article">
            <h2>The CSS Grid Revolution</h2>
            <img src="https://via.placeholder.com/800x400?text=CSS+Grid" alt="Article Banner">
            <p><strong>By Jane Doe | October 19, 2026</strong></p>
            <p>CSS Grid has fundamentally changed how we approach web layout. Before Grid, developers relied on hacks like floats and complex flexbox setups to achieve two-dimensional layouts. Now, we can intuitively name sections of our page and place them exactly where we want them.</p>
            <p>Using the <code>grid-template-areas</code> property, you literally draw a map of your interface in your CSS file. It makes adjusting layouts for mobile devices incredibly simple, as you only need to redraw the map inside a media query!</p>
        </main>

        <aside class="sidebar">
            <h3>Trending Now</h3>
            <ul class="trending-list">
                <li><a href="#">10 Flexbox Tricks You Didn't Know</a></li>
                <li><a href="#">Why Typography Matters in 2026</a></li>
                <li><a href="#">Building Accessible Color Palettes</a></li>
                <li><a href="#">The Death of Float-Based Layouts</a></li>
            </ul>
            
            <div class="ad-space">
                <p>Advertisement</p>
            </div>
        </aside>

        <footer class="footer">
            <p>&copy; 2026 The Daily Grid Magazine. All rights reserved.</p>
        </footer>

    </div>

</body>
</html>
2. CSS Styling (style.css)
CSS
/* Basic Reset & Magazine Typography */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: #f4f1ea; /* Slightly off-white, paper-like background */
    color: #1a1a1a;
    font-family: 'Merriweather', 'Georgia', serif; /* Serif font for magazine feel */
    line-height: 1.6;
    padding: 2rem;
}

h1, h2, h3, a {
    font-family: 'Helvetica Neue', Arial, sans-serif; /* Contrast headings with sans-serif */
}

/* =========================================
   GRID LAYOUT CONTAINER (Steps 2, 3 & 5)
   ========================================= */
.magazine-layout {
    display: grid;
    max-width: 1200px;
    margin: 0 auto;
    gap: 1.5rem; /* Space between grid areas */

    /* Step 5: Give the main article more space than the sidebar (3 fractions vs 1 fraction) */
    grid-template-columns: 3fr 1fr;

    /* Step 3: Set the layout using grid-template-areas */
    grid-template-areas:
        "header  header"
        "nav     nav"
        "main    sidebar"
        "footer  footer";
}

/* =========================================
   ASSIGN NAMED GRID AREAS (Step 4)
   ========================================= */
.header       { grid-area: header; }
.nav          { grid-area: nav; }
.main-article { grid-area: main; }
.sidebar      { grid-area: sidebar; }
.footer       { grid-area: footer; }

/* =========================================
   COMPONENT STYLING
   ========================================= */
.header {
    text-align: center;
    padding: 2rem 0;
    border-bottom: 4px solid #1a1a1a;
    border-top: 4px solid #1a1a1a;
}

.header h1 {
    font-size: 4rem;
    text-transform: uppercase;
    letter-spacing: 2px;
}

.nav {
    border-bottom: 1px solid #ccc;
    padding-bottom: 1rem;
}

.nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 2rem;
}

.nav a {
    text-decoration: none;
    color: #1a1a1a;
    font-weight: bold;
    text-transform: uppercase;
    font-size: 0.9rem;
}

.nav a:hover {
    color: #c0392b;
}

.main-article {
    padding-right: 1rem;
}

.main-article h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.main-article img {
    width: 100%;
    height: auto;
    margin-bottom: 1.5rem;
}

.main-article p {
    margin-bottom: 1.5rem;
    font-size: 1.1rem;
}

.sidebar {
    border-left: 1px solid #ccc;
    padding-left: 1.5rem;
}

.sidebar h3 {
    font-size: 1.2rem;
    text-transform: uppercase;
    margin-bottom: 1rem;
    border-bottom: 2px solid #1a1a1a;
    display: inline-block;
}

.trending-list {
    list-style: none;
    margin-bottom: 2rem;
}

.trending-list li {
    margin-bottom: 1rem;
}

.trending-list a {
    text-decoration: none;
    color: #333;
    font-weight: 500;
}

.trending-list a:hover {
    text-decoration: underline;
    color: #c0392b;
}

.ad-space {
    background-color: #e0e0e0;
    height: 250px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #777;
    font-family: sans-serif;
    border: 1px solid #ccc;
}

.footer {
    text-align: center;
    padding: 2rem 0;
    border-top: 2px solid #1a1a1a;
    font-family: sans-serif;
    font-size: 0.9rem;
    color: #555;
    margin-top: 2rem;
}

/* =========================================
   RESPONSIVE DESIGN (Step 6)
   ========================================= */
/* Watch the grid-template-areas map change completely on mobile! */
@media screen and (max-width: 800px) {
    .magazine-layout {
        grid-template-columns: 1fr; /* Switch to a single column */
        
        /* Redefine the layout map for small screens */
        grid-template-areas:
            "header"
            "nav"
            "main"
            "sidebar"
            "footer";
    }

    .sidebar {
        border-left: none;
        border-top: 1px solid #ccc;
        padding-left: 0;
        padding-top: 1.5rem;
    }
    
    .nav ul {
        flex-wrap: wrap;
    }
}
How to complete Step 6 (Test different sizes and alignments):
Desktop View: Open your index.html file in the browser on a wide screen. You will see the visual map defined in grid-template-areas: "main sidebar" perfectly distributing the space (75% width to the article, 25% width to the sidebar).

Mobile View: Resize your browser to be narrower than 800px. Because of the media query at the bottom of the CSS, the grid-template-areas map instantly transforms into a vertical stack ("header" "nav" "main" "sidebar" "footer"). This demonstrates the absolute power of grid areas—you completely restructured the entire layout layout without changing any HTML!