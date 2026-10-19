Step 1: Set Up Your Project Folder
Before writing the code, you need to create the correct file structure on your computer so the image paths work properly.

Create a main folder for this assignment (e.g., assignment-3.2).

Inside that folder, create a new file named portfolio.html.

Inside the same main folder, create a new subfolder named images.

Find 3 images on your computer (or download some) and place them inside the images folder. For this example, rename them to project1.jpg, project2.jpg, and project3.jpg (or .png depending on your file types).

Step 2: The HTML Code
Copy this code and paste it into your portfolio.html file. Make sure the filenames in the src attributes exactly match the images you saved in your folder.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
</head>
<body>

    <h1>My Portfolio Projects</h1>
    <p>Welcome to my visual portfolio. Below are screenshots of my recent work:</p>

    <hr>

    <!-- Project 1 -->
    <section>
        <h2>1. Weather Application</h2>
        <p>A simple app that fetches the current forecast.</p>
        <!-- Notice the src points to the images folder, and alt is highly descriptive -->
        <img src="images/project1.jpg" alt="Screenshot of a mobile weather application displaying a sunny 72-degree forecast" width="500" height="300">
    </section>

    <!-- Project 2 -->
    <section>
        <h2>2. E-Commerce Storefront</h2>
        <p>A mock clothing store built with HTML and CSS.</p>
        <img src="images/project2.jpg" alt="A mock e-commerce clothing website showing a grid of t-shirt product cards" width="500" height="300">
    </section>

    <!-- Project 3 -->
    <section>
        <h2>3. Personal Blog</h2>
        <p>My daily coding journal.</p>
        <img src="images/project3.jpg" alt="Homepage of a personal web development blog with dark mode enabled" width="500" height="300">
    </section>

</body>
</html>
Step 3: Test and Submit
Verify the Paths: Double-click your portfolio.html file to open it in your browser.

Check for Broken Images: If you see broken image icons, double-check that your images are actually inside the images folder, and that the file extensions (like .jpg vs .png) match your code exactly.

Check Alt Text: If an image fails to load, the alt text should appear. This text is critical for visually impaired users relying on screen readers.

Prepare Submission: Compress (zip) your entire main folder (which contains both portfolio.html and the images folder) and submit it according to your course instructions.