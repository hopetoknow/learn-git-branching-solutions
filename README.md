# Learn Git Branching Solutions

This repository contains my solutions to every single problem available on 
[Learn Git Branching](https://learngitbranching.js.org/). Each solution is designed to help you understand and master
various Git concepts.

Feel free to explore the solutions, use them as a reference, or contribute by submitting a pull request or creating
an issue if you find any problems or have suggestions for improvements.
## Main

### 1.1 Introduction to Git Commits
```
git commit
git commit
```

### 1.2 Branching in Git
```
git branch bugFix
git checkout bugFix
```
```
git checkout -b bugFix
```

### 1.3 Merging in Git
```
git checkout -b bugFix
git commit
git checkout main
git commit
git merge bugFix
```

### 1.4 Rebase Introduction
```
git checkout -b bugFix
git commit
git checkout main
git commit
git checkout bugFix
git rebase main
```

### 2.1 Detach yo' HEAD
```
git checkout C4
```

### 2.2 Relative Refs (^)
```
git checkout bugFix^
```
```
git checkout C4^
```

### 2.3 Relative Refs #2 (~)
```
git checkout HEAD~1
git branch -f main C6
git branch -f bugFix HEAD~1
```

### 2.4 Reversing Changes in Git
```
git reset local^
git checkout pushed
git revert pushed
```