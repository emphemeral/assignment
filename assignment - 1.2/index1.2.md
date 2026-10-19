Because this assignment requires installing software and setting up a local environment on your personal machine, I cannot perform the actions or take the screenshots for you. Here is the exact step-by-step walkthrough to complete the setup and capture your required submission files.

1. Install the Core Software
Visual Studio Code: Go to code.visualstudio.com and download the installer for your operating system. Run the installer using all the default settings.

Node.js: Go to nodejs.org and download the version marked LTS (Long Term Support). Run the installer and accept all default prompts.

2. Install VS Code Extensions
Open Visual Studio Code.

Click the Extensions icon in the left sidebar (it looks like four blocks, with one pulling away).

In the search bar, type Live Server (by Ritwick Dey) and click Install.

Clear the search, type Prettier - Code formatter (by Prettier), and click Install.

3. Create the Project Workspace
Create a new folder anywhere on your computer (like your Desktop) and name it web-development-practice.

Open VS Code, click File > Open Folder in the top menu, and select the folder you just created.

Hover over your folder name in the Explorer pane on the left, and click the New File icon to create these three exact files: index.html, style.css, and script.js.

Open index.html, type ! and press Enter (this generates a basic HTML starter template).

Add <h1>Environment Setup Complete!</h1> inside the <body> tags so you have something to look at, and save the file (Ctrl + S on Windows or Cmd + S on Mac).

📸 Take Screenshot 1: Take a screenshot of your entire VS Code window showing your opened project folder and the files on the left sidebar.

4. Verify Node.js via Terminal
Inside VS Code, open the integrated terminal by clicking Terminal > New Terminal in the top menu (or pressing Ctrl + `).

Type node -v and press Enter.

Type npm -v and press Enter.

You should see version numbers printed out on the screen (e.g., v20.x.x and 10.x.x).

📸 Take Screenshot 2: Take a screenshot of the bottom terminal panel showing these version numbers.

5. Run Live Server
Make sure you still have index.html open and selected in VS Code.

Right-click anywhere inside the code editor and select Open with Live Server (or click the "Go Live" button at the very bottom right corner of the VS Code window).

Your default web browser will automatically open and display your HTML page at an address like [http://127.0.0.1:5500/index.html](http://127.0.0.1:5500/index.html).

📸 Take Screenshot 3: Take a screenshot of your web browser showing the running webpage and the URL bar.