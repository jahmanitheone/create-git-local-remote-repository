# Create Git Local Remote Repository
Git remote repository is located at:<br/>
/mnt/FTEMP/GITREPOSITORY/

We are going to create a remote project called: firstrepo

cd /mnt/FTEMP/GITREPOSITORY/

Create a directory:<br/>
mkdir firstrepo


### Create Initial Remote Git Repository
Go to remote repository path:<br/>
cd /mnt/FTEMP/GITREPOSITORY

Create Git Init Repository:<br/>
git init --bare firstrepo

A subdirectory  is created:<br/>
firstrepo


### See The Directory Content:
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


### Lets' Look At The Remote Repository State

#### View simple log of changes:<br/>
git log -all

We see:<br/>
fatal: your current branch 'master' does not have any commits yet

Of course nothing has happened yet.


#### View detaild log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

We see:<br/>
Nothing is shown


#### See branches:<br/>
git branch -a

We see:<br/>
Nothing is shown

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

