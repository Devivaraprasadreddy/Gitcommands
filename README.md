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

### 2. If the files are larger than 100MB Git rejects the pushing, so install lfs

```bash
git lfs install
```
```bash
git lfs track "*.zip"
git lfs track "*.mp4"
git lfs track "*.exe"
git lfs track "*.pdf"
```
```bash
git add .gitattributes
```
```bash
git commit -m "Track Large Files"
```
```bash
git push
```

### Connect the local system to GitHub 
Step 1: Create the key
```bash
ssh-keygen -t RSA -b 4096 -C "devivaraprasad55@gmail.com"
```
Step 2: Check the agent connection
```bash
eval "$(ssh-agent -s)"
```
### It shows the ouput like this
```bash
Agent pid 2133
```
Step 3 : Add the private key
```bash
ssh-add ~/.ssh/id_ed25519
```
Step 4 : Copy the Public Key
```bash
cat ~/.ssh/id_ed25519.pub
```
Step 5 : Copy that public key and paste it into GitHub Settings --> SSH and GPG keys --> Click on New SSH key and paste the key
Step 6 : Check the Connection
```bash
ssh -T git@github.com
```
### It shows the Output Like this
```
Hi Devivaraprasadreddy! You've successfully authenticated, but GitHub does not provide shell access.
```
### Once Connection was Successfull Pelase follow the below commands
```bash
git remote add origin git@github.com:USERNAME/REPO.git
git branch -M main
git push -u origin main
```
