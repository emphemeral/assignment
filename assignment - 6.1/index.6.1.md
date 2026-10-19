index.html
This HTML structure creates three distinct cards to demonstrate how different box model properties affect an element's total size and spacing.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Model Inspection</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <h1>CSS Box Model Demonstration</h1>
    <p>Inspect these cards in DevTools to see how padding, borders, and margins interact.</p>
  </header>

  <main class="container">
    <!-- Card 1: Standard Border-Box -->
    <div class="card box-1">
      <h2>Card 1: Border-Box</h2>
      <p>This card uses <code>box-sizing: border-box</code>. The 300px width includes the padding and the border.</p>
    </div>

    <!-- Card 2: Content-Box -->
    <div class="card box-2">
      <h2>Card 2: Content-Box</h2>
      <p>This card uses <code>box-sizing: content-box</code> (default). The 300px width only applies to the content, making the total box wider once padding and borders are added.</p>
    </div>

    <!-- Card 3: Extreme Spacing -->
    <div class="card box-3">
      <h2>Card 3: Heavy Spacing</h2>
      <p>This card has exaggerated margins, thick borders, and heavy padding to make the box model clearly visible in DevTools.</p>
    </div>
  </main>

</body>
</html>
style.css
This stylesheet applies different box-sizing rules, paddings, borders, and margins to highlight the structural differences between the three cards.

CSS
/* Base Reset */
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: system-ui, sans-serif;
  background-color: #f4f4f5;
  color: #333;
  padding: 20px;
}

header {
  text-align: center;
  margin-bottom: 40px;
}

.container {
  display: flex;
  flex-direction: column;
  gap: 20px;
  align-items: center;
}

/* Base Card Styles */
.card {
  background-color: #ffffff;
  /* All cards share a base width of 300px to demonstrate sizing differences */
  width: 300px; 
}

/* Box 1: Border-Box (Modern Standard) */
.box-1 {
  box-sizing: border-box;
  padding: 20px;
  border: 5px solid #3b82f6; /* Blue */
  margin: 10px;
}

/* Box 2: Content-Box (Legacy Default) 
   Even though width is 300px, actual rendered width is 300 + 20(L-pad) + 20(R-pad) + 5(L-border) + 5(R-border) = 350px */
.box-2 {
  box-sizing: content-box;
  padding: 20px;
  border: 5px solid #ef4444; /* Red */
  margin: 10px;
}

/* Box 3: Exaggerated Box Model for easy DevTools inspection */
.box-3 {
  box-sizing: border-box;
  padding: 40px;
  border: 15px dashed #10b981; /* Green */
  margin: 50px;
}

h2 {
  font-size: 1.25rem;
  margin-bottom: 10px;
}

p {
  font-size: 0.9rem;
  line-height: 1.5;
  color: #555;
}
Box Model Annotation Guide
To complete the assignment's visual requirement, right-click any of the cards in your browser, select "Inspect", and navigate to the "Computed" tab in DevTools (usually on the right side of the elements panel). You will see a nested diagram representing the following layers:

Content (Innermost Blue Box): The actual space taken up by the text (the <h2> and <p>). In content-box (Card 2), the 300px width applies strictly to this area. In border-box (Cards 1 & 3), this area shrinks to accommodate the padding and border.

Padding (Green Area): The inner breathing room between the text (content) and the border. Background colors extend into this area.

Border (Yellow Area): The structural line wrapping the padding. In Card 3, this is the 15px dashed green line.

Margin (Orange Outermost Box): The invisible external space pushing this card away from other elements. Background colors do not extend into the margin.