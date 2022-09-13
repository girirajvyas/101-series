# About
This page contains the information for initializing/setting up github repo and commiting code from your local machine to the GitHub repo. This is a very basic scenarion when you are start working with GitHub.

Lets see the ways in which you can initialize a repository with your code.
 - Git Bash
 - TortoiseGit
 - IDE

What you will find below?
 - There are steps including commands to initialize and push project to remote repository
 - Also, you will find details about docusaurus which is used for creating the documentation.

Once you are done commiting your code to github, It might be the case you start searching how to publish these changes on a site, for this you can go through **GH-Pages** 

## GIT BASH

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
  git rm -r metadata
```

## Tortoise Git
- TODO


## IDE(STS)

**Step 1 :**
- New spring initializr
- **artifactId:** chayan (your project name)
- **groupId:** io.github.girirajvyas.chayan
- **package:** io.github.girirajvyas.chayan

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
- Go to remote repository an validate if changes are available there.


## GH-Pages
This is used for publishing your changes via static site. There can be 2 types of pages 
  - **User pages:** http://yourusername.github.io/ (1 per account)  
  - **Project Pages:** http://yourusername.github.io/projectname/ (1 per project)  

**Create User Page**
1. Create repository username.github.io (Menu -> new repository)  
*Note: using username is mandatory as url is mapped with username*  
2. repository must be public (any way you can only have public repository if you are not having a paid account)  
3. you may or may not initialize this with README.md  

**Project Page**
1. Create Repository  
2. Create branch from the above repository name "gh-pages" (if working from it terminal: git checkout -b gh-pages)  
"gh-pages" is a special branch used by Git to publish from.  
3. Commit your Html code with index.html (you can also publish your anular application)  

**Build static content**  
Github uses Jekyll as default site generator, but there are many good alternatives available as well.  

**Publish Project via gh-pages**
In case you have to publish your code to gh-pages, e.g: girirajvyas.github.io/profile  
Create a branch at start and delete everything in it so that we can finally deploy the dist folder.    

    ```
       git checkout gh-pages (-b if branch not already created)  
       git rm -r *
       git commit -m "removed everything from gh-pages"   
       git push --set-upstream origin gh-pages  
    ```

## Docusaurus

Initialize docusaurus
```
npx @docusaurus/init@next init gof-design-patterns classic
```

Logs: 
```
Success! Created gof-design-patterns
Inside that directory, you can run several commands:

  npm start
    Starts the development server.

  npm run build
    Bundles the app into static files for production.

  npm deploy
    Publish website to GitHub pages.

We suggest that you begin by typing:

  cd gof-design-patterns
  npm start
```

## References:  
**Rename Repository:**
 - https://stackoverflow.com/questions/5751585/how-do-i-rename-a-repository-on-github

**For Github flavored MarkDown:** 
 - https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet  
 - https://guides.github.com/features/mastering-markdown/

**Emojis in MarkDown:**
 - https://unicode-table.com/en/sets/arrow-symbols/ - icons
 - https://www.webfx.com/tools/emoji-cheat-sheet/ -icons
 - https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md
 
**Flowcharts in MarkDown**
 - https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/

**Adding new Repository via Git Bash (*it is not possible to do it with Egit plugin*):**
 - https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/

**Other:**
 - https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/  
 - https://stackoverflow.com/questions/22932422/get-github-avatar-from-email-or-name 

**Docusaurus:**  
 - https://v2.docusaurus.io/docs/docs-introduction
 - https://v2.docusaurus.io/docs/creating-pages
 - https://v2.docusaurus.io/docs/deployment/
 - https://v2.docusaurus.io/docs/installation

**gh-pages:**  
 - https://pages.github.com/
 - https://jekyllrb.com/
 - https://jekyllrb.com/docs/installation/windows/
 - https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll
 - https://docusaurus.io/docs/en/installation/
 - https://v2.docusaurus.io/docs/installation
 
**Git Handbook:**  
- https://guides.github.com/introduction/git-handbook/

**Use Github Avatars:**  
- https://avatars.githubusercontent.com/<username>
- https://avatars.githubusercontent.com/u/<userid>

**Jekyll:**  
- https://rubyinstaller.org/downloads/
- https://jekyllrb.com/docs/step-by-step/01-setup/
- https://docs.github.com/en/github/working-with-github-pages/about-github-pages-and-jekyll
- https://docs.github.com/en/github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-with-the-theme-chooser

**Consolidate Multiple projects in 1 repo**
 - https://stackoverflow.com/questions/14679614/whats-the-best-practice-for-putting-multiple-projects-in-a-git-repository
 - https://stackoverflow.com/questions/5514739/best-practice-for-git-repositories-with-multiple-projects-in-traditional-n-tier?rq=1
 - https://github.community/t/create-folder-for-multiple-repos/2087
 - https://github.community/t/how-to-move-multiple-repositories-into-one/2382