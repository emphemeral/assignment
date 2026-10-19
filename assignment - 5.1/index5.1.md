index.html
To link the stylesheet, add the <link> tag inside your <head> section. Replace the content inside the <body> with your actual Week 4 HTML.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled Website</title>
    <!-- Step 2: Link the external stylesheet -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Navigation section -->
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>

    <!-- Main content -->
    <main>
        <h1>Welcome to My Website</h1>
        <h2>About This Project</h2>
        <p>This paragraph demonstrates the text styling, line height, and font family settings. You can click this <a href="https://example.com" target="_blank">sample link</a> to see the inline link styles.</p>
    </main>
</body>
</html>
style.css
Create this file in the same folder as your HTML file.

CSS
/* Step 3: Set body background, text color, and font */
body {
    background-color: #f4f4f9;
    color: #333333;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
}

/* Step 4: Style headings, paragraphs, and links */
h1, h2, h3, h4, h5, h6 {
    color: #2c3e50;
    margin-bottom: 10px;
}

p {
    line-height: 1.6;
    margin-bottom: 15px;
    padding: 0 20px;
}

/* General inline links */
a {
    color: #007bff;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
    color: #0056b3;
}

/* Step 5: Make navigation links readable and attractive */
nav {
    background-color: #2c3e50;
    padding: 15px 20px;
    text-align: center;
}

nav a {
    color: #ffffff;
    font-size: 18px;
    font-weight: bold;
    margin: 0 15px;
    padding: 5px 10px;
    text-transform: uppercase;
    transition: color 0.3s ease;
}

nav a:hover {
    color: #f1c40f;
    text-decoration: none;
}
Step 6: Inspect styles using Chrome DevTools
To verify your styles are applying correctly, open your index.html file in Google Chrome, right-click anywhere on the page, and select Inspect. Use the Elements tab to click on your HTML elements and view or temporarily tweak the CSS rules in the Styles pane on the right.