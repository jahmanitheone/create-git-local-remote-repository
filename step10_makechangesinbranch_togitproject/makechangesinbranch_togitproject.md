# Making Changes TThe Local Repository
My working workspace git project is located at:<br/>
/mnt/FDEV/workspacegit/firstrepo


#### Make A File Change In The Branch
cd /mnt/FDEV/workspacegit/firstrepo:

Add "second line" tfile:<br/>
echo 2222 >> Readme.md

See the content:<br/>
cat Readme.md

We see:<br/> 
<pre>
1111
2222
</pre>



#### View The Local Git Project State
See git status:<br/>
git status


We see files staged but untracked:<br/>
<pre>
On branch firstbranch
Changes not staged for commit:<br/>
	modified:<br/>   Readme.md
nchanges added tcommit (use "git add" and/or "git commit -a")
</pre>


#### Commit Changes TLocal Git Repository
Add changes tgit for commit:<br/>
git add --all

Commit changes in git repository:<br/>
git commit -m "Changes in the firstbranch"

We see:<br/>
<pre>
[firstbranch 2fb6dd2] Changes in the firstbranch
 1 file changed, 1 insertion(+)
</pre>


#### Lets' Look At the Local Git Project State

#### See git status:<br/>
git status

We see:<br/>
<pre>
On branch firstbranch
nothing tcommit, working tree clean
</pre>

We are at the firstbranch


#### View simple log of changes:<br/>
git log --all

We see:<br/>
<pre>
commit 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (HEAD -> firstbranch)
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>49:<br/>07 2019 -0400
    Changes in the firstbranch

commit 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (origin/master, master)
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>40:<br/>35 2019 -0400
    Init
</pre>

We see the initial git commit and new branch commit.


#### View detailed log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

We see:<br/>
<pre>
* 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (HEAD -> firstbranch) Changes in the firstbranch
| diff --git a/Readme.md b/Readme.md
| index 5f2f16b..4f142ee 100644
| --- a/Readme.md
| +++ b/Readme.md
| @@ -1 +1,2 @@
|  1111
| +2222
* 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (origin/master, master) Init
  diff --git a/Readme.md b/Readme.md
  new file mode 100644
  index 0000000..5f2f16b
  --- /dev/null
  +++ b/Readme.md
  @@ -0,0 +1 @@
  +1111
</pre>

We what was changed in the file.


#### See branches:<br/>
git branch -a

We see:<br/>
<pre>
* firstbranch
  master
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


#### Push Branch TRepository
Push branch changes trepository:<br/>
git push --set-upstream origin firstbranch

We see:<br/>
<pre>
Writing objects:<br/> 100% (3/3), 264 bytes | 264.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
T/mnt/FTEMP/GITREPOSITORY/firstrepo
 * [new branch]      firstbranch -> firstbranch
Branch 'firstbranch' set up ttrack remote branch 'firstbranch' from 'origin'.
</pre>


#### Lets' Look At the Local Git Project State

#### See git status:<br/>
git status

We see:<br/>
<pre>
On branch firstbranch
nothing tcommit, working tree clean
</pre>

We are at the firstbranch.


#### View simple log of changes:<br/>
git log --all


We see:<br/>
<pre>
commit 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (HEAD -> firstbranch, origin/firstbranch)
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>49:<br/>07 2019 -0400
    Changes in the firstbranch

commit 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (origin/master, master)
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>40:<br/>35 2019 -0400
    Init
</pre>

We see the initial git commit and new commit tbranch.


#### View detailed log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

We see:<br/>
<pre>
* 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (HEAD -> firstbranch, origin/firstbranch) Changes in the firstbranch
| diff --git a/Readme.md b/Readme.md
| index 5f2f16b..4f142ee 100644
| --- a/Readme.md
| +++ b/Readme.md
| @@ -1 +1,2 @@
|  1111
| +2222
* 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (origin/master, master) Init
  diff --git a/Readme.md b/Readme.md
  new file mode 100644
  index 0000000..5f2f16b
  --- /dev/null
  +++ b/Readme.md
  @@ -0,0 +1 @
  +1111
</pre>

We see commits and the details of the changes in the file.


#### See branches:<br/>
git branch -a

We see:<br/>
<pre>
* firstbranch
  master
  remotes/origin/firstbranch
  remotes/origin/master
</pre>


We now have a twremote branches:<br/>
<pre>
remotes/origin/firstbranch
remotes/origin/master
</pre>


#### See the directory content:<br/>
ls -a1

We see:<br/>
<pre>
.
..
.git
Readme.md
</pre>


#### Go Back To Master Branch
Checkout the master branch:<br/>
git checkout master

We see:<br/>
<pre>
Switched tbranch 'master'
Your branch is up tdate with 'origin/master'.
</pre>

git status

We see:<br/>
<pre>
On branch master
Your branch is up tdate with 'origin/master'.
</pre>

git branch -a

We see:<br/>
<pre>
  firstbranch
* master
  remotes/origin/firstbranch
  remotes/origin/master
</pre>

See we  are at master branch

View the Readme.md content:<br/>
cat Readme.md

We se, we are back to:<br/>
1111

The firstbranch is not in the file


Go back tthe branch:<br/> firstbranch
git checkout firstbranch

We see:<br/>
Switched tbranch 'firstbranch'<br/>
Your branch is up tdate with 'origin/firstbranch'.

View the Readme.md content:<br/>
cat Readme.md

We se, we are back to:<br/>
<pre>
1111
2222
</pre>

Checkout the master branch:<br/>
git checkout master

