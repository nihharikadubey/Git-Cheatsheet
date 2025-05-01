# Git-Cheatsheet
Git-Cheatsheet

cd ~/Documents/DevOps/cursor/Jenkins_SharedLib        # Navigate to your shared lib project
git init                                               # Initialize Git repository
git add .                                              # Stage all files
git commit -m "Initial commit"                         # First commit
git remote add origin https://github.com/nihharikadubey/Jenkins_Shared_Library.git
git branch -M main                                     # Rename branch to main (standard)
git push -u origin main                                # Push to GitHub




🧾 Git Cheatsheet: Pushing Jenkins Shared Library to GitHub

**🔧 Initialize Local Git Repo
**

cd ~/Documents/DevOps/cursor/Jenkins_SharedLib
git init

🧺 Add + Commit + Push to Your GitHub Repo

git add .
git commit -m "Initial commit"

Create a new repository on your GitHub account
Repository: https://github.com/nihharikadubey/Jenkins_Shared_Library.git

Add your GitHub repo as the new remote:
git remote add origin https://github.com/nihharikadubey/Jenkins_Shared_Library.git
git branch -M main
git push -u origin main



⸻

🔁 Fixing Remote Conflicts

❌ If remote already exists:

git remote remove origin
git remote add origin https://github.com/nihharikadubey/Jenkins_Shared_Library.git

❌ If push fails due to remote changes:

git pull origin main --rebase
git push origin main



⸻

🧩 Add Additional vars/ Scripts (e.g. from another repo)

# Copy .groovy files to vars/
git add vars/
git commit -m "Added additional shared steps from LondheShubham153's library"
git push origin main



⸻

✏️ Change Last Commit Message

git commit --amend -m "Added shared Groovy steps to Jenkins Shared Library"
git push --force origin main



⸻

🛠️ Optional: Rebase to Edit Multiple Past Commits

git rebase -i HEAD~3       # Change 3 to however many commits back you want to edit
# Change 'pick' to 'reword' for desired commits
git push --force origin main

