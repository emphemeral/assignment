Here is the complete code for your assignment, fulfilling all the positioning and z-index requirements.

index.html
This HTML file creates a page with enough content to scroll, a navigation bar, a product card containing a badge, and a floating action button (FAB).

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Positioning Practice</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- Step 2: Sticky Navigation Bar -->
  <nav class="sticky-nav">
    <div class="logo">StoreFront</div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#products">Products</a></li>
      <li><a href="#about">About</a></li>
    </ul>
  </nav>

  <!-- Step 1: Multiple Scrollable Sections -->
  <main>
    <section id="home" class="scroll-section section-light">
      <h1>Welcome to StoreFront</h1>
      <p>Scroll down to test the sticky navigation and floating button.</p>
    </section>

    <section id="products" class="scroll-section section-mid">
      <h2>Featured Products</h2>
      
      <!-- Step 5: The Parent Container (Relative) -->
      <article class="card">
        <!-- Step 4: The Badge (Absolute) -->
        <span class="badge">Limited Time!</span>
        
        <h3>Wireless Headphones</h3>
        <p>Crystal clear audio with active noise cancellation.</p>
        <button class="buy-btn">Buy Now</button>
      </article>
    </section>

    <section id="about" class="scroll-section section-dark">
      <h2>About Us</h2>
      <p>Keep scrolling to see how the sticky nav stays at the top of the viewport.</p>
    </section>
  </main>

  <!-- Step 3: Floating Action Button (Fixed) -->
  <a href="#" class="floating-btn">💬 Help</a>

</body>
</html>
style.css
This stylesheet strictly applies sticky, fixed, relative, and absolute positioning, alongside z-index to manage how these elements overlap as the user scrolls.

CSS
/* Base Reset */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: system-ui, -apple-system, sans-serif;
  color: #334155;
  background-color: #f8fafc;
}

/* Step 2: Sticky Navigation Bar */
.sticky-nav {
  position: sticky;
  top: 0; /* Required for sticky to work */
  
  background-color: #0f172a;
  color: white;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  
  /* Step 6: Keep nav above scrolling content */
  z-index: 100; 
}

.logo {
  font-size: 1.25rem;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

/* Step 1: Scrollable Sections */
.scroll-section {
  /* Forcing a tall height so the page is scrollable */
  min-height: 80vh; 
  padding: 4rem 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.section-light { background-color: #f8fafc; }
.section-mid   { background-color: #e2e8f0; }
.section-dark  { background-color: #cbd5e1; }

.scroll-section h1, .scroll-section h2 {
  margin-bottom: 1rem;
}

/* Step 5: Relative Parent Container */
.card {
  position: relative; /* Acts as the anchor point for the absolute badge */
  
  background: white;
  padding: 2.5rem 1.5rem;
  border-radius: 12px;
  width: 300px;
  margin-top: 2rem;
  box-shadow: 0 10px 15px rgba(0,0,0,0.1);
}

.card h3 {
  margin-bottom: 0.5rem;
}

.card p {
  margin-bottom: 1.5rem;
  color: #64748b;
}

.buy-btn {
  background: #3b82f6;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  cursor: pointer;
}

/* Step 4: Absolute Positioned Badge */
.badge {
  position: absolute;
  top: -12px;   /* Pushed slightly outside the top edge of the card */
  right: -12px; /* Pushed slightly outside the right edge of the card */
  
  background-color: #ef4444; /* Red */
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 999px;
  font-size: 0.85rem;
  font-weight: bold;
  box-shadow: 0 2px 4px rgba(0,0,0,0.2);
  
  /* Step 6: Keeps badge cleanly above the card contents */
  z-index: 10; 
}

/* Step 3: Fixed Floating Action Button */
.floating-btn {
  position: fixed;
  bottom: 2rem;
  right: 2rem;
  
  background-color: #10b981; /* Green */
  color: white;
  text-decoration: none;
  padding: 1rem 1.5rem;
  border-radius: 999px;
  font-weight: bold;
  box-shadow: 0 4px 10px rgba(0,0,0,0.2);
  
  /* Step 6: Highest z-index to stay above everything (nav, cards, text) */
  z-index: 1000; 
}
For your submission screenshot: Open index.html in your browser. Scroll down slightly so that the black navigation bar is sticking to the top of the window while hovering over the gray background, making sure the red "Limited Time!" badge and the green "💬 Help" floating button in the bottom right corner are both visible in the frame.