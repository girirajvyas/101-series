# GIT BASH Commands to initialize and push project to remote repository

**Step 1: Only For first time user**
```
  git config --global user.email "UserName@example.com"
  git config --global user.name "User Name"
```
__Step 2: For adding new Repository to Github__
```
  git init
  git add
  git commit -m "First commit"
  git remote add origin https://github.com/girirajvyas/springcloud-startup-module1.git 
  git remote -v
  git push origin master
  ```
**Step 3: Error Scenarios**  
  In case you face error: "Github “fatal: remote origin already exists”"
  ```
  git remote rm origin
  git remote add origin https://github.com/girirajvyas/springcloud-startup-module1.git
  ```
  **OR** 
  ```
  git remote set-url origin https://github.com/girirajvyas/springcloud-startup-module1.git
  ```
**Delete folder in repository**
```
  git rm -r adata
```

# Complete process to create and push project to remote repository from an IDE(STS)
**Step 1 :**
- New spring initializr
- artifactId:chayan
- groupId:io.github.girirajvyas.chayan
- Package:io.github.girirajvyas.chayan

**Step 2:** 
- Create an empty repository(avoid .gitignore and README.md) to avoid unnecessary complications later
- Copy the URI fom second paragraph with heading "…or push an existing repository from the command line"
- URI: *https://github.com/girirajvyas/chayan.git*

**Step 3:** 
- Push the code Initialized on local repository to remote github repository
- Right click on project name > Team > share project
- Right click on project name > Team > Commit > drag all changes from un-staged to staged > commit message > commit
- Right click on project name > Team > Push > give URI(https://github.com/girirajvyas/chayan.git) > Next > Finish > Done

**Step 4:**
- go to remote repository an validate if changes are available there.
