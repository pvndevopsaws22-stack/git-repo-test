# 1. Install GitHub CLI

# Installs the GitHub CLI using Windows Package Manager (winget)
winget install --id GitHub.cli  

# Verification check: Displays the installed GitHub CLI version to ensure it installed correctly
gh --version

Note: Make sure to close and reopen your PowerShell window after running the installation command.

# 2. Log in to GitHub

# Starts the interactive authentication process to log into your GitHub account
gh auth login
When prompted by the interactive menu, choose the following options:
• GitHub.com
• HTTPS
• Login with a web browser

# 3. Delete Your Repository
# Deletes a specific repository (requires you to type the repository name to confirm)
gh repo delete username/reponame

# Deletes the specific repository named 'sshrepotest' owned by user 'pvn2282' (requires manual confirmation)
gh repo delete pvn2282/sshrepotest

# Forces the deletion of the repository immediately without asking for a confirmation prompt
gh repo delete pvn2282/sshrepotest --yes 

# 4.Create a New GitHub Repository & Push Code
# Creates a new PUBLIC repository named 'repotest', sets the current directory (.) as the source, 
# names the remote 'origin', and automatically pushes all local files to GitHub
gh repo create repotest --public --source=. --remote=origin --push

# Creates a new PRIVATE repository named 'repotest', sets the current directory (.) as the source, 
# names the remote 'origin', and automatically pushes all local files to GitHub
gh repo create repotest --private --source=. --remote=origin --push


