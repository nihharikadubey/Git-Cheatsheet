# 🧠 Git Cheatsheet

A complete guide to using Git for pushing your Jenkins Shared Library project to GitHub, managing remotes, handling conflicts, and rewriting commit messages.

---

## 📁 Initialize Local Git Repo

```bash
cd ~/Documents/DevOps/cursor/Jenkins_SharedLib
git init



⸻

📦 Add, Commit & Push to GitHub

git add .
git commit -m "Initial commit"
git remote add origin https://github.com/nihharikadubey/Jenkins_Shared_Library.git
git branch -M main
git push -u origin main



⸻

🔁 Fixing Remote Conflicts

❌ If remote already exists

git remote remove origin
git remote add origin https://github.com/nihharikadubey/Jenkins_Shared_Library.git

🔄 If push fails due to remote changes

git pull origin main --rebase
git push origin main



⸻

📂 Add Additional vars/ Scripts (e.g., from another repo)

# After copying new .groovy files to vars/
git add vars/
git commit -m "Added additional shared steps from LondheShubham153's library"
git push origin main



⸻

✏️ Update Last Commit Message

git commit --amend -m "Updated commit message for clarity"
git push --force origin main



⸻

🛠️ Reword Multiple Past Commits (Advanced)

git rebase -i HEAD~3   # Replace 3 with number of commits to go back
# Change 'pick' to 'reword' for the commits you want to rename
git push --force origin main



⸻

✅ Note: Use --force push carefully. Only recommended when you’re the sole contributor or understand the implications.

⸻

