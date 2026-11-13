# Step 1: Check if Git is installed
Open your terminal (PowerShell, CMD, or Git Bash) and run:

    git --version

If Git is installed, you'll see something similar to:

    git version 2.x.x

If you get an error saying Git is not recognized, download and install it:
Download Git for Windows

    https://git-scm.com/install/windows

During installation, the default options are fine for now.

run 

    git --version again

you should see this: <img width="501" height="282" alt="image" src="https://github.com/user-attachments/assets/a75313ac-1291-43c4-869b-cffa4b26712f" />

# Step 2: Configure your Git identity
Git needs to know who is making commits.

Run these commands, replacing the details with your GitHub name and email:

    git config --global user.name "Your Name"
    
    
    git config --global user.email "your-github-email@example.com"
    
    
Verify your configuration:

    git config --global --list

These settings identify you in your Git commit history. They don't authenticate you to GitHub.
<img width="805" height="389" alt="Screenshot 2026-11-13 120214" src="https://github.com/user-attachments/assets/e07b5064-dfe3-4861-af33-333a6d6ccdb2" />


# Step 3: Authenticate with GitHub
I recommend using GitHub CLI (gh) because it makes authentication and repository management easier.

    run : winget install --id GitHub.cli on cmd to install

<img width="476" height="87" alt="image" src="https://github.com/user-attachments/assets/688b25f2-ccf2-4f60-a548-de77871487b8" />


