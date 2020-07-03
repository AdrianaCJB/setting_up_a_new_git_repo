# Setting up a new Git Repo, pull and push commands:



## Create a new repository on the command line:

You would need to create the new repo on GitHub before pushing to it.

Open Git Bash
```
cd /path/project/           <!--- Change the current working directory to your local project. --->

git init                    <!--- Initialize the local directory as a Git repository --->

git add .                   <!--- For all the files in current Directory, we need to add a files to staging area --->
or 
git add <File_Name>         <!--- For Single File --->

git status                  <!--- To check if files are added or not  --->

git commit -m "First Commit"

git remote add origin https://github.com/AdrianaCJB/new_repo.git   <!---  Copy the https url of your newly created repo --->

git push origin master     <!---  Push the changes in your local repository to GitHub --->

```

**NOTICE: This is never a recommended use of git. This will overwrite changes on the remote. 
Only do this if you know 100% that your local changes should be pushed to the remote master.**

Try this: 
```
git push -force origin master
```

## Workfow github:

```
git clone -b master [repositorio]
cd [repositorio]
Update files...
git add .
git commit -m "commit message"
git push -u origin master
```

## Git Configuration:

```

$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com


<!--- Git can handle this by auto-converting CRLF line endings into LF when you add a file to the index, 
 and vice versa when it checks out code onto your filesystem.
 You can turn on this functionality with the core.autocrlf setting. 
 
If you’re on a Linux or macOS system that uses LF line endings, then you don’t want Git to automatically
convert them when you check out files; however, if a file with CRLF  endings accidentally gets introduced,
then you may want Git to fix it.

If you’re on a Windows machine, set it to true — this converts LF endings into CRLF when you check out code:  --->

$ git config --global core.autocrlf true


<!--- If you create a ~/.gitignore_global file with these contents:
*~
.*.swp
.DS_Store
--->


$ git config --global core.excludesfile ~/.gitignore_global

```
