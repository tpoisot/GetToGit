#t
fork you!!!!

MODIF

`git` is a version control system: it lets you control the version of things. It
also lets you collaborate with other people, track what you have been doing on
a code, keep backup, and a lot of other cool and useful and productive things.
It's extremely useful for

i) people working with code
ii) people working on manuscripts (if you write them in `LaTeX` or `markdown`, which you should)

Using `git` is really straightforward, *but* require to use the command line.
During the trainign session, we'll go through the different commands we need to
use. We'll also keep on updating this document, and turn it into a page for the
group [wiki](http://github.com/TheoreticalEcosystemEcology/LabProjects/wiki).

## Creating a project on github

The first thing to do is to go on *github* and create a project. With your free
account, you can only create *open* projects (everyone can see what you are
doing). The lab also has an account, with some *private* projects. Only the
holy trinity of super users (Dom, Philippe, and Tim) can create these projects.

## Setting things up on your computer

If you want to clone this project (it's formally called a *repository*, or
*repo* for short), there are two solutions. First, you don't want to
contribute, you only want to get the content:

```
git clone git://github.com/tpoisot/GetToGit.git
```

This line will create a folder called `GetToGit` in whichever folder you are
currently into with your terminal. You can then `cd GetToGit` to go into the
folder.

The other situation is that you want to collaborate on the project. To do that,
you need to (i) know the address of the repo, and (ii) make sure that you
have the rights to access it. In the case of a private (lab) repo, it means
sending Tim an email with your project name, and getting a URL and the
access back.

If everything is fine, you can just type

```
git clone https://github.com/tpoisot/GetToGit.git
```

The only thing that changed is that we access a secure version of the
repository, so we'll be able to send changes to it.

At this point, if you `ls -la` in the repository, you should see a `README.md`
file (*github* creates those for you), and a folder called `.git`. Don't go
there. 

## Putting your code in the folder

Once you have cloned the repo, you can start adding your code/manuscript. Just
`mv`, `cp`, or drag-and-drop everything in the folder. Now, you can start using
`git`. To see if anything happened, just type

```
git status
```

You should see a lot of things going on. Let's walk through them.

## Sending your code to the server

The first thing you need to do is to tell `git` which files he should monitor
for change. The command is relatively simple:

```
git add myfile.ext
```

Try to do a `git status` immediately after, and see what changed. If you want to
add a lot of files at once (you just copied your project in the repo), you can
do `git add .`. Note that the wildcard operator is `.`, not `*`.

The opposite of `add` is `rm`, and keep in mind that it not only `rm`s the file
from `git`, but also from your computer.

This command only told `git` to look for changes in different files. We need to
send the modifications to the server. 

## A brief aside: the`.gitignore`
