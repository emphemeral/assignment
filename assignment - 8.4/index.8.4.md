Here is the complete solution for Assignment 8.4. This assignment highlights one of the most powerful combinations in modern web design: using CSS Grid for the macro-layout (the skeleton of the page) and Flexbox for the micro-layout (aligning content inside the individual components).

1. HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grid & Flexbox Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 2: Outer container for the CSS Grid -->
    <div class="dashboard-wrapper">

        <!-- Step 1: Create a sidebar -->
        <aside class="sidebar">
            <div class="brand">DashPro</div>
            <nav class="sidebar-nav">
                <a href="#" class="active">🏠 Dashboard</a>
                <a href="#">👥 Users</a>
                <a href="#">📦 Products</a>
                <a href="#">⚙️ Settings</a>
            </nav>
        </aside>

        <!-- Step 1: Create a header -->
        <header class="header">
            <div class="search-bar">
                <input type="text" placeholder="Search...">
            </div>
            <div class="profile">
                <span>Jane Admin</span>
                <div class="avatar">JA</div>
            </div>
        </header>

        <!-- Step 1: Create the main content area -->
        <main class="main-content">
            <h2 class="page-title">Overview</h2>

            <!-- Step 3: Add 4 statistic cards in the main area -->
            <div class="cards-grid">
                
                <!-- Card 1 -->
                <div class="stat-card">
                    <div class="icon blue">🛒</div>
                    <div class="card-info">
                        <h3>Total Sales</h3>
                        <p class="number">1,245</p>
                    </div>
                </div>

                <!-- Card 2 -->
                <div class="stat-card">
                    <div class="icon green">💰</div>
                    <div class="card-info">
                        <h3>Revenue</h3>
                        <p class="number">$34,500</p>
                    </div>
                </div>

                <!-- Card 3 -->
                <div class="stat-card">
                    <div class="icon orange">👥</div>
                    <div class="card-info">
                        <h3>New Users</h3>
                        <p class="number">328</p>
                    </div>
                </div>

                <!-- Card 4 -->
                <div class="stat-card">
                    <div class="icon purple">📈</div>
                    <div class="card-info">
                        <h3>Conversion</h3>
                        <p class="number">4.6%</p>
                    </div>
                </div>

            </div>

            <!-- Step 5: Add a small table or recent activity section -->
            <section class="recent-activity">
                <h3>Recent Transactions</h3>
                <table class="activity-table">
                    <thead>
                        <tr>
                            <th>Order ID</th>
                            <th>Customer</th>
                            <th>Date</th>
                            <th>Status</th>
                            <th>Amount</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>#ORD-001</td>
                            <td>Michael Scott</td>
                            <td>Oct 18, 2026</td>
                            <td><span class="badge success">Completed</span></td>
                            <td>$250.00</td>
                        </tr>
                        <tr>
                            <td>#ORD-002</td>
                            <td>Dwight Schrute</td>
                            <td>Oct 19, 2026</td>
                            <td><span class="badge pending">Pending</span></td>
                            <td>$1,450.00</td>
                        </tr>
                        <tr>
                            <td>#ORD-003</td>
                            <td>Jim Halpert</td>
                            <td>Oct 19, 2026</td>
                            <td><span class="badge success">Completed</span></td>
                            <td>$75.00</td>
                        </tr>
                    </tbody>
                </table>
            </section>
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
    font-family: 'Segoe UI', system-ui, sans-serif;
}

body {
    background-color: #f3f4f6;
    color: #1f2937;
}

/* =========================================
   MACRO LAYOUT: CSS GRID (Step 2)
   ========================================= */
.dashboard-wrapper {
    display: grid;
    /* Sidebar takes 260px, remaining space goes to the main content */
    grid-template-columns: 260px 1fr;
    /* Header takes 70px, remaining height goes to the main content */
    grid-template-rows: 70px 1fr;
    
    /* Using named areas makes it highly readable */
    grid-template-areas:
        "sidebar header"
        "sidebar main";
    
    height: 100vh;
}

/* Assigning sections to the named grid areas */
.sidebar { grid-area: sidebar; }
.header { grid-area: header; }
.main-content { grid-area: main; }

/* =========================================
   SIDEBAR & HEADER (Grid Item Styling)
   ========================================= */
