Open the terminal
macOS: Terminal / Windows: Git Bash or PowerShell
Open your command line interface. If you are on Windows and don't have Git Bash, open PowerShell.

2
Create and navigate to the main folder
Use the mkdir (make directory) command to create the root folder, then cd (change directory) to move inside it.

Bash
mkdir web-development-practice
cd web-development-practice
3
Create the weekly subfolders
You can create multiple folders at once by separating their names with a space.

Bash
mkdir week-1 week-2 week-3
4
Create the index.html files
Windows PowerShell users: replace 'touch' with 'ni'
The touch command creates empty files. You can target the inside of each folder directly from where you are.

Bash
touch week-1/index.html week-2/index.html week-3/index.html
5
Practice navigating, renaming, and deleting
To fulfill step 5 of your assignment safely without destroying your work, let's create a temporary folder, move into it, step back out, rename it, and finally delete it.

Bash
# 1. Create a practice folder
mkdir practice-folder

# 2. Navigate into it, then navigate back out (..)
cd practice-folder
cd ..

# 3. Rename the folder using mv (move)
mv practice-folder delete-me-later

# 4. Delete the folder using rm -r (remove recursively)
rm -r delete-me-later
6
Open the project in VS Code
The code . command tells your terminal to open Visual Studio Code in your current directory (.).

Bash
code .

Bash
mkdir web-development-practice
cd web-development-practice
mkdir week-1 week-2 week-3
touch week-1/index.html week-2/index.html week-3/index.html
mkdir practice-folder
cd practice-folder
cd ..
mv practice-folder delete-me-later
rm -r delete-me-later
code .
For the screenshot: Once VS Code opens, click the "Explorer" icon on the top left sidebar to expand your folders. Take a screenshot showing web-development-practice with the three week folders and their respective index.html files nested inside.

Having trouble with 'code .' not working?

Yes