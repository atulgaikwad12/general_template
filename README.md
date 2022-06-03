# general_template
general template for any python project 


### Project Execution steps 
#### Clone repository in local
```bash
git clone <repository_url>
``` 
#### Execute below commands in git bash. (Note - Must have conda installed and path defined of conda in system environments)
##### Step 1 : Activate base conda Enviroment
`If using git bash then use below command`
```buildoutcfg
source activate base
```
`Else for cmd use`
```
conda activate base
```

##### Step 2 : Create new Conda Enviroment & Activate it
`To Create Conda Enviroment and activate it` 
```buildoutcfg
conda create -n <envName> python=3.7 -y
conda env list
activate <envName>
```

`Conda command to create virtual env inside current directly`
```
conda create --prefix ./env python=3.7 -y && conda activate ./env
```
##### Step 3 : Install required packages and List down libraries
```bash
pip install -r requirements.txt
conda list
```
##### Step 4 : To save your version of code. Create new git repository & then execute below commands only once to push change first time.
```bash
git add .
git status
git commit -m "commit message"
git remote add origin 'your_repository_url'
git branch -m master main
git push -u origin main
```
##### After first commit for subsequent changes just execute below commands
```bash
git add .
git commit -m "commit message"
git push
``` 
## To freeze new requirements.txt File
```buildoutcfg
pip freeze>requirements.txt
```

### Extra git commands just for reference
`Git commands to publish code (remote repo - "origin", local branch default name -  "master", renamed to "main") `
```buildoutcfg 
git init 
git add .
git commit -m 'First Commit Msg'
git status 
git remote add origin git@github.com:username/new_repo
git branch -m master main
git push -u origin main
```

`Stash changes to clean working tree (so to work with new changes keeping old changes stored temporay aside)`
```
git status
git stash
```
`Clean stash & again apply to working tree`
```
git status
git stash pop
```
`Reapply stash without cleaning it`
```
git status
git stash apply
```

`Sync local repository with remote one (remote repo - origin)`
```
git diff
git fetch origin
git log --oneline main..origin/main
git checkout main
git log origin/main
git merge origin/main
```

`Remove file from stagging area`
```
git status
git rm --cached fileName
```

`To see last commit log (press q to quit)`
```
git log -p -1
```

`To see summarized status`
```
git status -s
```

`To create new branch and switch to it`
```
git branch <newbranchnaame>
git branch
git checkout <newbranchName>
```
`Alternate way to do same `
```
git checkout - b <newBranchName>
```

`To merge new branch changes to master`
```
git checkout master
git merge <newbranchname>
```

`Clone any repository in local`
```
git clone <repo_url> <optional_foldename>
``` 

`To see merged/Non merged branch`
```
git branch --merged
git branch --non-merged
```

`To delete merged branch`
```
git branch -d <BranchName>
```

`To delete non merged branch`
```
git branch -D <BranchName>
```

`To unstage files from staging area not changing working directory so to match last commit`
```
git reset
```

`To unstage files from staging area as well as from working directory so to match last commit`
```
git reset
```
`Git add and commit in same command`
```
git commit -a -m "message"
```
