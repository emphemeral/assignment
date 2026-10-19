1. HTML Structure (index.html)
This creates the header containing the logo, a semantic <nav> element with links, and a call-to-action button.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Navigation Bar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 1: Create a header containing a logo and navigation links -->
    <header class="navbar">
        <div class="logo">BrandLogo</div>
        
        <nav>
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
        
        <a href="#" class="btn">Sign Up</a>
    </header>

</body>
</html>
2. CSS Styling (style.css)
This applies Flexbox to align the items horizontally, spaces them out, and includes a media query to stack the items neatly when you shrink the browser width.

CSS
/* Basic Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: sans-serif;
}

/* Steps 2, 3 & 4: Flexbox Container Setup */
.navbar {
    display: flex;                      /* 2. Apply display: flex */
    justify-content: space-between;     /* 3. Set spacing between items */
    align-items: center;                /* 4. Align vertically */
    padding: 1rem 2rem;
    background-color: #222;
    color: #fff;
}

/* Step 5: Style the navigation links and button */
.logo {
    font-size: 1.5rem;
    font-weight: bold;
    cursor: pointer;
}

.nav-links {
    display: flex;                      /* Applies Flexbox to the list items */
    list-style: none;
    gap: 2rem;                          /* Spacing between individual links */
}

.nav-links a {
    color: #fff;
    text-decoration: none;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: #3498db;                     /* Changes color on hover */
}

.btn {
    background-color: #3498db;
    color: #fff;
    padding: 0.5rem 1.5rem;
    border-radius: 4px;
    text-decoration: none;
    font-weight: bold;
    transition: background-color 0.3s;
}

.btn:hover {
    background-color: #2980b9;
}

/* Step 6: Inspect the layout by changing the browser width */
/* Responsive styling for screens smaller than 768px */
@media screen and (max-width: 768px) {
    .navbar {
        flex-direction: column;         /* Stacks the logo, nav, and button vertically */
        padding: 1rem;
        gap: 1rem;
    }

    .nav-links {
        flex-direction: column;         /* Stacks the links vertically */
        align-items: center;
        width: 100%;
        gap: 1rem;
    }
}