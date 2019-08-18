# Make A Git Branch The Master Branch
We are going to change the brach to the master branch.

Go back to master<br/>
cd /mnt/FDEV/workspacegit/firstrepo

git checkout master


#### View the Readme.md content:
cat Readme.md

We see, we are back to:<br/>
1111


## Reset master forcefully to the branch
git reset --hard firstbranch

We see:<br/>
HEAD is now at 2fb6dd2 Changes in the firstbranch

See the branch we are at:<br/>
git branch -a


We see we arem still at master:<br/>
<pre>
  firstbranch
* master
  remotes/origin/firstbranch
  remotes/origin/master
</pre>

## Push Reset To Remote Repository
git push -f origin master


We see:<br/>
<pre>
Total 0 (delta 0), reused 0 (delta 0)
To /mnt/FTEMP/GITREPOSITORY/firstrepo
   9ccd8f9..2fb6dd2  master -> master
</pre>


## Lets' Look At the Local Git Project State
See git status:<br/>
git status

We see:<br/>
<pre>
On branch master
Your branch is up to date with 'origin/master'.
nothing to commit, working tree clean
</pre>

#### View simple log of changes:<br/>
git log --all

We see:<br/>
<pre>
commit 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (HEAD -> master, origin/master, origin/firstbranch, firstbranch)
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>49:<br/>07 2019 -0400
    Changes in the firstbranch
commit 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>40:<br/>35 2019 -0400
    Init
</pre>

Note:<br/>
	Head is pointing to -> master
	With information on the branch changes:<br/>
		origin/master, origin/firstbranch, firstbranch
	
	Plus we see the commit messages.


#### View detailed log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

We see:<br/>
<pre>
* 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (HEAD -> master, origin/master, origin/firstbranch, firstbranch) Changes in the firstbranch
| diff --git a/Readme.md b/Readme.md
| index 5f2f16b..4f142ee 100644
| --- a/Readme.md
| +++ b/Readme.md
| @@ -1 +1,2 @@
|  1111
| +2222
* 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 Init
  diff --git a/Readme.md b/Readme.md
  new file mode 100644
  index 0000000..5f2f16b
  --- /dev/null
  +++ b/Readme.md
  @@ -0,0 +1 @@
  +1111
</pre>

We see commits and the details of the changes in the file.


####  See branches:<br/>
git branch -a


We see:<br/>
<pre>
  firstbranch
* master
  remotes/origin/firstbranch
  remotes/origin/master
</pre>

We are at master with information of the branches:<br/>
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

## See That Master Has The firstbranch Changes
#### View the Readme.md content:<br/>
cat Readme.md

We see, the initial and the firstbranch change:<br/>
<pre>
1111
2222
</pre>
Success!




