Here is the complete solution for Assignment 8.5. For this final mini-project, we are building a Portfolio Dashboard that incorporates an image gallery. This layout uses everything you've learned: grid-template-areas for the macro-layout (the whole page structure) and an auto-responsive repeat(auto-fit, minmax(...)) grid for the micro-layout (the photo gallery).

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Mini-Project</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- PRIMARY LAYOUT: Outer Grid Container -->
    <div class="app-layout">

        <!-- HEADER SECTION -->
        <header class="header">
            <div class="logo">GridFolio.</div>
            <nav class="nav-menu">
                <a href="#">Home</a>
                <a href="#">Galleries</a>
                <a href="#">Settings</a>
            </nav>
        </header>

        <!-- SIDEBAR SECTION -->
        <aside class="sidebar">
            <div class="profile-card">
                <img src="https://via.placeholder.com/100" alt="Profile Picture" class="profile-img">
                <h2>Alex Designer</h2>
                <p>Digital Artist & Photographer</p>
                <div class="stats">
                    <div><strong>142</strong><span>Posts</span></div>
                    <div><strong>8k</strong><span>Followers</span></div>
                </div>
                <button class="btn">Upload Photo</button>
            </div>
        </aside>

        <!-- MAIN GRID LAYOUT -->
        <main class="main-content">
            <h1 class="page-title">Recent Uploads</h1>
            
            <!-- MULTIPLE CARDS/IMAGES GRID -->
            <div class="gallery-grid">
                
                <!-- Card 1 -->
                <article class="gallery-card">
                    <div class="img-wrapper">
                        <img src="https://picsum.photos/id/1015/600/400" alt="River">
                    </div>
                    <div class="card-details">
                        <h3>Mountain River</h3>
                        <p>Landscape Photography</p>
                    </div>
                </article>

                <!-- Card 2 -->
                <article class="gallery-card">
                    <div class="img-wrapper">
                        <img src="https://picsum.photos/id/1018/600/400" alt="Nature">
                    </div>
                    <div class="card-details">
                        <h3>Forest Trail</h3>
                        <p>Nature</p>
                    </div>
                </article>

                <!-- Card 3 -->
                <article class="gallery-card">
                    <div class="img-wrapper">
                        <img src="https://picsum.photos/id/1025/600/400" alt="Pug">
                    </div>
                    <div class="card-details">
                        <h3>Cozy Pug</h3>
                        <p>Animals</p>
                    </div>
                </article>

                <!-- Card 4 -->
                <article class="gallery-card">
                    <div class="img-wrapper">
                        <img src="https://picsum.photos/id/1036/600/400" alt="Snow">
                    </div>
                    <div class="card-details">
                        <h3>Winter Peaks</h3>
                        <p>Landscape Photography</p>
                    </div>
                </article>

                <!-- Card 5 -->
                <article class="gallery-card">
                    <div class="img-wrapper">
                        <img src="https://picsum.photos/id/1039/600/400" alt="Waterfall">
                    </div>
                    <div class="card-details">
                        <h3>Hidden Waterfall</h3>
                        <p>Nature</p>
                    </div>
                </article>

                <!-- Card 6 -->
                <article class="gallery-card">
                    <div class="img-wrapper">
                        <img src="https://picsum.photos/id/1044/600/400" alt="Valley">
                    </div>
                    <div class="card-details">
                        <h3>Misty Valley</h3>
                        <p>Cinematic</p>
                    </div>
                </article>

            </div>
        </main>

        <!-- FOOTER SECTION -->
        <footer class="footer">
            <p>&copy; 2026 GridFolio Photography. All rights reserved.</p>
        </footer>

    </div>

</body>
</html>
2. CSS Styling (style.css)
CSS
/* Basic Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f3f4f6;
    color: #333;
}

/* =========================================
   RULE 1 & 3: CSS GRID WITH NAMED AREAS
   ========================================= */
.app-layout {
    display: grid;
    min-height: 100vh; /* Fills full screen height */
    
    /* Defines a 300px sidebar, and 1 fraction for the rest */
    grid-template-columns: 300px 1fr;
    /* Defines heights for Header, Main, and Footer */
    grid-template-rows: 70px 1fr auto; 

    /* Drawing the macro-layout map */
    grid-template-areas:
        "header header"
        "sidebar main"
        "sidebar footer";
}

