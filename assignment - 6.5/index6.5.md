index.html
This file contains the structure for a responsive Product Card. It includes the required image, title, description, price, buy button, and a promotional badge.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Product Card Component</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <main class="page-wrapper">
    
    <!-- Product Card Component -->
    <article class="product-card">
      
      <!-- Image & Badge Container (Relative Positioning) -->
      <div class="product-image-container">
        <!-- Badge (Absolute Positioning) -->
        <span class="product-badge">Sale</span>
        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=600&q=80" alt="Premium Wireless Headphones" class="product-image">
      </div>

      <!-- Content Container -->
      <div class="product-info">
        <h2 class="product-title">SonicPro Wireless Headphones</h2>
        <p class="product-description">Experience immersive sound and industry-leading active noise cancellation with our premium over-ear headphones. 30-hour battery life.</p>
        
        <div class="product-checkout-row">
          <div class="product-pricing">
            <span class="product-price">$249.00</span>
            <span class="product-price-original">$299.00</span>
          </div>
          <button class="product-btn">Add to Cart</button>
        </div>
      </div>

    </article>

  </main>

</body>
</html>
style.css
This stylesheet strictly adheres to the box model, utilizes clean semantic class names, applies background/border properties, and uses positioning for the "Sale" badge. The use of max-width and 100% widths ensures the card remains responsive on mobile screens.

CSS
/* --- Base Reset --- */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: system-ui, -apple-system, sans-serif;
  background-color: #f1f5f9;
  color: #334155;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  padding: 20px;
}

/* --- Product Card Container --- */
.product-card {
  background-color: #ffffff;
  border: 1px solid #e2e8f0;
  border-radius: 16px;
  
  /* Box Model & Responsive Sizing */
  width: 100%;
  max-width: 360px;
  overflow: hidden; /* Ensures the image doesn't break the rounded corners */
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.product-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
}

/* --- Image & Positioning --- */
.product-image-container {
  /* Parent container needs relative positioning to anchor the absolute badge */
  position: relative; 
  height: 240px;
  width: 100%;
  background-color: #e2e8f0;
}

.product-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

/* 
  Badge using Absolute Positioning
  Rule 3: Place a badge or button using positioning 
*/
.product-badge {
  position: absolute;
  top: 16px;
  right: 16px;
  
  background-color: #ef4444; /* Red background */
  color: #ffffff;
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 6px 12px;
  border-radius: 9999px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.2);
  z-index: 10;
}

/* --- Card Content --- */
.product-info {
  /* Applying Box Model Padding */
  padding: 24px;
}

.product-title {
  font-size: 1.25rem;
  font-weight: 700;
  color: #0f172a;
  margin-bottom: 8px;
  line-height: 1.3;
}

.product-description {
  font-size: 0.9rem;
  color: #64748b;
  line-height: 1.6;
  margin-bottom: 24px;
}

/* --- Checkout Area --- */
.product-checkout-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: auto;
}

.product-pricing {
  display: flex;
  flex-direction: column;
}

.product-price {
  font-size: 1.25rem;
  font-weight: 800;
  color: #0f172a;
}

.product-price-original {
  font-size: 0.85rem;
  color: #94a3b8;
  text-decoration: line-through;
}

/* Buy Button */
.product-btn {
  background-color: #2563eb;
  color: #ffffff;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.95rem;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.product-btn:hover {
  background-color: #1d4ed8;
}
For your submission screenshot: Open index.html in your browser. Ensure your screenshot captures the full card on the gray background, clearly showing the red "SALE" badge floating over the top right corner of the headphone image, and the rounded corners on the card itself. Shrinking your browser window will prove the card remains responsive (it won't exceed 360px wide, but shrinks fluidly on very small screens).