.sidebar {
    background-color: #111827;
    color: white;
    padding: 1.5rem;
}

.brand {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 2rem;
    color: #60a5fa;
    text-align: center;
    letter-spacing: 1px;
}

.sidebar-nav {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.sidebar-nav a {
    color: #d1d5db;
    text-decoration: none;
    padding: 0.75rem 1rem;
    border-radius: 6px;
    transition: background 0.2s;
}

.sidebar-nav a:hover, .sidebar-nav a.active {
    background-color: #374151;
    color: white;
}

.header {
    background-color: white;
    display: flex; /* Flexbox inside the Grid area to spread out items */
    justify-content: space-between;
    align-items: center;
    padding: 0 2rem;
    box-shadow: 0 1px 3px rgba(0,0,0,0.1);
    z-index: 10;
}

.search-bar input {
    padding: 0.5rem 1rem;
    border: 1px solid #d1d5db;
    border-radius: 20px;
    width: 250px;
}

.profile {
    display: flex;
    align-items: center;
    gap: 1rem;
    font-weight: 500;
}

.avatar {
    background-color: #3b82f6;
    color: white;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}

/* =========================================
   MAIN CONTENT
   ========================================= */
.main-content {
    padding: 2rem;
    overflow-y: auto;
}

.page-title {
    margin-bottom: 1.5rem;
    color: #111827;
}

/* Secondary Grid for the cards wrapper */
.cards-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1.5rem;
    margin-bottom: 2.5rem;
}

/* =========================================
   MICRO LAYOUT: FLEXBOX CARDS (Step 4)
   ========================================= */
.stat-card {
    background-color: white;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    
    /* Step 4: Use Flexbox to align the icon to the left, and info to the right */
    display: flex;
    align-items: center; 
    gap: 1.2rem;
}

.icon {
    font-size: 1.8rem;
    width: 60px;
    height: 60px;
    border-radius: 12px;
    
    /* Flexbox to perfectly center the emoji inside the square box */
    display: flex;
    justify-content: center;
    align-items: center;
}

/* Colored icon backgrounds */
.icon.blue { background-color: #dbeafe; color: #1d4ed8; }
.icon.green { background-color: #dcfce3; color: #15803d; }
.icon.orange { background-color: #ffedd5; color: #c2410c; }
.icon.purple { background-color: #f3e8ff; color: #7e22ce; }

.card-info {
    /* Stack the title and number vertically */
    display: flex;
    flex-direction: column;
}

.card-info h3 {
    font-size: 0.9rem;
    color: #6b7280;
    font-weight: 500;
}

.card-info .number {
    font-size: 1.5rem;
    font-weight: bold;
    color: #111827;
}

/* =========================================
   RECENT ACTIVITY TABLE (Step 5)
   ========================================= */
.recent-activity {
    background-color: white;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}

.recent-activity h3 {
    margin-bottom: 1rem;
    color: #111827;
}

.activity-table {
    width: 100%;
    border-collapse: collapse;
    text-align: left;
}

.activity-table th, .activity-table td {
    padding: 1rem;
    border-bottom: 1px solid #e5e7eb;
}

.activity-table th {
    background-color: #f9fafb;
    color: #4b5563;
    font-weight: 600;
}

.badge {
    padding: 0.25rem 0.75rem;
    border-radius: 9999px;
    font-size: 0.8rem;
    font-weight: bold;
}

.badge.success { background-color: #dcfce3; color: #15803d; }
.badge.pending { background-color: #fef08a; color: #854d0e; }
How to complete Step 6 (Check the layout using the DevTools Grid inspector):
Save the code into index.html and style.css and open the HTML file in Google Chrome, Firefox, or Edge.

Right-click on the background of the page and click "Inspect" (or press F12).

In the Elements panel, look for the <div class="dashboard-wrapper">.

Right next to the word div or class, you will see a small badge that says grid.

Click that grid badge! You will instantly see an overlay on your screen displaying exactly how the browser divided your screen into 260px for the sidebar, 70px for the header, and flexible 1fr spaces for the rest of the layout.

(Optional) You can also find the <div class="stat-card"> elements and click the flex badge next to them to see how Flexbox is positioning the icons and text inside the cards!