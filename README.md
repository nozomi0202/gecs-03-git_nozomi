# Exercises for GECS course (github)
> [!WARNING]
> The below commands are intended for people who understand git usage.
> Please do not run them if you are not really familiar with what is going on.

## Exercise part-1
1. Run below command to restart git  
```zsh
rm -rf .git
git init
```

2. Change ```madlibs.txt```, by filling in Author section. 

3. After your changes, add you ```madlibs.txt``` to git.
```zsh
git add madlibs.txt
git status
```

4. After staging your changes, commit your changes.
```zsh
git commit -m 'initial commit'
git status
```

5. Checkout your current git commits.
```zsh
git status
git log
```

6. Change your file again, this time filling in parentheses. 

7. Stage, then commit.
```zsh
git add madlibs.txt
git commit -m 'Updated text in madlibs.txt'
```

8. Checkout your last commit.
```zsh
git log
git checkout [commit hash]
```

9. Get back to your main branch.
```zsh
git checkout main
```

## Exercise part-2
1. Create new branch. 
```zsh
git branch change_noun
git checkout change_noun
```

2. Change a critical noun in your madlibs.txt.

3. Stage, commit, and return to main branch.
```zsh
git add madlibs.txt
git commit -m 'Changed noun [A] to [B]'
git checkout main
```

4. Repeat step 1-3. Change the same noun you did last time but to another one.
```zsh
git branch change_another_noun
git checkout change_another_noun
# Update your file.
git add madlibs.txt
git commit -m 'Changed noun [A] to [C]'
git checkout main
```

5. Merge your first branch to main.
```zsh
git merge change_noun
```

6. Merge your second branch to main.
```zsh
git merge change_another_noun
```

7. Resolve conflicts, stage and commit.
```zsh
git status
# correct conflict
git add madlibs.txt
git commit
```
