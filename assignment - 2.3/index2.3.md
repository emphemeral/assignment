Part 1: The Updated HTML Code
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Structured Personal Introduction</title>
</head>
<body>

    <!-- Header Section with a custom data-* attribute -->
    <div id="header-section" class="section-container" data-role="hero-banner">
        <h1 class="main-title">Your Full Name</h1>
        <h4 class="subtitle">Aspiring Web Developer | <span class="highlight-text">Creative Problem Solver</span></h4>
        <hr>
    </div>

    <!-- About Me Section -->
    <div id="about-section" class="section-container">
        <h2 class="section-title">About Me</h2>
        <p class="section-text">Hello! I am a dedicated student embarking on an exciting journey into <strong>web development</strong>. I have recently updated this webpage to use clean, structured HTML with proper attributes to better organize my content.</p>
        <hr>
    </div>

    <!-- Education Section -->
    <div id="education-section" class="section-container">
        <h2 class="section-title">Education</h2>
        <h3 class="degree-title">Bachelor of Science in Computer Science</h3>
        <h5 class="school-name">University of Technology | 2023 - Present</h5>
        <p class="section-text">Focusing on software engineering principles, <i>data structures</i>, and modern web technologies.</p>
        <hr>
    </div>

    <!-- Skills Section -->
    <div id="skills-section" class="section-container">
        <h2 class="section-title">Technical & Soft Skills</h2>
        <p class="section-text">
            <strong>Frontend Basics:</strong> HTML5, CSS3<br>
            <strong>Tools & Environment:</strong> VS Code, Git, GitHub, Terminal<br>
            <strong>Soft Skills:</strong> <em>Time Management</em>, Team Collaboration
        </p>
        <hr>
    </div>

    <!-- Contact Section (New Content) -->
    <div id="contact-section" class="section-container">
        <h2 class="section-title">Contact Me</h2>
        <p class="section-text">Feel free to reach out to me for collaboration or questions:</p>
        <p class="contact-info"><strong>Email:</strong> my.email@example.com</p>
        <p class="contact-info"><strong>GitHub:</strong> github.com/yourusername</p>
    </div>

</body>
</html>
Part 2: How to get your Screenshot
To prove that you have successfully structured the page using containers and attributes, the best method is to show the browser's developer tools.

Open your updated index.html page in your web browser using Live Server.

Right-click anywhere on the webpage and select Inspect (or press Ctrl + Shift + I / Cmd + Option + I).

Make sure you are on the Elements tab in the developer tools panel.

Click the small arrows next to the <body> tag to expand it. You will see your nicely stacked <div> containers showing their id, class, and data-role attributes.

📸 Take a screenshot of the browser window that clearly shows this "Elements" panel displaying your structured HTML code.