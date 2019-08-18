# Clone Local Remote Repository
My working workspace is at:<br/>
/mnt/FDEV/workspacegit


### Clone Remote Branch
Gtmy working workspace tcreate a git project:<br/>
cd /mnt/FDEV/workspacegit

Clone local repository:<br/>
git clone /mnt/FTEMP/GITREPOSITORY/firstrepo

We see:<br/>
Cloning int'firstrepo'...<br/>
warning: You appear thave cloned an empty repository.<br/>
done.

We see ./firstrepis created in the workspaces<br/>

ls -a1

We see:<br/> 
<pre>
.
..
.git
</pre>


###  Lets' Look At the Local Git Project State
#### View simple log of changes:<br/>
git log -all


We see:<br/>
fatal: your current branch 'master' does not have any commits yet

Of course nothing shows up


#### View detaild log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

Nothing shows up



### Lets' Look At The Remote Repository State
#### View simple log of changes:<br/>
git log -all

We see:<br/>
fatal: your current branch 'master' does not have any commits yet

Of course nothing has ppaned yet.


#### View detailed log of changes:<br/>
git log -p -2 --graph --decorate --all --pretty=oneline

We see:<br/>
Nothing is shown


See branches:<br/>
git branch -a

We see:<br/>
Nothing is shown

