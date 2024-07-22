# Road To Git Master 

## ⚙️ Set Up

### Git Config

#### See all the config
```bash
git config --list #show all the settings in gitconfig
```
#### Open config to edit
```bash
git config --global -e #open .gitconfig file
```
#### Set default editor
```bash
git config --global core.editor "code --wait" # set default text editor for git 
```
#### User settings
```bash
git config --global user.name "name" #set user.name
git config --global user.email "email" #set user.email
git config user.name #check user.name
git config user.email #check user.email
```
#### Set Auto CRLF
```bash
git config --global core.autocrlf true #for Windows
git config --global core.autocrlf input #for Mac
```
#### Git Aliases
```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

## 🔧 Tools

### 🐛 Basic Debugging
```bash
git blame file.txt
```

### 🔎 Bisect 
```bash
git bisect start
git bisect good hash
git bisect good 
git bisect bad
git bisect reset
```

### 🍯 Config 
```bash
# git config --global -e
[alias]
	hist = log --graph --all --pretty=format:'%C(yellow)[%ad]%C(reset) %C(green)[%h]%C(reset) | %C(white)%s %C(bold red){{%an}}%C(reset) %C(blue)%d%C(reset)' --date=short
	l = log --graph --all --pretty=format:'%C(yellow)%h%C(cyan)%d%Creset %s %Cgreen(%cr) %C(magenta)<%an>%Creset'
	s = status
	st = stastus
	up = !git fetch origin master && git rebase origin/master
	co = checkout
	ca = !git add -A && git commit -m
	cad = !git add -A && git commit -m "."
	c = commit -m
	b = branch
	pop = stash pop
	apply = stash apply
	rc = rebase --continue
	new = "!f(){ git co -b derek0k-$1 origin/master && git pull; };f"

# open ~/.zshrc
alias gs="git status"
alias gc="git checkout"
alias gh="git reset --hard HEAD"
alias gss="git stash save"
alias gsl="git stash list"
alias gsa="git stash apply"
```






