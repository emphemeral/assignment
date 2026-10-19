This code acts as the "After" version of your webpage. It replaces a generic div-heavy layout with proper semantic tags, ensuring the page is accessible for screen readers and search engines.

The Semantic HTML Code
Copy this code and save it as semantic-blog.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic Tech Blog</title>
</head>
<body>

    <!-- Header and Navigation -->
    <header>
        <h1>Tech Insights Blog</h1>
        <nav>
            <a href="#home">Home</a> |
            <a href="#articles">Articles</a> |
            <a href="#about">About</a> |
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <hr>

    <!-- Main Content Area -->
    <main>

        <!-- The primary article -->
        <article>
            <h2>The Power of Semantic HTML</h2>
            <p>By <strong>Jane Developer</strong> - Published on October 19, 2026</p>
            
            <!-- Image with meaningful alt text for accessibility -->
            <img src="images/semantic-code.jpg" alt="A laptop screen displaying cleanly formatted HTML5 tags" width="600" height="400">
            
            <p>Semantic HTML introduces meaning to the web page rather than just presentation. Tags like <code>&lt;article&gt;</code>, <code>&lt;section&gt;</code>, and <code>&lt;aside&gt;</code> help screen readers and search engines understand the structure of your content.</p>
            <p>When you replace meaningless <code>&lt;div&gt;</code> tags with descriptive elements, you improve both accessibility and SEO.</p>
        </article>

        <hr>

        <!-- A distinct section within the main content -->
        <section>
            <h3>Related Articles</h3>
            <ul>
                <li><a href="#css">Mastering CSS Flexbox</a></li>
                <li><a href="#a11y">A Beginner's Guide to Web Accessibility</a></li>
            </ul>
        </section>

    </main>

    <hr>

    <!-- Aside for secondary content (like a sidebar) -->
    <aside>
        <h2>About the Author</h2>
        <!-- Profile image with descriptive alt text -->
        <img src="images/author-profile.jpg" alt="Headshot of Jane Developer smiling outdoors" width="150" height="150">
        <p>Jane is a front-end developer passionate about accessible web design. She loves sharing her knowledge with the community.</p>
    </aside>

    <hr>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Tech Insights Blog. All rights reserved.</p>
        <!-- Footer navigation -->
        <nav>
            <a href="#privacy">Privacy Policy</a> | <a href="#terms">Terms of Service</a>
        </nav>
    </footer>

</body>
</html>
How to Prepare Your Submission:
Set Up Your Images: Create an images folder in the same directory as your HTML file and add two placeholder images named semantic-code.jpg and author-profile.jpg (or change the code to match images you already have).

Take the "Before" Screenshot: If your instructor provided a broken or div-based starting file, open that original file in your browser and take a screenshot. If they didn't provide one, just take a screenshot of an empty or unstyled text document to represent the "before" state.

Take the "After" Screenshot: Open your new semantic-blog.html file in your browser and take a clear screenshot showing how the structured content renders.

Submit: Upload your updated semantic-blog.html file along with the "before" and "after" screenshots.