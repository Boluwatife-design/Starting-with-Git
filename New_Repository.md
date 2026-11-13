# Step 1. Create your project directory
Run:
  
    cd $HOME\Documents
- Create a folder:

      mkdir powershell-github-lab

- Enter the folder:

      cd powershell-github-lab

- Check your current location:

      Get-Location
You should be inside:

    C:\Users\YourUsername\Documents\powershell-github-lab

# Step 2. Create your project files
Let's create a README file to document the project.

    New-Item README.md -ItemType File

- Create a PowerShell script:

      New-Item system-info.ps1 -ItemType File

- Open the README:
notepad README.md


      Add this content:
      # PowerShell GitHub Lab
      
      My first project managed through Windows PowerShell
      and published to GitHub using GitHub CLI.
      
      ## Project Contents
      
      - README.md: Project documentation
      - system-info.ps1: PowerShell system information script
      
      ## Objective
      
      Learn Git, GitHub CLI, version control and repository management.
      
      
      Save and close Notepad.
      
      Now open your script:
      notepad system-info.ps1
      
      
      Add:
      Write-Host "System Information"
      
      Get-ComputerInfo |
      Select-Object WindowsProductName, WindowsVersion, CsName
      
      
      Save and close.

- Your folder should now contain:
  
      powershell-github-lab/
      │
      ├── README.md
      └── system-info.ps1


- You have just created your first local project.
Phase 4: Initialize Git

# Step 3. Initialize your repository
    Run:
    git init

- This creates a hidden .git directory inside your project folder.

- That directory contains Git's version-control information.

- Set your default branch to main:

    git branch -M main


- Check the status:

      git status


You would see your two files listed as untracked.

# Step 4. Stage your files
## Tell Git which files you want to track:

    git add .

- Check the status again:

      git status

- Your files would now appear under changes to be committed.
  
# Step 5. Commit your changes
## A commit is a snapshot of your project at a particular point in time.

    Run:
    git commit -m "Initial commit: Create PowerShell project"

- You would receive a confirmation showing the files added.

      Check your commit history:
      git log --oneline
      
      
      Your first commit should appear.
      Phase 5: Publish your project to GitHub
      This is where your local project becomes an actual GitHub repository.

# Step 6. Create the remote GitHub repository
First, decide whether your repository should be public or private.
- Public: Anyone can view your code.
- Private: Only you and people you authorize can access it.
I recommend starting with Private while you're learning.

      Run:
      gh repo create powershell-github-lab --private --source=. --remote=origin --push
      Parameter	Meaning
      gh repo create	Create a GitHub repository
      powershell-github-lab	Repository name
      --private	Make it private
      --source=.	Use the current directory
      --remote=origin	Name the remote connection origin
      --push	Upload your local commits

- Expected result
- GitHub CLI would create the repository, configure the remote, and push your commit.
- You can also make it public by replacing --private with --public.
- This single command handles the repository creation and initial publishing. 
- Take GitHub to the command line+1

# Step 7. Verify your repository
- Check your remote connection:

      git remote -v
You should see your GitHub repository URL for both fetch and push.

- Check the repository details:

      gh repo view


-Open it in your browser:

      gh repo view --web
      
      You should now see:
      - Your repository name.
      - Your README documentation.
      - Your PowerShell script.
      - Your initial commit.

Phase 6: Learn the everyday workflow
Once your repository exists, this is the workflow you'll use whenever you modify your project.

- Imagine you update system-info.ps1 with another feature.

      Run:
      git status
      
      
      See what changed:
      git diff
      
      
      Stage your changes:
      git add .
      
      
      Commit:
      git commit -m "Improve system information script"
      
      
      Push:
      git push
      
      
      Your latest changes will be uploaded to GitHub.



Phase 7: Important things to know
Before publishing real projects, develop these habits:

      1. Never upload secrets
      
      Don't commit:
      - Passwords.
      - API keys.
      - Access tokens.
      - Private SSH keys.
      - Database credentials.
      2. Use .gitignore
      
      Create a file:
      New-Item .gitignore -ItemType File
      
      
      Add common exclusions:
      .env
      *.log
      __pycache__/
      .vscode/
      
      
      This tells Git which files to ignore.

### Understand these commands
Command	Purpose
- git init	Initialize Git
- git add .	Stage changes
- git commit	Save a snapshot
- git push	Upload changes
- git pull	Download and integrate changes
- git clone	Copy a remote repository
- git branch	Manage branches
- git checkout -b	Create and switch branches
- git status	Check working state
