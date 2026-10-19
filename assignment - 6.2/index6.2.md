Here is the complete code for your assignment, providing the HTML structure and the CSS to style the three distinct cards while demonstrating the requested display properties.

index.html
This file contains the structure for the three pricing cards and includes specific elements (like <span> and <a>) to demonstrate different display types.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pricing Cards - Display & Backgrounds</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <h1>Select Your Plan</h1>
    <p>Demonstrating backgrounds, borders, and <span class="highlight-inline">display properties</span> in CSS.</p>
  </header>

  <main class="card-container">
    
    <!-- Card 1: Basic -->
    <article class="card card-basic">
      <div class="card-content">
        <h2>Basic Plan</h2>
        <p>Perfect for individuals just getting started. Includes all the core features you need.</p>
      </div>
      <a href="#" class="btn btn-basic">Choose Basic</a>
    </article>

    <!-- Card 2: Standard -->
    <article class="card card-standard">
      <div class="card-content">
        <h2>Standard Plan</h2>
        <p>Our most popular tier. Includes advanced tools and Priority Support.</p>
      </div>
      <a href="#" class="btn btn-standard">Choose Standard</a>
    </article>

    <!-- Card 3: Premium -->
    <article class="card card-premium">
      <div class="card-content">
        <h2>Premium Plan</h2>
        <p>For enterprise users. Uncapped limits, 24/7 support, and custom onboarding.</p>
      </div>
      <a href="#" class="btn btn-premium">Choose Premium</a>
    </article>

  </main>

</body>
</html>
style.css
This stylesheet fulfills the requirements for distinct backgrounds, borders, border-radius, sizing constraints (width, height, max-width), and explicitly demonstrates display: block, inline, and inline-block.

CSS
/* Base Reset & Typography */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: system-ui, -apple-system, sans-serif;
  background-color: #f8fafc;
  color: #334155;
  padding: 40px 20px;
}

header {
  text-align: center;
  margin-bottom: 40px;
}

/* 
  DISPLAY: INLINE (Demonstration)
  Takes up only as much width as necessary. Ignores top/bottom margins and padding for layout flow. 
*/
.highlight-inline {
  display: inline;
  background-color: #fef08a; /* Yellow highlight */
  padding: 2px 4px;
  border-radius: 4px;
  font-weight: bold;
}

/* Layout Container */
.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
}

/* 
  DISPLAY: BLOCK (Demonstration)
  Forces a line break before and after the element. Takes up full width available unless constrained.
  (Applied here to the cards, though flexbox manages their layout horizontally)
*/
.card {
  display: block; 
  
  /* Sizing Requirements: width, height, and max-width */
  width: 100%;
  max-width: 320px; 
  height: 380px; /* Fixed height to demonstrate requirement */
  
  /* Card Layout via Flexbox for internal alignment */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  
  /* Rounded Corners */
  border-radius: 12px;
  padding: 24px;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}

.card-content h2 {
  margin-bottom: 16px;
  font-size: 1.5rem;
}

.card-content p {
  line-height: 1.6;
  color: inherit;
}

/* 
  DISPLAY: INLINE-BLOCK (Demonstration)
  Flows like text (inline) but allows setting width, height, padding, and margins (like block).
*/
.btn {
  display: inline-block;
  text-decoration: none;
  padding: 12px 24px;
  border-radius: 8px; /* Rounded corners for buttons */
  font-weight: 600;
  width: 100%;
  transition: transform 0.2s ease;
}

.btn:hover {
  transform: translateY(-2px);
}

/* 
  Card 1: Basic 
  Backgrounds & Borders 
*/
.card-basic {
  background-color: #ffffff;
  border: 1px solid #cbd5e1;
  color: #475569;
}
.btn-basic {
  background-color: #f1f5f9;
  color: #334155;
  border: 1px solid #cbd5e1;
}

/* 
  Card 2: Standard 
  Backgrounds & Borders 
*/
.card-standard {
  background-color: #eff6ff; /* Light Blue */
  border: 2px solid #3b82f6; /* Blue Border */
  color: #1e3a8a;
}
.btn-standard {
  background-color: #3b82f6;
  color: #ffffff;
  border: 1px solid transparent;
}

/* 
  Card 3: Premium 
  Backgrounds & Borders 
*/
.card-premium {
  background-color: #0f172a; /* Dark Slate */
  border: 2px solid #fbbf24; /* Gold Border */
  color: #f8fafc;
}
.btn-premium {
  background-color: #fbbf24; /* Gold Button */
  color: #0f172a;
  border: 1px solid transparent;
}