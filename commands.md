## 🔹 1. Configuration

```bash
git config --global user.name "Your Name"        # Set global username
git config --global user.email "you@example.com" # Set global email
git config user.name "Local Name"                # Set local username (repo-specific)
git config user.email "local@example.com"        # Set local email (repo-specific)
git config --list                                # List all current config settings
git config --show-origin                         # Show where each config is set
```

------------------------------------------------------------------------

## 🔹 2. Repository Initialization

```bash
git init             # Initialize a new Git repository
git clone <url>      # Clone an existing repo from remote
```

------------------------------------------------------------------------

## 🔹 3. File States and Staging

```bash
git status                  # Show status of files (staged, unstaged, untracked)
git add <file>              # Stage a specific file
git add .                   # Stage all modified and new files
git add -A                  # Stage all changes (including deletions)
git reset <file>            # Unstage a file
git reset                   # Unstage everything
```

------------------------------------------------------------------------

## 🔹 4. Committing Changes

```bash
git commit -m "message"     # Commit staged changes with a message
git commit -am "message"    # Add & commit tracked files in one step
```

------------------------------------------------------------------------

## 🔹 5. Viewing Commit History

```bash
git log                     # Full commit history
git log --oneline           # Condensed one-line format
git log --graph --all       # Graphical view of all branches
git show <commit>           # Show details of a specific commit
```

------------------------------------------------------------------------

## 🔹 6. Branching

```bash
git branch                  # List all branches
git branch <name>           # Create a new branch
git checkout <name>         # Switch to a branch
git checkout -b <name>      # Create and switch to a new branch
git branch -d <name>        # Delete a branch (only if merged)
git branch -D <name>        # Force delete a branch
```

------------------------------------------------------------------------

## 🔹 7. Merging & Rebasing

```bash
git merge <branch>          # Merge branch into current one
git rebase <branch>         # Reapply commits on top of another base
git rebase -i HEAD~n        # Interactive rebase last n commits
```

------------------------------------------------------------------------

## 🔹 8. Remote Repositories

```bash
git remote -v                       # List remotes
git remote add origin <url>        # Add remote repository
git push -u origin <branch>        # Push branch and track remote
git push                            # Push current branch to remote
git pull                            # Fetch and merge from remote
git fetch                           # Fetch from remote (without merging)
git remote remove origin            # Remove a remote
```

------------------------------------------------------------------------

## 🔹 9. Undoing Changes

```bash
git checkout -- <file>              # Discard changes in working directory
git restore <file>                  # Newer alternative to discard changes
git reset --hard                    # Discard all changes (DANGEROUS)
git reset --soft HEAD~1             # Undo last commit, keep changes staged
git reset --mixed HEAD~1            # Undo last commit, unstaged
git revert <commit>                 # Revert a specific commit by creating a new one
```

------------------------------------------------------------------------

## 🔹 10. Stashing (Temporary Save)

```bash
git stash                           # Save uncommitted changes
git stash list                      # List stashes
git stash apply                     # Apply latest stash
git stash pop                       # Apply and remove latest stash
git stash drop                      # Delete latest stash
```

------------------------------------------------------------------------

## 🔹 11. Tags (Software Versioning i.e. v1.0.0)

```bash
git tag                             # List all tags
git tag <name>                      # Create a lightweight tag
git tag -a <name> -m "message"      # Annotated tag
git push origin <tag>               # Push specific tag
git push origin --tags              # Push all tags
git tag -d v1.0.0                   # Delete the mentioned tag

OR

git tag -a v1.0.0 <SHA(optional)>
Vim editor:
Fn + insert key                     # write message(i.e. v1.0.0)
Esc key
:wq                                 # save and quit
git tag -d v1.0.0                   # Delete the mentioned tag
```

------------------------------------------------------------------------

## 🔹 12. Submodules

```bash
git submodule add <repo> <path>     # Add a submodule
git submodule update --init         # Initialize and update submodules
git submodule foreach git pull      # Update all submodules
```

------------------------------------------------------------------------

## 🔹 13. Useful Inspection Commands

```bash
git diff                            # Show unstaged differences
git diff --staged                   # Show staged differences
git blame <file>                    # Show who last modified each line
git clean -fd                       # Delete untracked files and folders
```

------------------------------------------------------------------------

## 🔹 14. Aliases (Optional Shortcuts)

```bash
git config --global alias.co checkout     # git co = git checkout
git config --global alias.br branch       # git br = git branch
git config --global alias.cm 'commit -m'  # git cm = git commit -m
git config --global alias.st status       # git st = git status
```

------------------------------------------------------------------------

## 🔹 15. Git Ignore & Attributes

### .gitignore — list files/folders to ignore
```
node_modules/
*.log
.env
```

### .gitattributes — control diff/merge behavior
```
*.pdf binary    # Treat PDFs as binary files
```

------------------------------------------------------------------------

## 🔹 16. Troubleshooting

```bash
git fsck                            # Check repository for issues
git gc                              # Garbage collect to optimize repo
git reflog                          # Show history of HEAD changes
```

------------------------------------------------------------------------

Use `--help` with any Git command to get detailed usage, e.g.:
```bash
git commit --help
```
