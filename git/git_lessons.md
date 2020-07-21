## Git Lessons

### Setup Git

#### Setup User name & Email

> git config --global user.name "iamvickyav"
> git config --global user.email vickyavw.10@gmail.com

#### To verify setup

> git config --list

<hr />

### Enable Git in your Project

#### Initialise Git

Go inside Project folder in command prompt & run the following command

> git init

- Created .git folder (hidden) inside your project
- Git starts tracking files inside your project

#### Create .gitignore file

.gitignore is a file where we can specify what are all files/folders we want the git to stop tracking  

> touch .gitignore

- Add following in .gitignore
``` 
target/ 
.idea/
.classpath
```

#### Check files in untracked & tracked state

> git status

This will only check & show status of files which are either in tracked or untracked state

<hr />

### Changing state of files

##### To Move file(s) from Untracked to Tracked state

> git add 1.txt

(or)

> git add .

##### To Move file(s) from Tracked state to Committed state

> git commit -m "1st file added"

Git commit command will created a unique hash value for each of the commits

E.g 6dee2302856a00217ba8346b9e600a6ad8318aab

<hr />

### Pushing code to remote

##### To Add a remote Github repo

> git remote add origin https://github.com/iamvickyav/mission-2021.git

    
##### Push code to remote Github repo

> git push -u origin master