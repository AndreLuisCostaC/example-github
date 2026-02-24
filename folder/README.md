# Example Git Repository
# https://git-school.github.io/visualizing-git/
# 
# This guide should be organized in an workflow maner
https://learngitbranching.js.org/

We are learning how to make commits

- git config --list (Check the git configuration user.name, user.email, etc...)

1. make some changes
2. git add -- "stage" the changes that we want to persist to our git history"
3. git commit -m "adding ..." --creates a commit (use messages in the present tense)

4. git log -- Show all git events
5. git checkout --travel to a specific commit (master to go to the last-one)
5.1 git checkout branch <name> to change the branch

6 git branch to list branchs
6.1 git branch <name> to create a new branch
6.2 git branch -d <name>

# Github (Remote)

#The three below commands to connect a local repository to a remote repository
1st - git remote add origin https://github.com/AndreLuisCostaC/example-github.git
2nd - git branch -M main
3rd - git push -u origin main


git push origin feature/docs => push a specific branch to the remote

git branch -a => list all branchs, the locals and the remotes

git remote -v => list all remote branchs associated with the repository

git push => push the commits from local to remote
git pull => bring the changes in remote to local

-- change the branch from main to feature/docs
git checkout feature/docs => change the branch

git merge main => update the feature/docs with the local main
git pull origin main => update the feature/docs with the remote main

another way to get the same result
git fetch origin main => fetch the content but not update the branch
git merge main => merge into the branch the updates that was fetched

it is equivalent to git pull origin main

Associate a branch in local with the branch in remote (other than main)
git push --set-upstream origin feature/docs


Git UI allow creating repositories, branches, commits, tag, etc..
# created the repo locally
from local repository ->(to) => "remote" (git add remote <name>(origin) <URL>)

# created the repo remotelly
git clone <URL>

#Git workflow
git checkout <branch>
git checkout -b <new branch>
git add, git commit -m "..." (several times)
git push origin <new branch>

git push --set-upstream origin <new branch>
git pull [origin <new branch>]

# create a new branch remotelly
using the GitHub UI to create <branch>
git fetch --all
git checkout <branch>
git pull