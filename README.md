# hello
go through github guide
1. git init

2. git status

3. git add octocat.txt // add this file to staging area

4. git commit -m "add cate file story" // store to local repo

5. git add '*.txt' // use wild card to add all the txt files

6. git commit -m 'Add a bunch of files'

7. git log // log of commits

8. git remote add origin https://github.com/try-git/try_git.git  // create a remote repo with the url which is at github server

9. git push -u origin master // push the commits on local branch master to the remote repo named origin, -u memorizes

10. git pull origin master // pull changes from origin that are made on master

11. git diff HEAD // head is pointer to the last change

12. git add octofamily/octodog.txt // add this txt file to staging

13. git diff --staged // show staged diff 

14. git reset octofamily/octodog.txt  // unstaging this txt file

15. git checkout -- octocat.txt // get rid of all the changes since the last commit for octocat.txt

16. git branch clean_up  // create a branch named clean_up for working on a specific task

17. git checkout clean_up  // switch the branch to clean_up

18. git rm '*.txt'  // remove all the txt files and stage the removal

19. git commit -m "remove all the txt files"  // commit the staged removal

20. git checkout master  // switch back to branch master

21. git merge clean_up  // merge all the commits in clean_up to master

22. git branch -d clean_up  // delete this branch since the task is done in branch clean_up

23. git push  // push master to remote url



                               git stash
--------------------------- ---------------------------------------------------
1. git stash  // usuaully used with git status, saves uncommited changes 

2. git stash pop  // apply all the changes and removes them from stash

3. git stash apply  // apply the cahnges and also kepp them

4. by default Git won't stash changes made to untracked or ignored files

5. git stash -u  // tells git stash to also stash untracked files

6. git stash -a(or --all)   // stash also ignored files

7. git stash list  // show multiple stashes

8. git stash save "any description" // give this stash a name so that it's easy to find in stash list

9. git stash pop  // by default it re-apply the most recent stash

10. git stash pop stash@{2}   // re-apply the stash numbered 2

11. git stash show // view a summary of a stash

12. git stash show -p(or --patch)  // view the full diff of a stash

13. git stash -p(or --patch)   // it will iterate through each changed hunk and ask whether you wish to stash it

14. ctrl -c aborts the stash process

15. git stash branch add-style stash@{1}  // create a branch named add-style from stash@{1}

16. git stash drop stash@{1}  // clean this stash

17. git stash clear // clean all stashes



----------------------------------------------------------------------------------------------
1. git checkout master-staging    // switch to branch master-staging

2. git pull  // pull the latest code from master staging

3. git checkout feature/RICE-18708  // switch to feature branch

4. git merge master-staging   // merge all the lastest changes to feature branch




 
