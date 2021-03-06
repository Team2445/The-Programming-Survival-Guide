---
title: Learning Git
category: Git
order: 1
---
### Pushing Changes to a Branch

| Bash Command | What it Does |  
| --- | --- |
| `git add --all` | Stages all changes that you made |
| `git commit -m "<Message>"` | Commit changes with message `<message>` |
| `git push` | Push your changes to remote repository. For pushing *pre-existing* branches |

### Creating a new Branch

| Bash Command | What it Does |  
| --- | --- |
| `git checkout -b [branch name]` | Creates new branch `[branch name]` and switches to it |
| `git push -u origin [branch name]` | Pushes *newly created* branch to remote repo. |

### Other Useful Commands  

| Bash Command | What it Does |  
| --- | --- |  
| `git merge [branch name]` | Merges [branch name] __into__ current branch |  
| `git log --oneline` | Shows full list of commit messages. Press **q** to stop viewing |
| `git reset --hard` | Resets all changes back to the last commit |
| `git commit --amend -m "message"` | Replaces last commit message with message |

## Simple Explanation of Git
This is a simplified explanation of git a small amount of reading
[The Simple Guide to Git](https://rogerdudler.github.io/git-guide/)

## Visual Guide
For the visual learners: [Visual Git Guide](https://marklodato.github.io/visual-git-guide/index-en.html)

## Interactive Branching Tutorial
Go through the introduction portions of this interactive git tutorial
[Learn Git Branching](https://learngitbranching.js.org/?locale=en_US)

## Git Cheat Sheet
For command references later you can use this: [Github Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)