1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Product Listing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1 class="page-title">Our Products</h1>
    </header>

    <!-- Step 3: Container for the product cards -->
    <main class="product-container">
        
        <!-- Step 1 & 2: Product Card 1 -->
        <article class="product-card">
            <img src="https://via.placeholder.com/300x200?text=Product+1" alt="Product 1">
            <h2 class="product-name">Wireless Headphones</h2>
            <p class="product-price">$99.99</p>
            <button class="btn">Add to Cart</button>
        </article>

        <!-- Product Card 2 -->
        <article class="product-card">
            <img src="https://via.placeholder.com/300x200?text=Product+2" alt="Product 2">
            <h2 class="product-name">Smart Watch</h2>
            <p class="product-price">$149.99</p>
            <button class="btn">Add to Cart</button>
        </article>

        <!-- Product Card 3 -->
        <article class="product-card">
            <img src="https://via.placeholder.com/300x200?text=Product+3" alt="Product 3">
            <h2 class="product-name">Bluetooth Speaker</h2>
            <p class="product-price">$59.99</p>
            <button class="btn">Add to Cart</button>
        </article>

        <!-- Product Card 4 -->
        <article class="product-card">
            <img src="https://via.placeholder.com/300x200?text=Product+4" alt="Product 4">
            <h2 class="product-name">Mechanical Keyboard</h2>
            <p class="product-price">$129.99</p>
            <button class="btn">Add to Cart</button>
        </article>

        <!-- Product Card 5 -->
        <article class="product-card">
            <img src="https://via.placeholder.com/300x200?text=Product+5" alt="Product 5">
            <h2 class="product-name">Gaming Mouse</h2>
            <p class="product-price">$49.99</p>
            <button class="btn">Add to Cart</button>
        </article>

        <!-- Product Card 6 -->
        <article class="product-card">
            <img src="https://via.placeholder.com/300x200?text=Product+6" alt="Product 6">
            <h2 class="product-name">4K Monitor</h2>
            <p class="product-price">$299.99</p>
            <button class="btn">Add to Cart</button>
        </article>

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
    font-family: Arial, sans-serif;
}

body {
    background-color: #f8f9fa;
    padding: 2rem;
}

.page-title {
    text-align: center;
    margin-bottom: 2rem;
    color: #333;
}

/* =========================================
   PRODUCT CONTAINER (Steps 3 & 4)
   ========================================= */
.product-container {
    display: flex;             /* Step 3: Use display: flex */
    flex-wrap: wrap;           /* Step 3: Allow cards to wrap to the next line (Step 6) */
    gap: 2rem;                 /* Step 4: Add spacing between cards using gap */
    justify-content: center;   /* Center the cards when they wrap */
    max-width: 1200px;
    margin: 0 auto;
}

/* =========================================
   PRODUCT CARDS (Step 5)
   ========================================= */
.product-card {
    display: flex;
    flex-direction: column;    /* Stack image, title, price, and button vertically */
    background-color: #fff;
    border-radius: 8px;
    padding: 1.5rem;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    
    /* 
       Step 5: Experiment with flex-grow, flex-shrink, and flex-basis.
       The shorthand 'flex: 1 1 300px' means:
       - flex-grow: 1 (Cards will grow to fill available empty space on the row)
       - flex-shrink: 1 (Cards will shrink if the container is smaller than 300px)
       - flex-basis: 300px (The ideal starting width of the card)
    */
    flex: 1 1 300px; 
    
    /* Optional: Set a max-width so they don't stretch too wide on huge screens */
    max-width: 350px; 
    transition: transform 0.3s ease;
}

.product-card:hover {
    transform: translateY(-5px);
}

.product-card img {
    width: 100%;               /* Makes image responsive inside the card */
    height: auto;
    border-radius: 4px;
    margin-bottom: 1rem;
}

.product-name {
    font-size: 1.25rem;
    color: #2c3e50;
    margin-bottom: 0.5rem;
}

.product-price {
    font-size: 1.2rem;
    font-weight: bold;
    color: #27ae60;
    margin-bottom: 1.5rem;
}

/* Push the button to the bottom if product names vary in length */
.btn {
    margin-top: auto;          
    background-color: #2c3e50;
    color: #fff;
    border: none;
    padding: 0.75rem;
    border-radius: 4px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
    text-align: center;
}

.btn:hover {
    background-color: #1a252f;
}
How to complete your submission (Step 6):
To finish your assignment and provide the required screenshots:

Open the index.html file in your web browser.

Take a Desktop Screenshot: Maximize your browser window. You should see the cards sitting side-by-side (likely 3 in a row, depending on your monitor width).

Take a Mobile Screenshot: Shrink the width of your browser window down to simulate a mobile phone. Because of flex-wrap: wrap and flex-basis: 300px, you will see the cards automatically snap into a single vertical column. Take a screenshot of this view.