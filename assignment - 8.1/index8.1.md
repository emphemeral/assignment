Here is the complete solution for Assignment 8.1. It provides the HTML structure and CSS styling to build a basic, functional dashboard layout using CSS Grid for both the outer page structure and the inner statistics cards.

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 4: Outer layout container for the CSS Grid -->
    <div class="dashboard-container">

        <!-- Step 1: Create the dashboard header -->
        <header class="header">
            <h2>Dashboard</h2>
            <div class="user-profile">Admin User</div>
        </header>

        <!-- Step 2: Create a sidebar -->
        <aside class="sidebar">
            <nav>
                <ul class="nav-menu">
                    <li><a href="#" class="active">Overview</a></li>
                    <li><a href="#">Analytics</a></li>
                    <li><a href="#">Reports</a></li>
                    <li><a href="#">Settings</a></li>
                </ul>
            </nav>
        </aside>

        <!-- Step 2: Create a main content area -->
        <main class="main-content">
            <h1 class="page-title">Overview</h1>
            
            <!-- Step 3: Add 3 or 4 statistic cards -->
            <div class="stat-cards-container">
                <div class="stat-card">
                    <h3>Total Users</h3>
                    <p class="stat-value">10,245</p>
                    <p class="stat-change positive">+5.2% this week</p>
                </div>
                <div class="stat-card">
                    <h3>Revenue</h3>
                    <p class="stat-value">$45,320</p>
                    <p class="stat-change positive">+8.4% this week</p>
                </div>
                <div class="stat-card">
                    <h3>Active Sessions</h3>
                    <p class="stat-value">1,432</p>
                    <p class="stat-change negative">-1.2% this week</p>
                </div>
                <div class="stat-card">
                    <h3>Bounce Rate</h3>
                    <p class="stat-value">42.3%</p>
                    <p class="stat-change positive">-3.1% this week</p>
                </div>
            </div>
            
            <!-- Placeholder for a chart or table below the cards -->
            <div class="content-panel">
                <h3>Recent Activity</h3>
                <p>Main content area continues here...</p>
            </div>
        </main>

    </div>

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
    background-color: #f0f2f5;
    color: #333;
}

/* =========================================
   OUTER DASHBOARD LAYOUT (Steps 4 & 5)
   ========================================= */
.dashboard-container {
    display: grid;                            /* Step 4: display: grid for outer layout */
    
    /* Step 5: Set grid-template-columns and grid-template-rows */
    grid-template-columns: 250px 1fr;         /* Sidebar is 250px, Main Content takes 1fr (the rest) */
    grid-template-rows: 70px 1fr;             /* Header is 70px, Main Content takes 1fr (remaining height) */
    
    height: 100vh;                            /* Fills the entire viewport height */
}

/* =========================================
   HEADER (Step 1)
   ========================================= */
.header {
    grid-column: 1 / 3;                       /* Forces the header to span across both columns */
    background-color: #ffffff;
    display: flex;                            /* Flexbox used just to align items inside the header */
    justify-content: space-between;
    align-items: center;
    padding: 0 2rem;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    z-index: 10;                              /* Keeps the shadow above other elements */
}

.header h2 {
    color: #2c3e50;
}

.user-profile {
    font-weight: bold;
    color: #3498db;
    cursor: pointer;
}

/* =========================================
   SIDEBAR (Step 2)
   ========================================= */
.sidebar {
    background-color: #2c3e50;
    color: #ffffff;
    padding: 2rem 0;
    /* Automatically sits in row 2, column 1 due to grid flow */
}

.nav-menu {
    list-style: none;
}

.nav-menu li a {
    display: block;
    color: #bdc3c7;
    text-decoration: none;
    padding: 1rem 2rem;
    transition: background-color 0.3s, color 0.3s;
}

.nav-menu li a:hover, .nav-menu li a.active {
    background-color: #34495e;
    color: #ffffff;
    border-left: 4px solid #3498db;
}

/* =========================================
   MAIN CONTENT (Step 2)
   ========================================= */
.main-content {
    padding: 2rem;
    overflow-y: auto;                         /* Allows scrolling if content gets too long */
    /* Automatically sits in row 2, column 2 due to grid flow */
}

.page-title {
    margin-bottom: 2rem;
    color: #2c3e50;
}

/* =========================================
   STATISTIC CARDS (Steps 3 & 6)
   ========================================= */
.stat-cards-container {
    display: grid;                            /* Secondary grid for the cards */
    grid-template-columns: repeat(4, 1fr);    /* Creates 4 equal columns */
    gap: 1.5rem;                              /* Step 6: Use gaps between cards */
    margin-bottom: 2rem;
}

.stat-card {
    background-color: #ffffff;
    padding: 1.5rem;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    transition: transform 0.2s;
}

.stat-card:hover {
    transform: translateY(-5px);
}

.stat-card h3 {
    font-size: 1rem;
    color: #7f8c8d;
    margin-bottom: 0.5rem;
}

.stat-value {
    font-size: 2rem;
    font-weight: bold;
    color: #2c3e50;
    margin-bottom: 0.5rem;
}

.stat-change {
    font-size: 0.85rem;
    font-weight: bold;
}

.stat-change.positive { color: #27ae60; }
.stat-change.negative { color: #e74c3c; }

/* Additional layout block for realism */
.content-panel {
    background-color: #ffffff;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    min-height: 300px;
}

/* Responsive adjustment for smaller screens */
@media screen and (max-width: 1024px) {
    .stat-cards-container {
        grid-template-columns: repeat(2, 1fr); /* Stacks cards 2-by-2 on medium screens */
    }
}
How to complete Step 7 (Inspect the layout):
To finish your assignment, you need to prove you know how to use browser developer tools.

Open your index.html file in a browser (like Chrome, Firefox, or Edge).

Right-click anywhere on the page and select "Inspect" (or press F12).

In the "Elements" tab, find the <div class="dashboard-container"> line.

Look for a tiny "grid" badge next to the word div. Click it!

This will highlight your layout directly on the screen, showing you the exact grid-template-columns (Sidebar and Main Content), grid-template-rows (Header and Main Area), and the gap sizing you defined.