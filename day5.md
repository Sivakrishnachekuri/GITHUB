TOPICS :
=================

✅ Branches vs Tags

🧳 Git Stash

♻️ Git Restore


## 🔀 Git Branch vs 🔖 Git Tag 
=======================================================

| Feature           | Branches                          | Tags                                      |
|-------------------|-----------------------------------|-------------------------------------------|
| **Purpose**        | For active development             | To mark a specific point in history (e.g. v1.0) |
| **Moves with Commits** | Yes                            | No – stays fixed to one commit            |
| **Mutable?**       | Yes, you can keep changing it     | No, unless forced                         |
| **Use Case**       | Working on new features, fixes    | Marking releases, stable versions         |
| **Create**         | `git branch feature-1`            | `git tag v1.0`                            |
| **Switch To**      | `git checkout feature-1`          | `git checkout v1.0` (read-only mode)      |
| **Push**           | `git push origin feature-1`       | `git push origin v1.0`                    |
| **List**           | `git branch`                      | `git tag`                                 |

---

## 🧳 Git Stash – Temporarily Save Work

### 🎯 What It Does
You're in the middle of editing files, but need to switch branches.  
Use `git stash` to **save your work temporarily** without committing.

### ✨ Commands

```bash
git stash save " message"            # Save your current uncommitted work
git stash list                       # View all saved stashes   # o/p : stash@{1289} ,stash@{9089}
git stash apply                      # Apply latest stash (keep it)
git stash pop                        # Apply and remove latest stash
git stash show                       # See what’s inside
git stash clear                      # Remove all stashes

🧠 Real-Life Analogy
===============================

You’re drawing something but need to pause.
You roll up your artwork, put it in a drawer (stash),
help your friend with another drawing (other branch),
then come back, unroll your artwork, and continue.

♻️ Git Restore – Undo Local Changes
===============================================
🎯 What It Does

Helps undo changes in your working directory before commit.


git restore filename        # Discard changes in a specific file
git restore .               # Discard changes in all files
git restore --staged file   # Unstage a file (move from index back to working area)

🧠 Use Case
===================================
Oops! You made changes but want to go back to how it was last commit?
Use git restore.


🙌 final  Summary
==========================================
🔀 Use branches to work on things

🔖 Use tags to mark important versions

🧳 Use stash to temporarily put your changes aside

♻️ Use restore to undo uncommitted changes

