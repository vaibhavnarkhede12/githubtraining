GIT USEFUL COMMANDS


there is a file name diskusage.py containing an error so we create a copy of file diskusage_copy.py which has the error correected so to send the
error using diff

1.  diff -u diskusage.py diskusage_copy.py > diskdiskusage.diff
2.  patch diskusage.py < diskusage.diff

configure global git parameters

1.	git config --global user.email "vaibhavnarkhede12@gmail.com"
2.	git config --global user.name "vaibhavnarkhede12"

to add single file to staging are 
1.	git add "diskusage.py"

(staging area consists of file that contins everything which will go in the next comit)
indicates the changes which are remaining to be commited
1.	git status 

to commit something to repo
1.	git commit -m "my first commit" 

(when we git add we add the file to staging area and is yet to be commited )
for details about the git conf parameters
1.	git config -l

command would we use to review the commit history for our project?
1	git log 
2	git log -p ( shows changes along with commit numbers)

track our file
1.	git add 

shortcut to commit files only which are tracked
1.	git commit -a 
to indicatee changes in specific commit 
1.	git show commit no    (commitno  commit number can be seen from git log command)

remove file from commit 
1.	git rm "diskuusage.py" 

to remove file before it is commited i.e from the staging area
1.	git rm -f "diskusage.py”

 change the name of the file
1.	git mv diskusage.py newname.py 

to revert back to the file before staging 
1.	git checkout diskusage.py 

if we want to revert to unstaging area after doing git add .
1.	git reset 
2.	git reset HEAD newfilewhichwasnottobestagedbutstaged.py *(if there is only a single file)


to revert a latest commit made locally to master -- OR --  if you delete any file from local master and you want it back 
1.	git reset --hard origin/master  

to revert back from commit to staging area
1.	git reset --soft HEAD~1 

overwrite the recent commited message
1.	git commit --amend 

to revert back chnages from latest commit to its previous commit 
1.	git revert HEAD or git revert commitno 

create new branch
1. git branch newbranchname //

switch to new branch or both in one commands
1.	git checkout newbranchname //

to delete branch
1.	git branch -d nameofbranchtodelete

to merge branch go to the parent with which the branch is to bemerged git checkout mainbranch
1.	git merge brnachtobemergedname

to push branch to master remotely
1.	git push -u origin newbranchtobeaddedtorepo














