Here is the complete solution for Assignment 3.1. You will need to create two separate HTML files in the same folder on your computer.

File 1: index.html (The Home Page)
Copy this code and save it as index.html. It includes the website name, an introduction, the navigation bar, and the external link with the required security attributes.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home - My Two-Page Website</title>
</head>
<body>

    <!-- Navigation Bar -->
    <nav>
        <a href="index.html">Home</a> | 
        <a href="about.html">About</a>
    </nav>

    <hr>

    <!-- Main Content: Name and Introduction -->
    <main>
        <h1>My Two-Page Website</h1>
        <p>Welcome to my home page! This website is a simple demonstration of how to connect multiple HTML pages together using navigation links.</p>

        <!-- External Link with target and rel attributes -->
        <p>Want to learn more about coding? Visit the 
            <a href="https://developer.mozilla.org/" target="_blank" rel="noopener noreferrer">MDN Web Docs</a>.
        </p>
    </main>

</body>
</html>
File 2: about.html (The About Page)
Copy this code and save it as about.html in the exact same folder as your index.html file. This ensures the links can find each other.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About - My Two-Page Website</title>
</head>
<body>

    <!-- Navigation Bar -->
    <nav>
        <a href="index.html">Home</a> | 
        <a href="about.html">About</a>
    </nav>

    <hr>

    <!-- Main Content -->
    <main>
        <h1>About This Site</h1>
        <p>This is the second page of my website. By clicking the "Home" link above, you will be taken right back to the main index page!</p>
    </main>

</body>
</html>
How to Prepare Your Submission:
Test the Links: Double-click your saved index.html file to open it in your web browser (like Chrome or Safari).

Verify Functionality:

Click the About link to make sure it goes to the second page.

Click the Home link to make sure it comes back.

Click the MDN Web Docs link to verify it opens in a new tab securely.

Take a Screenshot: While viewing the website in your browser, take a screenshot showing the page and the navigation bar.

Submit: Zip your index.html and about.html files together, and upload them along with your screenshot to complete your assignment!