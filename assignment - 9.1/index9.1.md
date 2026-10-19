Here is the complete solution for Assignment 9.1. We will use the Dashboard/Gallery from Week 8, but this time we are completely flipping the approach to Mobile-First.

Instead of building for a large screen and using max-width to strip things away, we will build the stacked mobile view as the default CSS, and use min-width media queries to add the complex grid layout as the screen gets larger.

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- Step 2: The viewport meta tag is CRITICAL for mobile responsiveness -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mobile-First Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="app-container">
        
        <header class="header">
            <div class="logo">MobileFirst.</div>
            <!-- Hamburger menu icon for mobile (visual only for this demo) -->
            <div class="menu-icon">☰</div>
        </header>

        <aside class="profile-section">
            <img src="https://via.placeholder.com/80" alt="Profile" class="avatar">
            <h2>Alex Designer</h2>
            <p>Digital Artist</p>
        </aside>

        <main class="main-content">
            <h1>Recent Work</h1>
            
            <div class="gallery">
                <img src="https://picsum.photos/id/1015/600/400" alt="Nature 1" class="card">
                <img src="https://picsum.photos/id/1018/600/400" alt="Nature 2" class="card">
                <img src="https://picsum.photos/id/1025/600/400" alt="Nature 3" class="card">
                <img src="https://picsum.photos/id/1036/600/400" alt="Nature 4" class="card">
            </div>
        </main>

        <footer class="footer">
            <p>&copy; 2026 MobileFirst Studio.</p>
        </footer>

    </div>

</body>
</html>
2. CSS Styling (style.css)
CSS
/* =========================================
   BASE STYLES (Step 3: Mobile First!)
   ========================================= */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; /* Step 7: Prevents padding from causing horizontal overflow */
    font-family: 'Segoe UI', system-ui, sans-serif;
}

body {
    background-color: #f8f9fa;
    color: #333;
    /* Step 7: Final safety net against horizontal scrolling on mobile */
    overflow-x: hidden; 
}

/* Default Mobile Layout: Everything stacks vertically */
.app-container {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.header {
    background-color: #111827;
    color: white;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-weight: bold;
    font-size: 1.25rem;
}

.menu-icon {
    font-size: 1.5rem;
    cursor: pointer;
}

.profile-section {
    background-color: white;
    padding: 2rem 1rem;
    text-align: center;
    border-bottom: 1px solid #e5e7eb;
}

.avatar {
    border-radius: 50%;
    margin-bottom: 0.5rem;
}

.main-content {
    padding: 1.5rem 1rem;
    flex-grow: 1; /* Pushes footer down */
}

.main-content h1 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
}

/* Mobile Gallery: 1 column */
.gallery {
    display: grid;
    grid-template-columns: 1fr;
    gap: 1rem;
}

.card {
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    object-fit: cover;
}

.footer {
    background-color: #e5e7eb;
    text-align: center;
    padding: 1rem;
    font-size: 0.875rem;
}

/* =========================================
   BREAKPOINT 1: TABLETS (Step 4 & 5)
   ========================================= */
@media screen and (min-width: 768px) {
    /* Upgrading the gallery to 2 columns for tablets */
    .gallery {
        grid-template-columns: repeat(2, 1fr);
        gap: 1.5rem;
    }

    .main-content {
        padding: 2rem;
    }
}

/* =========================================
   BREAKPOINT 2: DESKTOPS (Step 4 & 5)
   ========================================= */
@media screen and (min-width: 1024px) {
    
    /* Completely transform the layout into a CSS Grid Dashboard */
    .app-container {
        display: grid;
        grid-template-columns: 250px 1fr;
        grid-template-rows: 70px 1fr auto;
        grid-template-areas:
            "sidebar header"
            "sidebar main"
            "sidebar footer";
    }

    /* Assigning areas */
    .header { grid-area: header; }
    .profile-section { grid-area: sidebar; border-right: 1px solid #e5e7eb; border-bottom: none; }
    .main-content { grid-area: main; }
    .footer { grid-area: footer; }

    /* Adjusting elements for desktop context */
    .menu-icon {
        display: none; /* Hide the hamburger menu on desktop */
    }

    .profile-section {
        padding-top: 3rem;
    }

    /* Upgrading the gallery to an auto-responsive grid */
    .gallery {
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    }
}
How to complete Step 6 and Submission Instructions:
To get your screenshots using Chrome DevTools Device Mode:

Open index.html in Google Chrome.

Right-click the page and select Inspect (or press F12).

Click the Device Toggle icon (it looks like a phone next to a tablet) at the top-left of the Developer Tools panel, or press Ctrl+Shift+M (Windows) / Cmd+Shift+M (Mac).

Use the dropdown menu at the top of the browser to select different devices:

Mobile Screenshot: Select iPhone SE or Pixel 7. You will see the stacked, single-column layout.

Tablet Screenshot: Select iPad Mini. You will see the 2-column grid trigger from the first breakpoint.

Desktop Screenshot: Turn off device mode and maximize your browser window. You will see the full sidebar and main-content dashboard layout trigger from the second breakpoint.