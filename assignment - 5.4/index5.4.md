Here is the complete code for your assignment, separated into the HTML structure and the CSS design-token stylesheet.

index.html
This sample webpage implements the variables across headings, cards, and buttons.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Design Tokens Assignment</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Design System Showcase</h1>
  </header>

  <main class="container">
    <article class="card">
      <h2>Standard Card</h2>
      <p>This card uses the medium spacing and standard text sizes defined in our CSS variables.</p>
      <button class="btn btn-primary">Primary Action</button>
    </article>

    <article class="card">
      <h2>Secondary Card</h2>
      <p>This layout applies the secondary color scheme to demonstrate token flexibility.</p>
      <button class="btn btn-secondary">Secondary Action</button>
    </article>
  </main>
</body>
</html>
style.css
This stylesheet defines your design system in the :root pseudo-class and applies those tokens to the webpage elements.

CSS
/* 1-4. Define CSS variables for colors, spacing, and typography */
:root {
  /* Colors */
  --color-primary: #4F46E5;    /* Indigo */
  --color-secondary: #10B981;  /* Emerald */
  --color-bg: #F3F4F6;         /* Light Gray */
  --color-text: #1F2937;       /* Dark Gray */
  --color-card-bg: #FFFFFF;    /* White */

  /* Spacing */
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 32px;

  /* Font Sizes */
  --font-sm: 0.875rem;
  --font-md: 1rem;
  --font-lg: 1.5rem;
  --font-xl: 2rem;
}

/* 5. Use variables in elements (body, headings, cards, buttons) */

/* Base Styles */
body {
  background-color: var(--color-bg);
  color: var(--color-text);
  font-family: system-ui, sans-serif;
  font-size: var(--font-md);
  margin: 0;
  padding: var(--space-lg);
}

h1 {
  font-size: var(--font-xl);
  margin-bottom: var(--space-lg);
  color: var(--color-primary);
}

h2 {
  font-size: var(--font-lg);
  margin-top: 0;
  margin-bottom: var(--space-md);
}

/* Layout */
.container {
  display: flex;
  gap: var(--space-lg);
  flex-wrap: wrap;
}

/* Cards */
.card {
  background-color: var(--color-card-bg);
  padding: var(--space-lg);
  border-radius: var(--space-sm);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  max-width: 300px;
}

.card p {
  margin-bottom: var(--space-md);
  font-size: var(--font-md);
}

/* Buttons */
.btn {
  padding: var(--space-md) var(--space-lg);
  border: none;
  border-radius: var(--space-sm);
  font-size: var(--font-md);
  cursor: pointer;
  font-weight: bold;
  color: #FFFFFF;
}

.btn-primary {
  background-color: var(--color-primary);
}

.btn-secondary {
  background-color: var(--color-secondary);
}
To verify Step 6:
Change the --color-primary variable in your :root block from #4F46E5 to a red hex code like #E11D48. Upon saving and refreshing, you will see both the <h1> text and the Primary Button instantly change to red, confirming that the single token controls multiple elements.