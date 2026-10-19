Here is the complete solution for Assignment 9.2. This assignment focuses on the two most important elements of readability: ensuring your text scales beautifully across all devices and guaranteeing your images never break out of their containers.

This solution demonstrates the modern CSS clamp() function for truly fluid typography.

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Typography Article</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 1: Create an article page -->
    <main class="article-container">
        
        <header class="article-header">
            <!-- Step 2: Add headings and paragraphs -->
            <h1>The Art of Fluid Typography</h1>
            <p class="meta">Published on October 19, 2026 • By Design Pro</p>
        </header>

        <!-- Step 2: Add images -->
        <img src="https://picsum.photos/id/1025/1200/600" alt="A pug wrapped in a blanket" class="hero-image">

        <section class="content">
            <h2>Why Static Fonts Are Dead</h2>
            <p>For years, web developers have relied on fixed pixel values for their typography. But as the variety of screen sizes continues to explode, from tiny smartwatches to massive ultrawide monitors, locking your text into a static size is no longer viable.</p>

            <blockquote>
                "Fluid typography is the secret ingredient to creating designs that feel tailor-made for every device, adapting naturally like water filling a cup."
            </blockquote>

            <h2>The Magic of Clamp()</h2>
            <p>Modern CSS provides us with the <code>clamp()</code> function. This incredible tool takes three values: a minimum size, a preferred responsive size, and a maximum size. It automatically scales your text up and down based on the user's screen width, without needing complex media queries.</p>

            <img src="https://picsum.photos/id/119/800/500" alt="Notebook and workspace" class="content-image">

            <p>Additionally, ensuring your images are responsive is just as crucial. By setting a simple <code>max-width: 100%</code> and <code>height: auto</code>, your images will gracefully shrink on mobile devices while never expanding past their container on a wide desktop screen.</p>
        </section>

    </main>

</body>
</html>
2. CSS Styling (style.css)
CSS
/* Basic Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    /* Sets the base font size to browser default (usually 16px) */
    font-size: 100%; 
}

body {
    font-family: 'Georgia', serif;
    color: #2c3e50;
    background-color: #fcfcfc;
    /* Step 6: Improve spacing. 1.8 provides excellent vertical reading rhythm */
    line-height: 1.8; 
    padding: 2rem 0;
}

/* =========================================
   CONTAINER & LINE LENGTH (Steps 5 & 6)
   ========================================= */
.article-container {
    /* Step 5: Set a suitable max-width. 800px creates an optimal line length 
       of roughly 65-75 characters, which prevents eye strain on desktops. */
    max-width: 800px;
    margin: 0 auto;
    
    /* Padding ensures text doesn't touch the extreme edges of mobile screens */
    padding: 0 1.5rem; 
}

.article-header {
    margin-bottom: 2rem;
    text-align: center;
}

/* =========================================
   TYPOGRAPHY (Step 3)
   ========================================= */

h1 {
    /* 
       Step 3: Use clamp() for fluid font sizes.
       clamp(MIN, PREFERRED, MAX)
       - Minimum size: 2rem (32px) on mobile
       - Preferred size: 5vw (5% of the viewport width) as screen stretches
       - Maximum size: 4rem (64px) caps it so it isn't massive on a 4K TV
    */
    font-size: clamp(2rem, 5vw, 4rem);
    line-height: 1.2;
    margin-bottom: 0.5rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #1a1a1a;
}

.meta {
    color: #7f8c8d;
    font-size: 0.9rem; /* Using rem for standard sizing */
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

h2 {
    /* Fluid subheadings */
    font-size: clamp(1.5rem, 3vw, 2.5rem);
    margin-top: 3rem;
    margin-bottom: 1rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #1a1a1a;
}

p {
    /* Step 3: Using rem for scalable paragraphs (1.125rem = 18px) */
    font-size: 1.125rem; 
    margin-bottom: 1.5rem;
}

blockquote {
    font-size: clamp(1.25rem, 2.5vw, 1.75rem);
    font-style: italic;
    color: #34495e;
    border-left: 4px solid #3498db;
    margin: 2rem 0;
    background-color: #f8f9fa;
    padding: 1.5rem;
    border-radius: 0 8px 8px 0;
}

/* =========================================
   IMAGES (Steps 4 & 7)
   ========================================= */
img {
    /* Step 4: Apply max-width: 100% and height: auto */
    /* This prevents the image from breaking out of its container and 
       ensures it maintains its original aspect ratio! */
    max-width: 100%;
    height: auto;
    
    display: block; /* Removes the tiny white space that sits under inline images */
    border-radius: 8px;
}

.hero-image {
    margin-bottom: 3rem;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
}

.content-image {
    margin: 2.5rem 0;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
}
How to test your layout (Step 7):
Open the index.html file in your browser and slowly drag the window horizontally to make it wider and narrower.

Watch the text: Notice how the h1 and h2 headings dynamically scale up and down like water filling a space, without suddenly "jumping" sizes like they would with standard media queries.

Watch the images: Notice how the images perfectly shrink down with the width of your screen on mobile sizes, but stop expanding exactly when they hit 800px wide, preserving their quality.