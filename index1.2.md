1. Install VS Code and Node.js
Visual Studio Code: Go to code.visualstudio.com, download the installer for your operating system, and run it.

Node.js: Go to nodejs.org and download the LTS (Long Term Support) version. Run the installer and accept all the default settings (this ensures npm is installed alongside Node.js).

Note: Restart your computer after installing Node.js so your terminal recognizes the new commands.

2. Install Extensions in VS Code
Open VS Code and click the Extensions icon on the left sidebar (or press Ctrl+Shift+X on Windows / Cmd+Shift+X on Mac).

Search for Live Server (by Ritwick Dey) and click Install.

Search for Prettier - Code formatter (by Prettier) and click Install.

3. Create Your Workspace and Files
Create a new folder on your computer named web-development-practice.

Drag and drop this folder into your open VS Code window, or go to File > Open Folder and select it.

In the VS Code Explorer panel (left side), click the "New File" icon to create these three files: index.html, style.css, and script.js.

Paste the following basic code into your files so you have something visible for your final browser screenshot:

index.html

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Dev Practice</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>My Development Environment is Ready!</h1>
    <script src="script.js"></script>
</body>
</html>
style.css

CSS
body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin-top: 50px;
    background-color: #f4f4f9;
}
script.js

JavaScript
console.log("Environment setup successfully!");
4. Verify Node.js (Capture Screenshot 1)
In VS Code, open the integrated terminal by going to Terminal > New Terminal in the top menu (or press Ctrl+`).

Type the following command and press Enter:

Bash
node -v
Next, type this command and press Enter:

Bash
npm -v
Take your first screenshot: Capture the VS Code terminal panel showing the version numbers that print out (e.g., v20.x.x and 10.x.x).

5. Run Live Server (Capture Screenshots 2 & 3)
Open your index.html file in VS Code.

Right-click anywhere inside the HTML code and select Open with Live Server (alternatively, click the "Go Live" button at the very bottom right of the VS Code window).

This will automatically open your default web browser to a local address (usually [http://127.0.0.1:5500/index.html](http://127.0.0.1:5500/index.html)) displaying your page.

Take your second screenshot: Capture your entire VS Code window showing your code, the file explorer, and your installed extensions.

Take your third screenshot: Capture the web browser window showing your rendered HTML page.