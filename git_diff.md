# git diff commands
## BY using git diff command we easily compare file updates into different stages and also different branch 
## diff between working directory and staging area
git diff          

## diff between staging are to local repo
git diff --staged 

## diff between local repo and working directory 
git diff head     

## diff between local repo and remote repo
git diff main origin/main   

## diff between branches example if you are in dev branch it will show diff between dev and main
git diff main    

## show the diff of what is in branchA that is not in branchB
git diff branch-A branch-B