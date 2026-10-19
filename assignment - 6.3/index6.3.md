Here is the complete code to demonstrate the four CSS overflow properties and how to fix a common layout break caused by overflowing content.

index.html
This file creates four fixed-size boxes loaded with excess text to test the overflow states, plus a dedicated section showing a broken layout and its fixed counterpart.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Overflow Demonstrations</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <h1>Overflow & Layout Fixing</h1>
    <p>Testing visible, hidden, scroll, and auto properties.</p>
  </header>

  <main>
    <!-- Steps 1-4: Demonstrating Overflow Values -->
    <section class="overflow-grid">
      
      <!-- Visible: Spills out of the box -->
      <div class="box box-visible">
        <h2>1. Visible (Default)</h2>
        <p>This text is intentionally very long to force an overflow. Because the overflow property is set to visible, the text will spill completely out of this container and overlap with surrounding elements, ignoring the box's height constraint entirely.</p>
      </div>

      <!-- Hidden: Cuts off -->
      <div class="box box-hidden">
        <h2>2. Hidden</h2>
        <p>This text is intentionally very long to force an overflow. Because the overflow property is set to hidden, the text that exceeds the container's boundaries is simply cut off and invisible to the user.</p>
      </div>

      <!-- Scroll: Forces scrollbars -->
      <div class="box box-scroll">
        <h2>3. Scroll</h2>
        <p>This text is intentionally very long to force an overflow. With the scroll property, the browser forces scrollbars to appear on both the X and Y axes, regardless of whether they are actually needed.</p>
      </div>

      <!-- Auto: Smart scrollbars -->
      <div class="box box-auto">
        <h2>4. Auto</h2>
        <p>This text is intentionally very long to force an overflow. The auto property is the smartest option—it only adds a scrollbar if the content actually exceeds the container's boundaries. Otherwise, it remains clean.</p>
      </div>
    </section>

    <!-- Step 5: Identify and Fix a Layout Issue -->
    <section class="fix-demo">
      <h2>Step 5: Layout Fixing Demonstration</h2>
      <p>A common issue occurs when a single, unbroken string of text (like a URL) exceeds the width of its parent container, breaking the layout horizontally.</p>
      
      <div class="demo-container">
        <!-- The Broken Version -->
        <div class="layout-box broken-layout">
          <h3>Broken Horizontal Overflow</h3>
          <p class="long-word">Supercalifragilisticexpialidocious_ThisStringIsTooLongToFitInsideItsContainer</p>
        </div>

        <!-- The Fixed Version -->
        <div class="layout-box fixed-layout">
          <h3>Fixed Layout</h3>
          <p class="long-word fixed-text">Supercalifragilisticexpialidocious_ThisStringIsTooLongToFitInsideItsContainer</p>
        </div>
      </div>
    </section>
  </main>

</body>
</html>
style.css
This stylesheet enforces the fixed height on the containers to trigger the overflow behavior and applies the specific fixes for Step 5.

CSS
/* Base Reset */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: system-ui, sans-serif;
  background-color: #f8fafc;
  color: #334155;
  padding: 40px 20px;
}

header {
  text-align: center;
  margin-bottom: 50px;
}

/* --- Steps 1-4: Overflow Grid --- */
.overflow-grid {
  display: flex;
  gap: 30px;
  flex-wrap: wrap;
  justify-content: center;
  margin-bottom: 60px;
}

/* Step 1: Container with a fixed height and width */
.box {
  width: 250px;
  height: 150px;
  background: #ffffff;
  border: 2px solid #3b82f6; /* Blue border */
  border-radius: 8px;
  padding: 15px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}

.box h2 {
  font-size: 1.1rem;
  margin-bottom: 10px;
  color: #1d4ed8;
}

.box p {
  font-size: 0.9rem;
  line-height: 1.5;
}

/* Step 3 & 4: Applying overflow rules */
.box-visible { overflow: visible; }
.box-hidden  { overflow: hidden; }
.box-scroll  { overflow: scroll; }
.box-auto    { overflow: auto; }


/* --- Step 5: Layout Fixing Demo --- */
.fix-demo {
  max-width: 700px;
  margin: 0 auto;
  background: #ffffff;
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}

.fix-demo > p {
  margin-bottom: 20px;
  color: #64748b;
}

.demo-container {
  display: flex;
  gap: 20px;
}

.layout-box {
  flex: 1;
  padding: 15px;
  border-radius: 8px;
  /* Fixed width to force the horizontal overflow issue */
  width: 100%;
  max-width: 300px; 
}

.broken-layout {
  border: 2px solid #ef4444; /* Red border for broken */
  background: #fef2f2;
}

.fixed-layout {
  border: 2px solid #10b981; /* Green border for fixed */
  background: #ecfdf5;
}

.layout-box h3 {
  font-size: 1rem;
  margin-bottom: 10px;
}

.long-word {
  background: #e2e8f0;
  padding: 5px;
  font-family: monospace;
  font-size: 0.85rem;
}

/* THE FIX: Forces long unbroken text strings to wrap to the next line 
   instead of overflowing the container horizontally. */
.fixed-text {
  overflow-wrap: break-word;
  word-break: break-all;
}
For your submission screenshot: Open index.html in your browser. The first box (Visible) will show text bleeding out of the bottom border. Take a screenshot of the page, ensuring you capture both the grid of four boxes and the green "Fixed Layout" box at the bottom.