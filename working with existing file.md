# Step 1: Get your repository URL
  1. Open your repository on GitHub.
  2. Click the green Code button.
  3. Select HTTPS.
  4. Copy the repository URL.
  It should look something like:

    https://github.com/username/repository-name.git
<img width="1610" height="869" alt="Screenshot 2026-11-13 122120" src="https://github.com/user-attachments/assets/01f7fb76-7064-40e1-8381-95f0380e67be" />


# Step 2: Clone the repository
- Open PowerShell or Git Bash and navigate to where you want to store your projects.

      For example:
      cd Desktop
      mkdir GitHub
      cd GitHub
  
- Now clone your repository:

      git clone https://github.com/username/repository-name.git
<img width="947" height="334" alt="Screenshot 2026-11-13 122329" src="https://github.com/user-attachments/assets/eaac54e8-bd08-4078-855e-d0fa3d7a51c3" />

# Step 3: Enter the repository

    cd repository-name
- Check its status:

      git status
- See the files:

      use ls or dir depending on the terminal you are using

<img width="687" height="529" alt="Screenshot 2026-11-13 122429" src="https://github.com/user-attachments/assets/ef0af44c-ce84-4729-9891-4438c0db6ffd" />

# Step 4: Start working
- You can now open the project in VS Code:

      code .
- Make your changes, save your files, then push them:

      git add .
      git commit -m "Updated project files"
      git push

## Note: You don't need VS Code to work with GitHub from your CLI.

You can use PowerShell, CMD, or Git Bash to manage your repositories, create files, edit code and push changes.

You have two options:
### Option 1: Work directly from your terminal
You can:
- Clone repositories.
- Create files and folders.
- Edit files using Notepad.
- Run scripts.
- Commit and push changes.
For example, to open a file using Notepad:

      notepad README.md

### Option 2: Install VS Code (recommended)

- Free code editor with an integrated terminal and Git support.

Download: Official VS Code website : https://code.visualstudio.com/

- You can use VS Code's integrated terminal to execute Git commands without switching applications.
