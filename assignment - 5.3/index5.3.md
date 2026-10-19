index.html

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typography Showcase</title>
    
    <!-- Step 1: Link 2 complementary font families from Google Fonts (Playfair Display & Roboto) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="showcase-header">
        <h1>Typography Showcase</h1>
        <p class="subtitle">Exploring Web Fonts and CSS Text Properties</p>
    </header>

    <main>
        <!-- Step 6: Section 1 - Heading Styles -->
        <section id="heading-styles" class="card">
            <h2>Heading Styles</h2>
            <h1 class="heading-large">Main Title (H1)</h1>
            <h2 class="heading-medium">Section Title (H2)</h2>
            <h3 class="heading-small">Subsection Title (H3)</h3>
        </section>

        <!-- Step 6: Section 2 - Paragraph Styles -->
        <section id="paragraph-styles" class="card">
            <h2>Paragraph Styles</h2>
            <p class="standard-paragraph">
                This is a standard paragraph. It uses the default line height and letter spacing for the body font. Good typography ensures that the user can read the content comfortably without eye strain.
            </p>
            <p class="spaced-paragraph">
                This paragraph demonstrates adjusted <strong>letter-spacing</strong> and a taller <strong>line-height</strong>. Notice how the extra breathing room changes the texture and readability of a dense block of text.
            </p>
            <p class="centered-paragraph">
                This paragraph is <strong>center-aligned</strong>. It is often used for pull quotes or highlighting a central idea within an article.
            </p>
        </section>

        <!-- Step 6: Section 3 - Text Emphasis -->
        <section id="text-emphasis" class="card">
            <h2>Text Emphasis</h2>
            <p>You can emphasize text in various ways to draw the user's attention:</p>
            <ul>
                <li><span class="weight-bold">Bold Weight:</span> Used for strong importance.</li>
                <li><span class="weight-light">Light Weight:</span> Used for subtle text or contrasting large headers.</li>
                <li><span class="style-italic">Italic Style:</span> Used for titles of works, foreign words, or gentle emphasis.</li>
                <li><span class="decor-underline">Underlined Text:</span> Typically reserved for links, but can be forced via text-decoration.</li>
                <li><span class="decor-strikethrough">Strikethrough Text:</span> Used to indicate deleted or outdated information.</li>
            </ul>
        </section>
    </main>
</body>
</html>
style.css

CSS
/* Step 2: Set different fonts for heading and body text */
:root {
    --font-heading: 'Playfair Display', serif;
    --font-body: 'Roboto', sans-serif;
    --color-bg: #f8f9fa;
    --color-text: #333;
    --color-accent: #2c3e50;
}

body {
    font-family: var(--font-body);
    background-color: var(--color-bg);
    color: var(--color-text);
    margin: 0;
    padding: 20px;
    /* Step 5: Default line-height */
    line-height: 1.6; 
}

h1, h2, h3, h4, h5, h6 {
    font-family: var(--font-heading);
    color: var(--color-accent);
    margin-top: 0;
}

.showcase-header {
    /* Step 4: Apply text-align */
    text-align: center;
    margin-bottom: 40px;
}

.subtitle {
    /* Step 4: Apply font-style */
    font-style: italic; 
    color: #666;
    /* Step 5: Adjust letter-spacing */
    letter-spacing: 1.5px; 
}

.card {
    background: #ffffff;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 30px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}

/* Step 3: Use different font sizes and weights for Headings */
.heading-large {
    font-size: 3rem;
    font-weight: 700;
}

.heading-medium {
    font-size: 2rem;
    font-weight: 400;
}

.heading-small {
    font-size: 1.25rem;
    font-weight: 700;
    text-transform: uppercase;
}

/* Paragraph Styles */
.standard-paragraph {
    font-size: 1rem;
    font-weight: 400;
}

.spaced-paragraph {
    /* Step 5: Adjust letter-spacing and line-height */
    letter-spacing: 0.5px;
    line-height: 2.2;
    font-size: 1.1rem;
    color: #444;
}

.centered-paragraph {
    /* Step 4: Apply text-align */
    text-align: center;
    font-size: 1.1rem;
    font-style: italic;
    margin: 20px 0;
}

/* Step 3 & 4: Text Emphasis Utility Classes */
.weight-bold {
    font-weight: 700;
}

.weight-light {
    font-weight: 300;
}

.style-italic {
    font-style: italic;
}

.decor-underline {
    /* Step 4: Apply text-decoration */
    text-decoration: underline;
    text-decoration-color: var(--color-accent);
    text-decoration-thickness: 2px;
}

.decor-strikethrough {
    text-decoration: line-through;
    color: #888;
}

ul {
    list-style-type: square;
    padding-left: 20px;
}

li {
    margin-bottom: 10px;
}