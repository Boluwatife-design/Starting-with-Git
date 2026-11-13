# 1. create a folder

    For example:
    cd Desktop
    mkdir Test
    cd Test
    code .

This opens the project folder in VS Code.

# 2. Create your project files in VS Code
    In VS Code:
    1. Click New File.
    2. Create README.md.
    3. Create system-info.ps1.
Add the following to README.md:

    # PowerShell GitHub Lab
    
    My first project managed using Git and GitHub CLI.
    
    ## Objectives
    - Learn Git version control.
    - Manage repositories through CLI.
    - Publish projects to GitHub.


Add this to system-info.ps1:

    Write-Host "System Information"
    
    Get-ComputerInfo |
    Select-Object WindowsProductName, WindowsVersion, CsName
Save both files.
<img width="1908" height="997" alt="Screenshot 2026-11-13 154122" src="https://github.com/user-attachments/assets/19d14490-acb6-4936-b7f6-a49e32a15ebc" />
<img width="1167" height="659" alt="Screenshot 2026-11-13 153946" src="https://github.com/user-attachments/assets/3dda541f-db37-402e-8765-bdcf96f1c7b2" />

# 3. Open the integrated terminal
Inside VS Code:
- Press Ctrl + ~ (backtick key).
- Click the terminal dropdown.
- Select Command Prompt or PowerShell.
You can execute Git commands directly inside VS Code.

# 4. Continue with Git
Run these commands in your VS Code terminal:

    git init
    
    
    git branch -M main
    
    
    git add .
    
    
    git commit -m "Initial commit"
    
    
    Then authenticate:
    gh auth login
    
    
    Finally, publish:
    gh repo create powershell-github-lab --private --source=. --remote=origin --push

<img width="1410" height="987" alt="Screenshot 2026-11-13 154423" src="https://github.com/user-attachments/assets/bff05de6-424a-405d-91d7-9a5fe248ad11" />

