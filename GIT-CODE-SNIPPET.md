git clone git@github.com:saspalani/HAT.git
cd HAT
git remove upstream
git remote add upstream git@github.com:QualitySuits/HAT.git
git fetch --all
# rebasing the forked repository
git rebase upstream/master

git mergetool
git add .
git status
git rebase --continue

git push -f origin master



#COMPARING WORKING DIRECTORY AND STAGING AREA
COMMAND : git diff (or) git difftool
USAGE : shows the difference

#COMPARING BETWEEN THE WORKING DIRECTORY AND GIT REPOSITORY(LAST COMMIT)
COMMAND :  git diff HEAD

#COMPARING BETWEEN THE STAGING AREA AND GIT REPOSITORY(LAST COMMIT)
COMMAND :  git diff --staged HEAD

## LIMITING TO ONE FILE
COMMAND : git diff -- README.md<any_file_name_you_want_to_compare>

#COMPARING BETWEEN COMMMITS
COMMAND: git diff <commit_id> <commit_id>

#COMPARING BETWEEN COMMIT AND HEAD
COMMAND: git diff <commit_id> HEAD

#COMPARING BETWEEN LAST TWO COMMITS
COMMAND: git diff HEAD HEAD^

#COMPARING BETWEEN LOCAL MASTER BRANCH(last commit) VS REMOTE MASTER BRANCH
COMMAND: git diff master origin/master

##https://docs.gitlab.com/ee/topics/git/numerous_undo_possibilities_in_git/#undo-local-changes
	#Discard all local changes to all files permanently: git reset --hard
	#iscarding local changes (permanently) to a file: git checkout -- <file>


1. Install visual studio code
2. Install diff tool - compareit
3. Take all the files from your sprint 2 branch using the following command
     How to list all the files in a commit?
     git diff-tree --no-commit-id --name-only -r bf4ceb3de0fb39890baca296f9111e7c7bc842d7
     git show --pretty="" --name-only 17085050
     3.a. Copy the required files to a folder
4. clone master branch in your local
5. find the difference between files collected in step 3 vs files in local master branch using Visual Studio diff tool
6. merge your changes into local master
7. Import your code in eclipse and run the test cases particular to your changes.
8. do a (git pull)
    git pull origin master
9. commit & push your changes in master (IF you are confident)
    git push -m "US-NAME DESC"
10. create a branch after you push the code
    git checkout -b branch_name
    git push origin branch_name
11. delete your old branch
    git branch -d old_branch_name
    git push -f origin old_branch_name
