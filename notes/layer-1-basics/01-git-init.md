# 01 — `git init`

---

## 🎯 Technical Definition 

> `git init` initializes a new, empty Git repository in the current working directory by creating a hidden `.git/` subdirectory. This `.git/` folder contains all the metadata, object storage, and configuration Git needs to track the history, branches, and state of the project. Without it, Git has no awareness of the directory whatsoever.

---

## 📌 What I Did

1. Created a folder on my PC called `git-learning-lab`
2. Opened Git Bash
3. Navigated into the folder using `cd`
4. Ran `git init`

---

## ❓ Why I Did It

I already had a folder on my PC.
To make Git start tracking it, I had to tell Git —
*"this folder is now a repository."*
That is exactly what `git init` does.

---

## 💻 Command I Ran

```bash
cd git-learning-lab
git init
```

---

## 📤 Output I Got

```
Initialized empty Git repository in /c/Users/Sasi/git-learning-lab/.git/
```

---

## 🗂️ What Gets Created — The `.git/` Folder

```
.git/
├── HEAD          ← Points to current branch (default: main)
├── config        ← Repo-level Git configuration
├── description   ← Used by GitWeb (ignore for now)
├── hooks/        ← Scripts that run on Git events (advanced)
├── info/         ← Exclude patterns (like .gitignore but local)
├── objects/      ← Where ALL your file data and commits are stored
└── refs/         ← Pointers to branches and tags
```

> 💡 This `.git/` folder **IS** the repository.
> Delete it → Git forgets everything. Your files stay, history gone.

---

## 🧠 What I Understood

- A normal folder and a Git repository look the same from outside
- `git init` is what makes the difference — it adds the `.git/` folder
- I am literally telling Git *"start watching this folder from now"*
- Git does not track anything automatically before `git init`

---

## 🔁 When to Use `git init` vs `git clone`

| Situation | Command |
|---|---|
| Folder exists on my PC, starting fresh | `git init` |
| Repo already exists on GitHub | `git clone <url>` |
| Created repo on GitHub first | `git clone <url>` — no init needed |

> `clone` already brings `.git/` with it. Never run `git init` inside a cloned repo.

---

## 😅 What Confused Me

I thought I needed `git init` even when cloning from GitHub.

## ✅ How I Resolved It

`git clone` creates the `.git/` folder automatically.
`git init` is only for folders that have **never** been a Git repo before.

---

## ⚡ One Line to Remember

> *"git init tells Git — this folder is yours now, start watching."*

---

**Layer:** 🟢 Layer 1 — Local Basics  
**Practice:** 1.1  
**Date:** May 2026  
**Author:** Sasi Kiran
