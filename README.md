$ git init
Initialized empty Git repository in C:/Users/Ecc/Downloads/VC Day2/.git/

(master)
$ echo "# Lab 2" > file.txt

(master)
$ git add .
warning: in the working copy of 'file.txt', LF will be replaced by CRLF the next time Git touches it

(master)
$ git commit -m "initial commit"
[master (root-commit) f144c62] initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 file.txt

(master)
$ git remote add origin https://github.com/Hebaade/VC-Day2-Task.git

(master)
$ git branch -M main

(main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 216 bytes | 108.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Hebaade/VC-Day2-Task.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

(main)
$ git checkout -b dev
Switched to a new branch 'dev'

(dev)
$ echo "dev file" > dev.txt

(dev)
$ git add .
warning: in the working copy of 'dev.txt', LF will be replaced by CRLF the next time Git touches it

(dev)
$ git commit -m "add dev file"
[dev 324a327] add dev file
 1 file changed, 1 insertion(+)
 create mode 100644 dev.txt

(dev)
$ git push -u origin dev
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 274 bytes | 137.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Hebaade/VC-Day2-Task/pull/new/dev
remote:
To https://github.com/Hebaade/VC-Day2-Task.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

(dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

(main)
$ git checkout -b test
Switched to a new branch 'test'

(test)
$ echo "test file" > test.txt

(test)
$ git add .
warning: in the working copy of 'test.txt', LF will be replaced by CRLF the next time Git touches it

(test)
$ git commit -m "add test file"
[test c78739f] add test file
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt

(test)
$ git push -u origin test
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 280 bytes | 280.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Hebaade/VC-Day2-Task/pull/new/test
remote:
To https://github.com/Hebaade/VC-Day2-Task.git
 * [new branch]      test -> test
branch 'test' set up to track 'origin/test'.

(test)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

(main)
$ git merge dev
Updating f144c62..324a327
Fast-forward
 dev.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 dev.txt

(main)
$ git merge test
Merge made by the 'ort' strategy.
 test.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt

(main)
$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 323 bytes | 323.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Hebaade/VC-Day2-Task.git
   f144c62..895b819  main -> main

(main)
$ git tag -a v1.7 -m "version 1.7"

(main)
$ git push origin v1.7
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 158 bytes | 79.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Hebaade/VC-Day2-Task.git
 * [new tag]         v1.7 -> v1.7
