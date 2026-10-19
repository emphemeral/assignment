1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Auto-Responsive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>My Photo Gallery</h1>
        <p>Resize the browser window to see the grid adjust automatically!</p>
    </header>

    <main>
        <!-- The main CSS Grid container -->
        <div class="gallery-grid">
            
            <!-- Steps 1 & 2: 8 images placed inside gallery items -->
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1015/600/400" alt="River and mountains">
            </div>
            
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1016/600/400" alt="Canyon">
            </div>
            
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1018/600/400" alt="Nature landscape">
            </div>
            
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1025/600/400" alt="Pug wrapped in blanket">
            </div>
            
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1036/600/400" alt="Snowy mountain peak">
            </div>
            
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1039/600/400" alt="Waterfall in forest">
            </div>
            
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1043/600/400" alt="View from a tent">
            </div>
            
            <div class="gallery-item">
                <img src="https://picsum.photos/id/1044/600/400" alt="Foggy valley">
            </div>

        </div>
    </main>

</body>
</html>
2. CSS Styling (style.css)
CSS
/* Basic Reset & Typography */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #121212; /* Dark theme makes photos pop */
    color: #ffffff;
    padding: 2rem;
}

header {
    text-align: center;
    margin-bottom: 3rem;
}

header h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

header p {
    color: #aaaaaa;
}

/* =========================================
   GALLERY GRID (Steps 3 & 5)
   ========================================= */
.gallery-grid {
    display: grid;
    
    /* 
       Step 3: Auto-responsive magic! 
       - auto-fit: Automatically creates as many columns as will fit in the container.
       - minmax(250px, 1fr): Cards will never be smaller than 250px wide. 
         If there is extra space, they will evenly share it (1fr).
    */
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    
    /* Step 5: Keep consistent spacing using gap */
    gap: 1.5rem;
    
    max-width: 1200px;
    margin: 0 auto; /* Centers the grid horizontally */
}

/* =========================================
   GALLERY ITEMS & IMAGES (Step 4)
   ========================================= */
.gallery-item {
    border-radius: 8px;
    overflow: hidden; /* Ensures the image doesn't break out of rounded corners */
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
    background-color: #1e1e1e;
    
    /* Sets a fixed height so all grid items are strictly uniform */
    height: 250px; 
    
    /* Optional: Adding a hover effect */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
}

.gallery-item:hover {
    transform: scale(1.03);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.8);
}

.gallery-item img {
    /* Step 4: Apply width: 100% and suitable object-fit */
    width: 100%;
    height: 100%;
    
    /* 
       object-fit: cover ensures the image fills the 250px height completely
       without stretching or distorting. It crops the image automatically!
    */
    object-fit: cover; 
    display: block;
}
How to complete Step 6 and Submission Instructions:
To finish your assignment and provide the required screenshots:

Verify the Layout (Step 6): Open the index.html file in your web browser. Start with the browser window maximized. You should see 3 or 4 images per row. Slowly drag the edge of your browser window inward to make it narrower. Watch as the images magically resize and automatically drop down to 2 columns, and eventually 1 column on mobile widths—all without writing a single @media query!

Desktop Screenshot: Maximize your browser window and take a screenshot of the multi-column layout.

Mobile Screenshot: Make the browser window narrow (like a phone screen) so the images stack neatly into a single column, and take a screenshot of that view.