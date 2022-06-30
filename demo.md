# Github Demo

## Step 1: Sign up and Install
Create account on `github.com`, follow the instructions below (email required)

GOTO Setting => Developer settings => Personal access tokens => Generate new token => copy paste it as your `password`

Install `git` on the server

get help:
- Google `git cheating paper` and choose one you like for reference
- another way is to use `git --help`
---
## Step2: Configuration
Do some global configurations: 
- `git config --global user.name “Your Name”`
- `git config --global user.email “you@example.com”`
- `git config --global color.ui auto`

To avoid password promt everytime:

`git config --global credential.helper store` then do anything that needs login

---
## Step3: Create repo & upload your first file

goto `https://github.com/demonorthrock?tab=repositories` change demonorthrock into your username
click new => choose a name for the repo => make it `PRIVATE` => 

```bash
mkdir directory && cd directory
touch file
git init
git add file
git commit -m 'first commit'
git branch -M main
git remote add origin https://github.com/demonorthrock/new-repo.git 
# change demonorthrock into your username, change new-repo into your repo name
git push -u origin main
```

---
## Step4: Add collaborators 
goto `https://github.com/demonorthrock/new-repo` => settings => collaborators => add people => search for username(stevenwongchess) => check your email => 

---
## Step5: Basic work flow
For collaborators (do this once)

`git clone https://github.com/demonorthrock/new-repo.git && cd new-repo`

`git branch steven && git checkout steven`

```bash
# each create a file
touch b.txt
git add b.txt
git commit -m 'add b.txt'`
git push --set-upstream origin demo` 
# BUT next time only need to type `git push`

# do the same thing for a.txt on another branch
git checkout main && git merge steven
git pull --rebase
git push origin main

# on demo branch 
git pull origin main
git push origin demo

# on main branch
git merge demo
git push
```
