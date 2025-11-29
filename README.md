# Gitcommands

### 1. If you push the files from local to GitHub Repository

Step - 1 : Intialization
```bash
git init
```

Step - 2 : Set the Origin or Add the Origin
```bash
git remote add origin <git_url>
```
```bash
git remote set-url origin <git_url>
```
Step - 3 : Add the files to that Repository
```bash
git add .
```
Step - 4 : Before commiting the files check the status of files
```bash
git status
```
Step - 5 : Commit the Files
```bash
git commit -m "<Any message>"
```
Step - 6 : Before Pushing the files check the branch name
```bash
git branch
```
Step - 7 : Push the files to exact branch
```bash
git push origin <branch_name>
#or
git push --set-upstream origin <branch_name>
```

