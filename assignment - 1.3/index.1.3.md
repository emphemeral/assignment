Just like the previous assignment, I cannot execute these commands on your computer or take the screenshot for you, but I can provide the exact "record of terminal commands" you need to submit, along with instructions on how to capture your screenshot.

Because terminal commands can contain code, I have formatted this using standard code blocks rather than interactive steps.

Part 1: Record of Terminal Commands for Submission
You can copy and paste the text below into your assignment submission. These commands represent the standard Unix/Bash workflow (used in Mac, Linux, and Git Bash on Windows) which is the industry standard for web development.

Bash
# 1. Create the main project folder
mkdir web-development-practice

# 2. Navigate into the new folder
cd web-development-practice

# 3. Create the three weekly folders inside it
mkdir week-1 week-2 week-3

# 4. Create an index.html file inside each folder
touch week-1/index.html week-2/index.html week-3/index.html

# 5. Practice navigating, renaming, and deleting
mkdir temp-folder           # Create a temporary folder
cd temp-folder              # Navigate into it
cd ..                       # Navigate back out
mv temp-folder old-folder   # Rename the folder
rm -r old-folder            # Delete the folder completely

# 6. Open the project folder in VS Code
code .
(Note: If you are strictly using the default Windows Command Prompt instead of Git Bash or PowerShell, you would use type nul > week-1\index.html instead of touch, ren instead of mv, and rmdir /s instead of rm -r).

Part 2: How to get your Screenshot
To fulfill the visual part of your assignment, you need to show the final folder structure that these commands created.

Open your terminal (Terminal on Mac, or Git Bash / PowerShell on Windows).

Type or paste the commands above one by one, pressing Enter after each line.

When you run the final command (code .), Visual Studio Code will automatically open on your screen with the web-development-practice folder loaded.

In VS Code, look at the Explorer sidebar on the left.

Click the little arrows next to week-1, week-2, and week-3 so they expand to show the index.html file sitting inside each one.

📸 Take a screenshot of your entire VS Code window showing this completed folder structure in the left sidebar.