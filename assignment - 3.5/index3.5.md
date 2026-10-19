Here is the complete solution for Assignment 3.5. This project uses two HTML files (index.html and projects.html) connected by a working navigation bar to fulfill all the requirements.

File 1: index.html (Home, About, Skills, Links)
Copy this code and save it as index.html in your project folder.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio - Home</title>
</head>
<body>

    <!-- Header and Navigation -->
    <header>
        <h1>Alex Dev Portfolio</h1>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="projects.html">My Projects</a> | 
            <a href="https://github.com" target="_blank" rel="noopener noreferrer">GitHub Profile</a>
        </nav>
    </header>

    <hr>

    <main>
        <!-- About Me Section -->
        <section id="about">
            <h2>About Me</h2>
            <p>Hello! I am a passionate web developer learning to build accessible, semantic, and highly functional websites. I enjoy solving problems and bringing creative ideas to life through code.</p>
        </section>

        <!-- Skills Section using a list -->
        <section id="skills">
            <h2>Technical Skills</h2>
            <ul>
                <li>Semantic HTML5</li>
                <li>CSS3 & Responsive Design</li>
                <li>Version Control (Git/GitHub)</li>
                <li>Web Accessibility Basics</li>
            </ul>
        </section>

        <!-- Useful Links Section -->
        <section id="links">
            <h2>Useful Links</h2>
            <ul>
                <li><a href="https://developer.mozilla.org" target="_blank" rel="noopener noreferrer">MDN Web Docs</a></li>
                <li><a href="https://www.w3.org" target="_blank" rel="noopener noreferrer">W3C Standards</a></li>
            </ul>
        </section>
    </main>

    <hr>

    <!-- Footer with contact details -->
    <footer>
        <h2>Contact Me</h2>
        <p>Email: <a href="mailto:alex@example.com">alex@example.com</a></p>
        <p>&copy; 2026 Alex Dev. All rights reserved.</p>
    </footer>

</body>
</html>
File 2: projects.html (Blog Posts / Projects with Images)
Save this as projects.html in the exact same folder as your index.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio - Projects</title>
</head>
<body>

    <!-- Header and Navigation -->
    <header>
        <h1>Alex Dev Portfolio</h1>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="projects.html">My Projects</a> | 
            <a href="https://github.com" target="_blank" rel="noopener noreferrer">GitHub Profile</a>
        </nav>
    </header>

    <hr>

    <main>
        <section id="portfolio">
            <h2>Recent Projects & Blog Posts</h2>
            <p>Here are some of the things I have been working on recently.</p>

            <!-- Project 1 inside an article tag -->
            <article>
                <h3>1. HTML Foundations Website</h3>
                <img src="images/project-html.jpg" alt="Screenshot of a basic HTML webpage with a white background" width="400" height="250">
                <p>This project demonstrates my ability to structure web pages using raw HTML5, semantic tags, and accessible image alt text.</p>
            </article>

            <hr>

            <!-- Project 2 inside an article tag -->
            <article>
                <h3>2. Accessibility Audit Blog</h3>
                <img src="images/project-blog.jpg" alt="A laptop screen displaying a web accessibility testing tool" width="400" height="250">
                <p>A blog post detailing how I used semantic HTML elements to improve the screen-reader experience of a legacy website.</p>
            </article>
        </section>
    </main>

    <hr>

    <footer>
        <h2>Contact Me</h2>
        <p>Email: <a href="mailto:alex@example.com">alex@example.com</a></p>
        <p>&copy; 2026 Alex Dev. All rights reserved.</p>
    </footer>

</body>
</html>
Setup and Submission Instructions
Set Up the Folder: Create a folder named Portfolio-Project. Inside, save both index.html and projects.html.

Add Images: Inside that folder, create an images subfolder. Add two images named project-html.jpg and project-blog.jpg (or update the code to match the names of images you already have).

Test Locally: Open index.html in your browser. Click the "My Projects" link to ensure it navigates to the second page, and verify the images load correctly.

Push to GitHub:

Initialize Git in your folder: git init

Add files: git add .

Commit: git commit -m "Complete final portfolio mini-project"

Push to a new GitHub repository following the same steps you used in Assignment 2.5.

Submit: Zip your Portfolio-Project folder and submit it along with your newly created GitHub repository link.