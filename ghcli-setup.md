## 1. Install GitHub CLI

```powershell
# Installs the GitHub CLI using Windows Package Manager (winget)
winget install --id GitHub.cli  

# Verification check: Displays the installed GitHub CLI version to ensure it installed correctly
gh --version
```

> **Note:** Make sure to close and reopen your PowerShell window after running the installation command.

---

## 2. Log in to GitHub

```powershell
# Starts the interactive authentication process to log into your GitHub account
gh auth login
```

When prompted by the interactive terminal menu, select the following choices:
*   `GitHub.com`
*   `HTTPS`
*   `Login with a web browser`

---

## 3. Delete Your Repository

```powershell
# Deletes a specific repository (requires you to type the repository name to confirm)
gh repo delete username/reponame

# Deletes the specific repository named 'repo-test' owned by user 'pvn22' (requires manual confirmation)
gh repo delete pvn22/repo-test

# Forces the deletion of the repository immediately without asking for a confirmation prompt
gh repo delete pvn22/repo-test --yes 
```

---

## 4. Create a New GitHub Repository & Push Code

```powershell
# Creates a new PUBLIC repository named 'repotest', sets the current directory (.) as the source, 
# names the remote 'origin', and automatically pushes all local files to GitHub
gh repo create repotest --public --source=. --remote=origin --push

# Creates a new PRIVATE repository named 'repotest', sets the current directory (.) as the source, 
# names the remote 'origin', and automatically pushes all local files to GitHub
gh repo create repotest --private --source=. --remote=origin --push
```

---

## 5. Rename Repository & Update Configuration

```powershell
# Renames the GitHub repository 'repo-test' to your new desired name 'git-commands-handbook'
gh repo rename git-commands-handbook --repo pvndevopsaws22-stack/repo-test

# Updates your local 'origin' to the new repository URL
git remote set-url origin https://github.com/pvndevopsaws22-stack/git-commands-handbook.git

# Verification check: Run this to confirm the URL changed successfully
git remote -v

# Push your current branch to the newly renamed remote repository
git push -u origin main
```