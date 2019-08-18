# Create A Branch In The Local Repository
My working workspace git project is located at:<br/>
/mnt/FDEV/workspacegit/firstrepo


### Create New Branch
cd /mnt/FDEV/workspacegit/firstrepo


Create a branch called: firstbranch<br/>
git checkout -b firstbranch

We see:<br/>
Switched ta new branch 'firstbranch'

See git status:<br/>
git status

We see:<br/>
<pre>
On branch firstbranch<br/>
nothing tcommit, working tree clean<br/>
</pre>

We are at firstbranch


### Lets' Look At the Local Git Project State
#### See git status:<br/>
git status

We see:<br/>
<pre>
On branch firstbranch<br/>
nothing tcommit, working tree clean<br/>
</pre>

We are at the firstbranch


#### View simple log of changes:<br/>
git log --all

We see:<br/>
<pre>
commit 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (HEAD -> firstbranch, origin/master, master)<br/>
Author: YOURUSERNAME <demo@demo.net>
Date:  Sat Aug 17 22:40:35 2019 -0400<br/>
    Init<br/>
</pre>

We see only the initial git commit.


#### View detailed log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

We see:<br/>
<pre>
*9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (HEAD -> firstbranch, origin/master, master)<br/>
 Init<br/>
  diff --git a/Readme.md b/Readme.md<br/>
  new file mode 100644<br/>
  index 0000000..5f2f16b 
  --- /dev/null<br/>
  +++ b/Readme.md<br/>
  @@ -0,0 +1 @@<br/>
  +1111<br/>
</pre>

#### See branches:<br/>
git branch -a

We see:<br/>
*firstbranch<br/>
  master<br/>
  remotes/origin/master

#### See the directory content:<br/>
ls -a1

We see:
<pre>
.
..
.git
Readme.md
</pre>


