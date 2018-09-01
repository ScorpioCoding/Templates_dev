# GIT Cheat Sheat

### Git: Configuration

- `$git config --global user.name "FirstName LastName"`
- `$git config --global user.email "your-email@email-provider.com"`
- `$git config --global color.ui true`
- `$git config --list`

### Git: Starting a repository

- `$git init`
- `$git status`

### Git: Starting files

- `$git add <file-name>`
- `$git add <file-name> <another-file-name> <yet-another-file-name>`
- `$git add .`
- `$git add -all`
- `$git add A`
- `$git rm --cached <file-name>`
- `$git reset <file-name>`

### Git: Commiting to a repository

- `$git commit -m "Your Message"`
- `$git reset --soft HEAD^`
- `$git commit --amend -m "Your Message"`

### Git: Pulling & Pushing from and to repositories

- `$git remote add origin <link>`
- `$git push -u origin master`
- `$git push -u origin gh-pages`
- `$git clone <clone>`
- `$git pull`\* `
- `$git push --set-upstream gh-pages gh-pages`

### Git Branching

- `$git branch`
- `$git branch <branch-name>`
- `$git checkout <branch-name>`
- `$git merge <branch-name>`
- `$git checkout -b <branch-name>`

### Git: Store git credentials on windows

If you use wincred for credential.helper, git is using the standard windows Credential Manager to store your credentials.

- `$git config --global credential.helper wincred`
- You can view the Credential Manager from your Control Panel settings.

### Projects with a GitHub pages repo

1. Create a prj folder ex. WidePack
2. Create to sub folders `dev` & `pub`
3. On Github create a repo widepack.dev
4. clone the repo widepack.dev -> dev folder.
5. On Github create a repo widepack
   - do not name the repo widepack.pub otherwise the url becomes https://<user>.ginthub.io/widepack.pub
6. create a new branch gh-pages, set it to default and delete the master.
7. Settings->Github Pages > Source => gh-pages branch and delete the master
8. clone the repo widepack -> pub folder
9. In the pub folder do a `npm init` and then an `npm i --save-dev gh-pages`
10. Modify the package.json file : aad a script : `"depoly": "gh-pages -d dist"`
    - remember to add a comma to the last existing script
11. copy index.html from the dev folder to the pub folder.
12. add the git origin to pub `git remote add origin <link>`
    - for some reason an remote origin is required otherwise
13. do a git add . and a `git commit -m "init"`
14. run npm : => `npm run deploy`
15. If succesfully publish you can delete all files and folders in the pub folder except the .git folder.
16. Start developing in the dev folder and commit reguarly to the dev repo
17. when you want to publish the rest or just a milestone

- copy the require files to pub folder and do a `git add .` and a `git commit -m "update 2018-02-02 : milestone or fix or release #..."`

#### Conclusion:

You only have to install npm gh-pages once in the pub folder
And once publish you can git the rest and delete the node_modules folder.

---

## WidePack Origin

- Add a remote origin  
  `git remote add origin https://github.com/ScorpioCoding/widepack.git`