/* Assigning the HTML elements to the named Grid Areas */
.header       { grid-area: header; }
.sidebar      { grid-area: sidebar; }
.main-content { grid-area: main; }
.footer       { grid-area: footer; }

/* =========================================
   HEADER & FOOTER
   ========================================= */
.header {
    background-color: #111827;
    color: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2rem;
    z-index: 10;
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: #3b82f6;
}

.nav-menu a {
    color: #d1d5db;
    text-decoration: none;
    margin-left: 1.5rem;
    font-weight: 500;
}

.nav-menu a:hover {
    color: #fff;
}

.footer {
    background-color: #fff;
    text-align: center;
    padding: 1.5rem;
    border-top: 1px solid #e5e7eb;
    color: #6b7280;
    font-size: 0.9rem;
}

/* =========================================
   SIDEBAR
   ========================================= */
.sidebar {
    background-color: #fff;
    border-right: 1px solid #e5e7eb;
    padding: 2rem;
}

.profile-card {
    text-align: center;
}

.profile-img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 1rem;
    border: 3px solid #3b82f6;
}

.profile-card h2 {
    font-size: 1.2rem;
    margin-bottom: 0.25rem;
}

.profile-card p {
    color: #6b7280;
    font-size: 0.9rem;
    margin-bottom: 1.5rem;
}

.stats {
    display: flex;
    justify-content: space-around;
    margin-bottom: 2rem;
}

.stats div {
    display: flex;
    flex-direction: column;
}

.stats strong {
    font-size: 1.25rem;
    color: #111827;
}

.stats span {
    font-size: 0.8rem;
    color: #6b7280;
}

.btn {
    width: 100%;
    background-color: #3b82f6;
    color: #fff;
    border: none;
    padding: 0.75rem;
    border-radius: 6px;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s;
}

.btn:hover {
    background-color: #2563eb;
}

/* =========================================
   MAIN CONTENT & GALLERY GRID (RULE 2)
   ========================================= */
.main-content {
    padding: 2rem;
}

.page-title {
    margin-bottom: 1.5rem;
    color: #111827;
}

.gallery-grid {
    display: grid;
    /* Rule 2: Using repeat(), minmax(), and 1fr */
    /* This creates auto-responsive columns that wrap automatically! */
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem; /* Consistent gaps */
}

/* =========================================
   CARDS (RULE 4: Prevent overflow)
   ========================================= */
.gallery-card {
    background-color: #fff;
    border-radius: 10px;
    overflow: hidden; /* Prevents images from breaking out of rounded corners */
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    transition: transform 0.2s, box-shadow 0.2s;
}

.gallery-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 15px rgba(0,0,0,0.1);
}

.img-wrapper {
    height: 200px;
    width: 100%;
}

.img-wrapper img {
    width: 100%;
    height: 100%;
    object-fit: cover; /* Prevents image distortion and overflow */
    display: block;
}

.card-details {
    padding: 1rem;
}

.card-details h3 {
    font-size: 1.1rem;
    margin-bottom: 0.25rem;
    white-space: nowrap;     /* Rule 4: Text overflow prevention */
    overflow: hidden;
    text-overflow: ellipsis; 
}

.card-details p {
    color: #6b7280;
    font-size: 0.9rem;
}

/* =========================================
   RULE 5: TEST ON DIFFERENT WIDTHS
   ========================================= */
/* Change layout for tablets and mobile devices */
@media screen and (max-width: 900px) {
    .app-layout {
        grid-template-columns: 1fr; /* Switch from 2 columns to 1 column */
        
        /* Redraw the entire layout map for smaller screens! */
        grid-template-areas:
            "header"
            "sidebar"
            "main"
            "footer";
    }

    .sidebar {
        border-right: none;
        border-bottom: 1px solid #e5e7eb;
    }

    .nav-menu {
        display: none; /* Hide navigation on small screens for simplicity */
    }
}
Final Submission Steps:
Test Your Work (Rule 5): Open the index.html file in your browser. View it on full screen to see the Dashboard Layout (sidebar on the left, gallery on the right). Then, make the browser window narrow. You'll see the layout seamlessly snap into a single column (grid-template-areas doing its magic), and the gallery cards shrink down properly without overflowing.

Push to GitHub:

Save the code in index.html and style.css in a folder.

Open GitHub Desktop or your terminal.

Create a new repository, commit these files, and push them to GitHub.

Submit: Copy the URL to your GitHub repository and submit it for Assignment 8.5!