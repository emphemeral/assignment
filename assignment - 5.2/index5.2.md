index.html

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Selectors Practice</title>
    <!-- Links the external stylesheet -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>CSS Selectors Assignment</h1>
        <h2>Understanding the Cascade</h2>
    </header>

    <!-- Specific section using an ID -->
    <section id="special-section">
        <h3>Important Notice</h3>
        <!-- Element with conflicting CSS rules -->
        <p class="text-conflict">This paragraph tests CSS specificity and cascade rules. What color will it be?</p>
        <p>This is a standard paragraph inside the special section.</p>
    </section>

    <!-- Multiple sections using a class -->
    <main>
        <div class="card">
            <h3>Feature One</h3>
            <p>This is the first feature card.</p>
        </div>
        <div class="card">
            <h3>Feature Two</h3>
            <p>This is the second feature card.</p>
        </div>
    </main>
</body>
</html>
style.css

CSS
/* 5. Universal selector: Applies to every element on the page */
* {
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 0;
}

/* 6. Grouping selector: Applies the same style to multiple different elements */
h1, h2, h3 {
    margin-bottom: 10px;
    color: #333333;
}

/* 2. Element selector: Targets all <p> and <body> tags globally */
body {
    padding: 20px;
    background-color: #f9f9f9;
}

p {
    line-height: 1.6;
    margin-bottom: 15px;
}

/* 4. ID selector: Targets the single specific #special-section element */
#special-section {
    background-color: #e0f7fa;
    border-left: 5px solid #00acc1;
    padding: 20px;
    margin-bottom: 20px;
}

/* 3. Class selector: Targets all elements with the .card class */
.card {
    background-color: #ffffff;
    border: 1px solid #dddddd;
    border-radius: 5px;
    padding: 15px;
    margin-bottom: 15px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

/* 7. Conflicting CSS rules (Cascade and Specificity) */

/* Rule A: Class selector (Specificity: 0, 1, 0) */
.text-conflict {
    color: green;
    font-weight: bold;
}

/* Rule B: ID + Class selector (Specificity: 1, 1, 0) */
#special-section .text-conflict {
    color: red; 
}
Explanation of Selectors Used
Universal Selector (*): Used to reset margins and padding across all elements and establish a global box-sizing rule, ensuring consistent layout dimensions across the browser.

Element Selector (body, p): Used to set baseline styles for standard HTML tags, such as the global background color and default paragraph line height.

Class Selector (.card): Applied to multiple <div> elements to give them an identical visual "card" styling (borders, background, shadow) without repeating code.

ID Selector (#special-section): Used to uniquely identify and style the highlighted notice area. It applies a specific background and left border only to that single section.

Grouping Selector (h1, h2, h3): Combines multiple heading elements into a single comma-separated rule to give them consistent bottom margins and text color efficiently.

Conflicting Rules (Cascade & Specificity): The .text-conflict paragraph is targeted by two rules. Rule A (class only) tells the text to be green. Rule B (ID + class) tells the text to be red. The text will render as red. Even though Rule A is a valid instruction, Rule B includes an ID (#special-section), which gives it a mathematically higher specificity weight than a standalone class.