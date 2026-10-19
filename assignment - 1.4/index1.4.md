Part 1: Terminal Commands to Run
First, ensure you have downloaded and installed Git from git-scm.com. Then, open your terminal (or Git Bash on Windows) in your project folder and run these commands one by one.

(Make sure to replace "Your Name" and "your.email@example.com" with your actual details).

Bash
# 1. Verify Git installation
git --version

# 2. Configure your Git identity (only needs to be done once per computer)
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# 3. Initialize the Git repository in your current folder
git init

# 4. Create an HTML file
touch index.html

# 5. Check status, add, and make Commit #1
git status
git add index.html
git commit -m "Initial commit: create blank index.html"

# 6. Make a change and create Commit #2
echo "<h1>Hello Git!</h1>" > index.html
git add index.html
git commit -m "Add main heading to index.html"

# 7. Make another change and create Commit #3
echo "<p>Learning version control today.</p>" >> index.html
git add index.html
git commit -m "Add description paragraph to index.html"

# 8. View your commit history (This is for your screenshot)
git log --oneline
Part 2: How to get your Screenshots
📸 Screenshot 1: The Repository Folder
To prove this is a Git repository, you need to show the hidden .git folder.

Open your project folder in your computer's normal file explorer (File Explorer on Windows or Finder on Mac).

On Windows: Click the View tab at the top and check the box that says Hidden items.
On Mac: Press Cmd + Shift + . (period) to reveal hidden files.

You should now see a faded folder named .git sitting next to your index.html file. Take a screenshot of this folder window.

📸 Screenshot 2: The History of Three Commits

Look back at your terminal where you ran the commands.

The final command you ran (git log --oneline) will output a neat list of the three commits you just made, complete with their generated ID hashes and your messages.

Take a screenshot of the terminal window clearly showing this git log output.