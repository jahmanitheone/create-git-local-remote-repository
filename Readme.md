# Create Git Local Remote Repository

We can have our own GitHub in our local computer. 
Naah! Not really. 

We can however have a local remote repository using:<br/> 
git init --bare.

### Normal Git Repository
The git init command creates a new Git repository. To be exact a 
local git repository. Executing git init creates a subdirectory:<br/>
.git 

The command for git init in a directyory:<br/>
git init .

This git repository is hard to share amongst different users.



### Share Git Repository
The git init command can also be used to create a new Git repository
that can be shared. We add the --bare to the git init command. It
does not creaate a ./git directory, but a list of directories:
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

The command for git init shared directyory is:<br/>
git init --bare .


This git repository easilly share amongst different users.



### The Point To Be Made
For local repository use: git init .
For shared local repository use:<br/> git init --bare .



