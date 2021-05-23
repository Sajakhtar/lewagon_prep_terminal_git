1. [Terminal 101](#terminal-101)
1. [Git and Github](#git-and-github)
1. [Github Pages](#github-pages)

# Terminal 101

### Print current directory

`pwd`
`echo %cd%` for windows

### List files in current directory

`ls`
`dir` - for windows

### navigate to directory

`cd folderName`

### Move back up a directory

`cd ..`

### Make a directory

`mkdir newfolderName`

### Make a file

`touch filename.ext`
`type nul > filename.ext` for windows empty file
`echo some text > filename.ext` for windows non-empty file

### Rename file

`mv currentFilename.ext newFilename.ext`
`rename currentFilename.ext newFilename.ext` for windows

### Move file

`mv file.ext folderPath/ file.ext`
`move file.ext folderPath\file.ext` for windows

### Print file content

`cat file.ext`
`more file.ext` for windows
`type file.ext` for windows

### Remove a file

`rm file.ext`
`del file.ext` for windows

### Move back to home directory

`cd`
No command for windows

# Git and Github

### initialize repo

`git init`

### check branch

`git branch`

### Change branch from Master to Main

`git branch -M main`

### check status of changes

`git status`

### add changes

`git add .`
`git add 'filename'`
`git add 'file1' 'file2'`

### Undo a Git add .

`git reset`

### commit changes

`git commit –m "add a comment of the changes"`

### see historical commits

`git log`

### Check remote connections

`git remote -v`

There can be many remote connections e.g. Github, Heroku, etc...

### Assign GitHub repository to local directory

`git remote add origin https://github.com/Sajakhtar/{REPO NAME}.git`

### push changes to github first time

`git push –u origin main`

### push changes after first time round

`git push`

### Creating branches

`git checkout -b new-branch-name`

One branch = One feature

### Change to a branch

`git checkout branch-name`

### difference between branches

### delete a branch

`git branch -d branch-name`

### Check difference between branches

`git diff main..branch-name`

`git diff branch1..branch2`

`git diff master..feature`

### Compare commits between branches

`git log branch1..branch2`

`git log master..feature`

### Compare two branches using commit abbreviations

`git log --oneline --graph --decorate --abbrev-commit branch1..branch2`

`git log --oneline --graph --decorate --abbrev-commit master..feature`

### Merge branche with Main

`git checkout branch-name`
`git merge main` - updates `branch-name` to match `main`

`git checkout main`
`git merge branch-name` - updates `main` to match `branch-name`

During situations when you require a merge commit during a fast forward merge for record-keeping purposes, you will execute git merge with the --no-ff parameter.
`git merge --no-ff branch-name`

### Pull requests

- Pull Request opens a conversation among your team.
- In Github UI, your teammates will read the changes you made, comment (line by line if need be), ask questions, request corrections and maybe new changes.
- This will trigger new commits on your side, and when everyone is satisfied, the lead developer will merge the changes to the master/ main branch i.e. the live version of your website.
- In Github UI, The leader developer can can click the the `Merge Pull Request` button, to merge your branch into the Main branch.
- When you file a pull request, all you’re doing is requesting that another developer (e.g., the project maintainer) pulls a branch from your repository into their repository.

clone the repo:
`git clone https://github.com/{USERNAME}/{REPO_NAME}.git`

Create new branch:
`git checkout -b new_branch`

Create a new remote for the upstream repo:
`git remote add upstream https://github.com/{USERNAME}/{REPO_NAME}.git`

"upstream repo" refers to the original repo you created your fork from

The idea of branches is to create them for small changes and merge them with the Main branch swiftly. If you're branch is being worked on for days, then you'll likely face conflicts when merging.

# Github Pages

### create github pages branch

`git checkout -b gh-pages`

### create github pages branch first time

`git push -u origin gh-pages`

In Browser, go to GitHub repo (`https://github.com/Sajakhtar/{REPO NAME}`), then go to Settings, then go to Github Pages or Pages to find the URL for your hosted site.

The project will be hosted on `https://sajakhtar.github.io/{REPO_NAME}}/` which defaults to the `index.html` or `READNE.md`. Follow the repo folder strucuture to reach other `.html` page.

e.g. `https://sajakhtar.github.io/{REPO_NAME}}/about.html` or `https://sajakhtar.github.io/{REPO_NAME}}/{FOLDER_NAME}/{FILE.html}`

## Making Updates

### Switch to main branch

`git checkout main`

### add changes

`git add .`

### commit changes

`git commit –m "add a comment of the changes"`

### push changes on main branch

`git push`

### Switch to gh-pages branch

`git checkout gh-pages`

### Check difference between branches

`git diff main..gh-pages`

### merge changes from main branch on to gh-pages branch

`git merge main`

### push changes on gh-pages branch

`git push`
