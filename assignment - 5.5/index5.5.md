Design Choices Explanation
For this college Coding Club website, I selected a modern tech-inspired palette using midnight blue for structure, vibrant cyan for interactive elements, and an off-white background to reduce eye strain. I utilized system sans-serif fonts to ensure a clean, highly readable typography scale across all devices. CSS variables centralize these design tokens, guaranteeing consistency while making the styles easily reusable and maintainable. Forms and tables are heavily padded with subtle borders to prioritize user accessibility and clear data presentation.

index.html (Home & Schedule)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>College Coding Club | Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header class="site-header">
    <div class="container header-flex">
      <div class="logo">{" />"} Coding Club</div>
      <nav class="main-nav">
        <ul>
          <li><a href="index.html" class="active">Home</a></li>
          <li><a href="contact.html">Join Us</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <h1>Build, Hack, and Learn Together</h1>
      <p>Join the largest community of student developers on campus. Whether you're writing your first "Hello World" or deploying full-stack apps, there's a place for you here.</p>
      <a href="contact.html" class="btn btn-primary">Become a Member</a>
    </section>

    <section class="schedule">
      <h2>Upcoming Events</h2>
      <table>
        <thead>
          <tr>
            <th>Date</th>
            <th>Event Name</th>
            <th>Location</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Oct 24</td>
            <td>Intro to React.js</td>
            <td>Lab 302</td>
          </tr>
          <tr>
            <td>Nov 2</td>
            <td>Fall Hackathon</td>
            <td>Student Center</td>
          </tr>
          <tr>
            <td>Nov 15</td>
            <td>Alumni Tech Panel</td>
            <td>Auditorium B</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <p>&copy; 2026 College Coding Club. All rights reserved.</p>
    </div>
  </footer>

</body>
</html>
contact.html (Join Form)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>College Coding Club | Join Us</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header class="site-header">
    <div class="container header-flex">
      <div class="logo">{" />"} Coding Club</div>
      <nav class="main-nav">
        <ul>
          <li><a href="index.html">Home</a></li>
          <li><a href="contact.html" class="active">Join Us</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="form-section">
      <h1>Join the Club</h1>
      <p>Fill out the form below to get added to our mailing list and Discord server.</p>
      
      <form action="#" method="POST" class="contact-form">
        <div class="form-group">
          <label for="name">Full Name</label>
          <input type="text" id="name" name="name" required placeholder="Jane Doe">
        </div>
        
        <div class="form-group">
          <label for="email">Student Email</label>
          <input type="email" id="email" name="email" required placeholder="jane@college.edu">
        </div>
        
        <div class="form-group">
          <label for="experience">Coding Experience</label>
          <select id="experience" name="experience">
            <option value="beginner">Beginner</option>
            <option value="intermediate">Intermediate</option>
            <option value="advanced">Advanced</option>
          </select>
        </div>

        <div class="form-group">
          <label for="message">Why do you want to join?</label>
          <textarea id="message" name="message" rows="4" placeholder="I want to learn web development..."></textarea>
        </div>

        <button type="submit" class="btn btn-primary">Submit Application</button>
      </form>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <p>&copy; 2026 College Coding Club. All rights reserved.</p>
    </div>
  </footer>

</body>
</html>
style.css (External Stylesheet)
CSS
/* 1. CSS Variables (Design Tokens) */
:root {
  /* Colors */
  --clr-primary: #0ea5e9;       /* Cyan */
  --clr-primary-hover: #0284c7; /* Darker Cyan */
  --clr-dark: #0f172a;          /* Midnight Blue */
  --clr-light: #f8fafc;         /* Off-white */
  --clr-gray: #64748b;          /* Slate */
  --clr-border: #e2e8f0;        /* Light Slate */

  /* Typography */
  --font-main: system-ui, -apple-system, sans-serif;
  
  /* Spacing */
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 2rem;
  --space-xl: 4rem;

  /* Borders */
  --radius: 6px;
}

/* 2. Resets & Base Styles */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: var(--font-main);
  background-color: var(--clr-light);
  color: var(--clr-dark);
  line-height: 1.6;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.container {
  width: 90%;
  max-width: 1000px;
  margin: 0 auto;
}

/* Typography */
h1, h2, h3 {
  line-height: 1.2;
  margin-bottom: var(--space-md);
  color: var(--clr-dark);
}

h1 { font-size: 2.5rem; }
h2 { font-size: 1.75rem; }
p { margin-bottom: var(--space-md); color: var(--clr-gray); }

/* 3. Navigation */
.site-header {
  background-color: var(--clr-dark);
  color: white;
  padding: var(--space-md) 0;
}

.header-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: var(--clr-primary);
}

.main-nav ul {
  list-style: none;
  display: flex;
  gap: var(--space-lg);
}

.main-nav a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.main-nav a:hover, .main-nav a.active {
  color: var(--clr-primary);
}

/* Layout */
main {
  flex-grow: 1;
  padding: var(--space-xl) 0;
}

.hero {
  text-align: center;
  margin-bottom: var(--space-xl);
}

/* Buttons */
.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: var(--radius);
  text-decoration: none;
  font-weight: 600;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-primary {
  background-color: var(--clr-primary);
  color: white;
}

.btn-primary:hover {
  background-color: var(--clr-primary-hover);
}

/* 4. Tables */
table {
  width: 100%;
  border-collapse: collapse;
  background: white;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  border-radius: var(--radius);
  overflow: hidden;
}

th, td {
  padding: var(--space-md);
  text-align: left;
  border-bottom: 1px solid var(--clr-border);
}

th {
  background-color: var(--clr-dark);
  color: white;
  font-weight: 600;
}

tr:last-child td {
  border-bottom: none;
}

/* 5. Forms */
.form-section {
  max-width: 600px;
  margin: 0 auto;
  background: white;
  padding: var(--space-lg);
  border-radius: var(--radius);
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
}

.form-group {
  margin-bottom: var(--space-md);
}

label {
  display: block;
  margin-bottom: var(--space-sm);
  font-weight: 600;
  color: var(--clr-dark);
}

input, select, textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid var(--clr-border);
  border-radius: var(--radius);
  font-family: inherit;
  font-size: 1rem;
}

input:focus, select:focus, textarea:focus {
  outline: none;
  border-color: var(--clr-primary);
  box-shadow: 0 0 0 2px rgba(14, 165, 233, 0.2);
}

/* Footer */
.site-footer {
  text-align: center;
  padding: var(--space-lg) 0;
  background-color: var(--clr-dark);
  color: var(--clr-gray);
  margin-top: auto;
}