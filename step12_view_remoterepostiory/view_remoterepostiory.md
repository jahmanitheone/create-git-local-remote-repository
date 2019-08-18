# View The Remote Repository Changes
The remote repository project is located at:<br/>
/mnt/FTEMP/GITREPOSITORY/firstrepo


### Lets' Look At the Local Git Project State
cd /mnt/FTEMP/GITREPOSITORY/firstrepo

#### View simple log of changes:<br/>
git log --all

We see:<br/>
<pre>
commit 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (firstbranch)
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>49:<br/>07 2019 -0400
   Changes in the firstbranch
ommit 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (HEAD -> master)
Author:<br/> YOURUSERNAME <demo@demo.net>
Date:<br/>   Sat Aug 17 22:<br/>40:<br/>35 2019 -0400
   Init
</pre>


We see the initial git commit and new commit to branch.

#### View detailed log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline


We see:<br/>
<pre>
* 2fb6dd24b2050eec9db21d481cc0b0b30f577df6 (firstbranch) Changes in the firstbranch
| diff --git a/Readme.md b/Readme.md
| index 5f2f16b..4f142ee 100644
| --- a/Readme.md
| +++ b/Readme.md
| @@ -1 +1,2 @@
|  1111
| +2222
* 9ccd8f999d10e1241ccc72ebe8b6f26ec5c90299 (HEAD -> master) Init
  diff --git a/Readme.md b/Readme.md
  new file mode 100644
  index 0000000..5f2f16b
  --- /dev/null
  +++ b/Readme.md
  @@ -0,0 +1 @@
  +1111
</pre>

We see commits and the details of the changes in the file.

See branches:<br/>
git branch -a

We see:<br/>
<pre>
  firstbranch
* master
</pre>

We see the current branches in the remote repository.


#### See the directory content:<br/>
ls -a1

We see:<br/>
<pre>
.
..
branches
config
description
HEAD
hooks
info
objects
refs
</pre>

The remote repository tracking information.
