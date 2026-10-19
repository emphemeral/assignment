1. HTML Structure (index.html)HTML<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pricing & Login</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- PRICING SECTION -->
    <section class="pricing-section">
        <h2 class="section-title">Our Pricing Plans</h2>
        
        <!-- Step 3: Parent container for pricing cards -->
        <div class="pricing-container">
            
            <!-- Step 1 & 2: Basic Card with price, features, and button -->
            <div class="pricing-card">
                <h3>Basic</h3>
                <p class="price">$9.99/mo</p>
                <ul class="features">
                    <li>1 User</li>
                    <li>10GB Storage</li>
                    <li>Email Support</li>
                </ul>
                <button class="btn">Choose Basic</button>
            </div>

            <!-- Step 1 & 2: Pro Card -->
            <div class="pricing-card pro">
                <h3>Pro</h3>
                <p class="price">$19.99/mo</p>
                <ul class="features">
                    <li>5 Users</li>
                    <li>50GB Storage</li>
                    <li>Priority Support</li>
                </ul>
                <button class="btn">Choose Pro</button>
            </div>

            <!-- Step 1 & 2: Premium Card -->
            <div class="pricing-card">
                <h3>Premium</h3>
                <p class="price">$29.99/mo</p>
                <ul class="features">
                    <li>Unlimited Users</li>
                    <li>500GB Storage</li>
                    <li>24/7 Phone Support</li>
                </ul>
                <button class="btn">Choose Premium</button>
            </div>

        </div>
    </section>

    <hr>

    <!-- LOGIN SECTION -->
    <!-- Step 5: Container to center the login form -->
    <section class="login-section">
        <form class="login-form">
            <h2>Welcome Back</h2>
            <div class="input-group">
                <label for="username">Username</label>
                <input type="text" id="username" placeholder="Enter username">
            </div>
            <div class="input-group">
                <label for="password">Password</label>
                <input type="password" id="password" placeholder="Enter password">
            </div>
            <button type="submit" class="btn login-btn">Log In</button>
        </form>
    </section>

</body>
</html>
2. CSS Styling (style.css)   CSS/* Basic Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: sans-serif;
}

body {
    background-color: #f4f7f6;
    color: #333;
}

.section-title {
    text-align: center;
    margin: 3rem 0 2rem;
    font-size: 2rem;
}

hr {
    border: 0;
    height: 1px;
    background: #ccc;
    margin: 2rem 0;
}

/* =========================================
   PRICING CARDS (Steps 3, 4, 6)
   ========================================= */

.pricing-container {
    display: flex;                  /* Step 3: Flexbox on parent container */
    justify-content: center;        /* Step 4: Align cards horizontally to the center */
    align-items: center;            /* Step 4: Align cards vertically */
    gap: 2rem;                      /* Spacing between cards */
    padding: 2rem;
    flex-wrap: wrap;                /* Allows cards to wrap on smaller screens */
}

.pricing-card {
    display: flex;
    flex-direction: column;         /* Step 6: Practical use of flex-direction to stack card contents vertically */
    align-items: center;            /* Centers text inside the card */
    background: #fff;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    width: 250px;
    transition: transform 0.3s;
}

.pricing-card:hover {
    transform: translateY(-10px);
}

/* Highlight the middle "Pro" card slightly */
.pricing-card.pro {
    border: 2px solid #3498db;
    transform: scale(1.05);
}

.pricing-card.pro:hover {
    transform: scale(1.05) translateY(-10px);
}

.price {
    font-size: 1.5rem;
    font-weight: bold;
    color: #3498db;
    margin: 1rem 0;
}

.features {
    list-style: none;
    margin-bottom: 2rem;
    width: 100%;
}

.features li {
    padding: 0.5rem 0;
    border-bottom: 1px solid #eee;
    text-align: center;
}

/* =========================================
   LOGIN FORM (Steps 5 & 6)
   ========================================= */

.login-section {
    display: flex;                  /* Step 5: Flexbox to center the form */
    justify-content: center;        /* Step 5: Centers form horizontally */
    align-items: center;            /* Step 5: Centers form vertically */
    min-height: 60vh;               /* Gives the container enough height to demonstrate vertical centering */
    padding: 2rem;
}

.login-form {
    display: flex;
    flex-direction: column;         /* Step 6: Uses flex-direction to stack form inputs */
    background: #fff;
    padding: 2rem 3rem;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    width: 100%;
    max-width: 400px;
    gap: 1.5rem;                    /* Spacing between form elements */
}

.login-form h2 {
    text-align: center;
    margin-bottom: 1rem;
}

.input-group {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.input-group input {
    padding: 0.75rem;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 1rem;
}

/* Shared Button Styles */
.btn {
    background-color: #3498db;
    color: #fff;
    border: none;
    padding: 0.75rem 1.5rem;
    border-radius: 4px;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s;
    width: 100%;
    margin-top: auto;               /* Pushes the button to the bottom of the pricing card */
}

.btn:hover {
    background-color: #2980b9;
}