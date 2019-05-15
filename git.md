
## BRANCH
### delete 
```bash
git branch -d <branch_name> # local
git push --delete <remote_name> <branch_name> # remote
```

### Push to remote 
```bash
git push -u origin <branch>
```

### List all files that changed in branch
```bash
git diff --name-only master...
```

Migrate bzr to git
----------------------
git init &&
   bzr fast-export `pwd` | git fast-import &&
   rm -r .bzr &&
   git reset HEAD &&
   mv .bzrignore .gitignore
