# Add Content TLocal  Repository
My working workspace git project is located at:<br/>
/mnt/FDEV/workspacegit/firstrepo


### Add Content TCloned Repository
cd /mnt/FDEV/workspacegit/firstrepo

Create a Readme.md file
touch Readme.md

Add "first line" tfile:<br/>
echo 1111 > Readme.md

See the content:<br/>
cat Readme.md

We see:<br/> 
1111
:

### View The Local Git Project State
See git status:<br/>
git status

We see files staged but untracked:<br/>
Untracked files:<br/>
Readme.md



### Commit Changes TLocal Git Repository
Add changes tgit for commit:<br/>
git add --all

Commit changes in git repository:<br/>
git commit -m "Init"

We see:<br/>
<pre>
[master (root-commit) 89b4e41]
 Init
 1 file changed, 1 insertion(+)
 create mode 100644 Readme.md
</pre>



### Push Changes TLocal Remote Repository
push changes<br/>
git push

We see:<br/>
<pre>
Writing objects: 100% (3/3), 217 bytes | 217.00 KiB/s, done.
. . .
T /mnt/FTEMP/GITREPOSITORY/firstrepo
 * [new branch]      master -> master
</pre>


### Lets' Look At the Local Git Project State
See git status:<br/>
git status

We see:<br/>
<pre>
On branch master
Your branch is up tdate with 'origin/master'.
nothing tcommit, working tree clean
</pre>

#### View simple log of changes:<br/>
git log --all

We see:<br/>
<pre>
commit 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (HEAD -> master, origin/master)
Author: YOURUSERNAME <demo@demo.net>
Date: Sat Aug 17 22:40:35 2019 -0400
    Init
</pre>

#### View detaild log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

We see:<br/>
<pre>
 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (HEAD -> master, origin/master) Init
  diff --git a/Readme.md b/Readme.md
  new file mode 100644
  index 0000000..5f2f16b
  --- /dev/null
  +++ b/Readme.md
  @@ -0,0 +1 @@
  +1111
</pre>

#### See branches:<br/>
git branch -a

We see:<br/>
<pre>
* master
  remotes/origin/master
</pre>

See the directory content:<br/>
ls -a1

We see:<br/>
<pre>
.
..
.git
Readme.md
</pre>
