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

### 3.1 Cherry-pick Intro
```
git cherry-pick C3 C4 C7
```

### 3.2 Interactive Rebase Intro
```
git rebase -i HEAD~4
```
```
git rebase -i overHere
```

### 4.1 Grabbing Just 1 Commit
```
git checkout main
git cherry-pick C4
```
```
git rebase -i main
git checkout main
git merge bugFix
```
```
git rebase -i main
git branch -f main C4'
```

### 4.2 Juggling Commits
```
git rebase -i HEAD~2
git commit --amend
git rebase -i HEAD~2
git branch -f main HEAD
```
```
git rebase -i main;
git commit --amend;
git rebase -i main;
git rebase caption main
```

### 4.3 Juggling Commits #2
```
git checkout main
git cherry-pick C2
git commit --amend
git cherry-pick C3
```

### 4.4 Git Tags
```
git tag v0 C1
git tag v1 C2
git checkout v1
```

### 4.5 Git Describe
```
git commit
```

### 5.1 Rebasing over 9000 times
```
git rebase main bugFix
git rebase bugFix side
git rebase side another
git rebase another main
```

### 5.2 Multiple parents
```
git branch bugWork C2
``` 
```
git branch bugWork HEAD~^2~
```
```
git branch bugWork HEAD^^2^
```

### 5.3 Branch Spaghetti
```
git rebase main one
git rebase -i C1
git rebase main two
git rebase -i C1
git branch -f three C2
```
```
git checkout one
git cherry-pick C4 C3 C2
git checkout two
git cherry-pick C5 C4 C3 C2
git branch -f three C2
```

## Remote

### 1.1 Clone Intro
```
git clone
```

### 1.2 Remote Branches
```
git commit
git checkout o/main
git commit
```

### 1.3 Git Fetchin'
```
git fetch
```

### 1.4 Git Pullin'
```
git pull
```

### 1.5 Faking Teamwork
```
git clone
git fakeTeamwork 2
git commit
git pull
```

### 1.6 Git Pushin'
```
git commit
git commit
git push
```

### 1.7 Diverged History
```
git clone
git fakeTeamwork
git commit
git pull --rebase
git push
```

### 1.8 Locked Main
```
git reset --hard o/main
git checkout -b feature C2
git push
```
```
git branch feature main
git reset --hard HEAD^
git push origin feature
git checkout feature
```

### 2.1 Push Main!
```
git fetch
git rebase o/main side1
git rebase side1 side2
git rebase side2 side3
git rebase side3 main
git push
```

### 2.2 Merging with remotes
```
git checkout main
git pull
git merge side1
git merge side2
git merge side3
git push
```

### 2.3 Remote Tracking
```
git checkout -b side o/main
git commit
git pull --rebase
git push
```

### 2.4 Git push arguments
```
git push origin main
git push origin foo
```

### 2.5 Git push arguments -- Expanded!
```
git push origin foo:main
git push origin main^:foo
```

### 2.6 Fetch arguments
```
git fetch origin foo:main
git fetch origin main^:foo
git checkout foo
git merge main
```

### 2.7 Source of nothing
```
git push origin :foo
git fetch origin :bar
```

### 2.8 Pull arguments
```
git pull origin bar:foo
git pull origin main:side
```
