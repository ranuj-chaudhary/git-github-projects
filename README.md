# 📘 Git Commands Cheat Sheet

Version control ensures **code quality**, **accountability**, and **efficient collaboration** in projects. This guide provides essential Git commands and workflows for beginners and intermediate users.

---

## 🔰 Getting Started

### Step 1: Install Git
- Download and install Git Bash from the official [Git website](https://git-scm.com/).

### Step 2: Initialize a Repository
```bash
git init
```
- Creates a `.git` hidden directory.

### Step 3: Set Default Branch Name
```bash
git branch -M main
```

### Step 4: Configure Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list
```

---

## 📂 Working with Files

### Check File Status
```bash
git status
```

### View Changes
```bash
git diff filename.txt           # Working area
git diff --staged filename.txt # Staging area
```

### Stage Files
```bash
git add filename.ext
git add .                       # Stage all files
```

### Unstage Files
```bash
git reset HEAD filename.ext
```

---

## ✅ Commit Changes

```bash
git commit -m "Your commit message"
git commit -am "Message"  # Add and commit together
```

### Revert a Commit
```bash
git revert <commit-hash>
```

---

## 🔍 Compare Changes

```bash
git diff commit1 commit2
git diff branch1..branch2
git diff branch1..branch2 filename.txt
```

---

## 🧠 Notes on Key Commands

- **reset**: Moves the branch pointer to a different commit (modifies history).
- **restore**: Restores files from index or commit (does not modify history).
- **revert**: Creates a new commit that undoes changes from another commit.

---

## 🛠️ Git Editor

Set VS Code as your Git editor:
```bash
git config --global core.editor "code --wait"
```

---

## 📁 File System Commands (Git Bash)

```bash
pwd                 # Print working directory
ls                  # List directory
cd ..               # Go up a level
cd foldername       # Enter folder
mkdir foldername    # Create directory
touch file1.txt     # Create file(s)
rm filename         # Delete file
rm -rf foldername   # Delete folder
```

---

## 🌐 Remote Repositories

### Add Remote
```bash
git remote add origin git@github.com:User/Repo.git
```

### Change Remote URL
```bash
git remote set-url origin git@github.com:User/Repo.git
```

---

## 🌿 Branching

### Create a Branch
```bash
git branch new-branch
```

### Rename Branch
```bash
git branch -m new-name
```

### Create and Switch
```bash
git switch -c new-branch
```

### Switch Branch
```bash
git switch branch-name
```

### Delete Branch
```bash
git branch -d branch-name
git branch -D branch-name           # Force delete
git push origin --delete branch    # Delete remote branch
```

---

## 🧾 Logs

### View Commit History
```bash
git log
git log --oneline
```

---

## 🔀 Merging

```bash
git checkout main
git merge feature-branch
git merge --abort
```

---

## 📦 Stashing

```bash
git stash                     # Save changes
git stash pop                 # Apply and remove latest stash
git stash list
git stash apply stash@{1}     # Apply specific stash
git stash drop                # Delete stash
```

---

## ⏳ Time Traveling with Git

### Checkout Old Commit
```bash
git checkout <commit-hash>
git checkout HEAD~1
```

### Restore File to Previous State
```bash
git restore filename
git restore --source HEAD~1 filename
```

### Unstage a File
```bash
git restore --staged filename
```

---

## 🧼 Clean Up

### Reset Repository
```bash
git reset <commit-hash>          # Soft
git reset --hard <commit-hash>   # Hard
```

### Clean Untracked Files
```bash
git clean -dfx
```

---

## 🚧 Undo Commits (Collaboration Safe)

```bash
git revert <commit-hash>
```

---

## 📚 Summary: Git Workflow

1. `git init`
2. `git add .`
3. `git commit -m "message"`
4. `git branch feature`
5. `git switch feature`
6. Work & commit
7. `git switch main`
8. `git merge feature`
9. `git push origin main`

---

> Created by **Ranuj Chaudhary**