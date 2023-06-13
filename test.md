# github
## initialize a Git repository
git init
    # e.g. /Users/hyunoh/.git
touch .gitignore

## …or create a new repository on the command line
echo "# script" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/hyun52/script.git
git push -u origin main
    # github perpetual cose
    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

# …or push an existing repository from the command line
git remote add origin https://github.com/hyun52/script.git
git branch -M main
git push -u origin main

## PUSH YOUR CHANGES
# First, you can either add all or only selected changed files for the next commit.
git add .
git add <path/to/file>

# There is also a way back from a staged to an unstaged file.
git reset HEAD <path/to/file>

# commit the staged files with a commit that comes with a commit message.
git commit -m "<message>"

# Use the default commit command to make a more elaborated commit message with multi-lines afterward.
git commit

# push all the commits in one command to the remote repository.
git push origin master

# pull all the changes from the remote repository before you are allowed to push your own changes.
git pull origin master

## GIT STATUS, LOG AND HISTORY
# check the local staged and unstaged changes
git status

# see your local unstaged changes compared to the recent commit
git diff

# see the git history of commits
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"

git log

## BRANCHING
# (1) create a new branch
git checkout -b <branch_name>

# (2) check out an available branch
git checkout <branch_name>
