
# CREATING A NEW REPO FROM LOCAL (ACTUALLY JUST CONNECTING TO NEWLY CRETAED GITHUB REPO)

zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ nano README.md
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ ls
README.md
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git init
Initialized empty Git repository in /home/zsolt/Desktop/GitHub/demo-repo2/.git/
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git add README.md 
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git commit README.md -m "Created first file in localy created Git repo" -m "If you would like to create a new Git repo you have to create a 1. new folder, 2 cd in to that folder 3. git init 4. git add {file name} 5. git git commit {file name} 6. git push ...  " 
[master (root-commit) 7fb2cd8] Created first file in localy created Git repo
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git status
On branch master
nothing to commit, working tree clean
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git commit README.md 
On branch master
nothing to commit, working tree clean
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git push origin master
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

# THIS MEANS THAT GIT DOESN'T KNOW THIS REPOSITORY ==> WE HAVE TO CREATE IT FIRST.
#  WE HAVE TO CREATE THE NEW REPOSITORY ON GITHUB AND CONNECT THE LOCAL TO THE REPO: 
# Connecting local(origin) to git remote (master)
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git remote add origin https://github.com/suraninarus/demo-repo2.git
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git remote -v
origin  https://github.com/suraninarus/demo-repo2.git (fetch)
origin  https://github.com/suraninarus/demo-repo2.git (push)
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git push master origin
error: src refspec origin does not match any
error: failed to push some refs to 'master'
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git push origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 342 bytes | 342.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/suraninarus/demo-repo2.git
 * [new branch]      master -> master

 # Setting push up so we don't have to type out "origin" and "master" every time for git push 
 # ============================================================================================
 zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ git push -u origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 1.14 KiB | 1.14 MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/suraninarus/demo-repo2.git
   7fb2cd8..e9aba05  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
zsolt@galvatron:~/Desktop/GitHub/demo-repo2$ 


# HERE I WOULD HAVE ADDED THE BRANCHING PART, BUT I CREATED ANOTHER FILE INSTEAD. 

