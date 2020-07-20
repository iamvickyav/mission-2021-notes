## Git Lessons

    > git config --global user.name "iamvickyav"
    > git config --global user.email vickyavw.10@gmail.com
    > git config --list

    user.name
    user.email

    Go inside Project folder (git_sample)

    > git init

    	Start tracking files inside the folder
    	also creates a .git folder (hidden)

    > .gitignore created & add target/ .idea/

    > git status

    	untracked/tracked files, but not committed files

    > git add 1.txt

    > git commit -m "1.txt file added"

    	HASH --> 6dee2302856a00217ba8346b9e600a6ad8318aab

    > git remote add origin https://github.com/iamvickyav/mission-2021.git

        Cloud URL to which code to be sent

    > git push -u origin master

        To send files to cloud
