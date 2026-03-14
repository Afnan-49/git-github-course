# git and GitHub course
Please read till the end, I wrote this all by myself (except for like the six lines that I got from the README file you have sent and the git docs)

## What I Learned During the Course

## Table of contents:
- git
- GitHub
- git Commands (and their parallel on GitHub)
- more of what I learned -brain dump-


## What is git?
'git' is a program that stores a database, and is used to organize and manage files, used in inquery, and in communicating with other git databases.

### How can I access git?
git is downloaded on every machine. the way you access it is through multiple choices of interfaces, such as the command line, GitHub, Visual Studio Code, and many others.

### What will I find?
on the outside git is usaully a blank screen or an organized UI, but internally I view it as a labyrinth.
It starts with the .git file at the root, from there the project expands, if the .git file is not at the root of the project, then git doesn't "see" my project (the working tree).

### How is git structured?
git can be maped in three core places or areas and an extra fourth one (so four really):

1. the Working Tree (WT) or the Working Directory (WD)
2. the Index or Stage
3. .git
4. Stash

#### WT/ WD:
This is the place where I would work on my files. I see it as an active playground in whitch I can minipulate the content of my files, and with each edit the working tree can be described as 'dirty', and when there are no modifications the working tree can be described as 'clean' (but to me it's never actually clean).

#### the Index/ Stage:
It's where the files move when I am done with editing them. to use the taught analogy; it's like placing my groceries in a basket/ trolly, after each choice was made to pick up a product I would collect them in one basket, so that I can check them out all at once. This is where I would use the command 'git add'.

#### .git:
Is where the "checkout" happens. After adding my modified files in the Stage area, then I am ready to 'commit' them. Placing my files in the .git area (using the command "git commit"); forms, let's say a finished product, that you can use with other commits to run a program for example.

#### Stash:
To me this is the most self-explanitory term, although I didn't know it existed (even when we all needed it). the stash is where I can.. well, stash my files away from the rest of the project and from the rest of the team if I were to be working with one.

---

To expand the picture of git further, let's place myself inside of that labyrinth and work from there:
adding a commit into the .git area forms the "initial commit", and adding another after another commit forms a branch in the visual sense, but there is also a branch that points to the last commit formed (it's automatically called the main or master branch), on top of that branch there's a **Head** which points to that branch.
Each one of these commits refers to the one before, so if I want to start a different branch growing from one of the commits in the main branch, each commit there would refer to the one before it untill the root commit, but not the one after the base commit -the original branch from which the new branch formed-.

---

Before moving on to the next section, there are some details concerning commits, and branches; so each commit is named with a hash number that is stored in the .git database, and each branch, like the main branch or branch X that moves with the last commit is just a name that helps the human using the machine remeber that branch's name, but to the machine that branch is just another commit with another hash number. It's also worth mentioning that one commit can have two named branches pointing at it, but only one head moves with one named branch at a time. so you can move the Head to the main branch or branch X, but it is the only one there in the entire project/ working tree.

--------

### The Objects of git

For us mere mortal humans, we have to name every little thing and signify it as something for us to remember and use it. but for git, it breaks all of the data that we work on into just four simple objects (talk about belittling your efforts, eh). Everthing that we store into git, internally it is just one of those four objects:
- a Commit
- a Tree
- a Blob (binary large object)
- a tag

#### the commit object:
I forgot to mention earlier that commits are basically a snapshot of my reposotory, since snapshots of my entire project are basically what builds my project, it is within it self an object for git.

#### the Tree object:
a tree object for git is what the directory or folder is for us. a single directory can store multiple files and multiple directories so in a sense it has many branches, hense why it's called a tree.

#### the Blob object:
a blob for git, is what a file is for us. whatever that file stores, it is still a blob for git.

#### the tag object:
I veiw a tag as a marker in a book; it signifies specific (usually important) points in the repository's history. The most common use is to tag the latest release of a project.

---------

One of the things that we have learned or relearned in this course, is that to make sure that we understand something and to explain that thing effectevly, it's better for us to come up with a picture that flows with the logic of the information and connects the concepts that we've learned together -because no knowladge or tool in the world is isolated.. so here is a simple picture (albeit from the git docs and not from me) that organizes the connection between each Object:

![image alt](https://github.com/Afnan-49/git-github-course/blob/1e62ef66388303c7535b6b5423df43e7a5818ef8/data-model-3.png)

## GitHub:
Github is a platform in which I and/ or teams can store their data as a backup. It is one of many examples of a remote repository and it's basically another interface for git, just in parallel to commands, there are buttons, arrows, dropdown menues.. etc, interacting with my mouse and keyboard.
Speaking of commands, I'll get into each command and what its core functionality is, and its parallel acton in GitHub:

---

## git commands:

### git init:
To start a project I would intiate a new repository to store that project in by using the command `git init`
the GitHub equivilant to that command is using the button **new reposptory** or **new** after entering the Reposotories page.

### touch:
using the command `touch` (to make a file) or the type of file name (ex: `vi`, `vim`, `nano`):
building a project by adding code or documenting something (usually with the file extention like txt or md) requiers a file to store that data. To create the file I would use the command **touch** and to enter the file I would use the type of the file then the name of the file, ex: 'vi name-of-file-1'
on GitHub, there is a **create file** button on the top right corner of the repository page which will make an empty file appear, but to make a directory I would just add a slash '/' at the end of the name of the file.

I kind of already explained 'git add' and 'git commit' earlier, so I'll move on to the next command.

### git push:
This is a command which is used to sync the commits between the local repository and the remote reposotory. So pushing all the files "upstream".
when I commit a file on GitHub that's basically the two commands `git commit` and `git push` in one command.

### git pull:
Basically the oppsit of git push; pulling part of or all of the project from the remote repository to the local one (downstream).

### ls:
To view the project repository's content. use ls -a to display all files, including hidden ones (such as .git).
on GitHub every file and directory is viewed on the left handside pannel.

### git status:
Shows the status of my working directory and staging area. showing which files are staged, unstaged, or untracked.

### git log:
Shows the history of the commits, all of the metadata of who commited the changes and when.. etc
on GitHub, it can be shown by pressing the '# commits' or 'history' button then it will show the page with all the metadata of the commits and users who commited them.

### git diff:
Used to show the differences between the working directory and the staging area.

### git merge:
merging commits (two at a time) in one branch.

### git branch:
By using the command `git branch -name of branch-` I would create a branch if the name of that branch doesn't exist yet, and by using `git branch` I would list the branches that already exist. Branches allow you to work on different features or fixes without affecting the main codebase.
on GitHub, there's a dropdown menue on the left handside with the name of the active branch

### gitcheckout:
Used to switch between branches or revert files to a previous state.
by using `gitcheckout -name of branch-` I would switch to that branch and make it the active branch.

### git cherry-pick:
This allows me to apply specific commits from one branch to another without merging the entire branch.

### git reset:
Removes files from the staging area, but keeps changes in the working directory.

### git reflog:
If I accidentally reset my branch and lost commits, they may not appear in git log, but they are still in the reflog

### git rebase:
changing the base of a particular branch. so moving a branch into another base, whether it's the tip or in the middle of a given branch.

### git restore:
Restores files to their previous state.

---------

## There are some terms that I want to go over quickly like:

### Squashing:
Combines multiple commits into a single commit. This is often used to clean up a commit history before merging branches.

### Atomic commit:
It doesn't really exist for git but it's a term worth knowing that is used when I commit a simple change like adding a line in a file, each time I do that, that is said to be as commiting atomic commits.

### Fork:
Forking is copying a repository/ project from one GitHub account remote repository into another. and to copy that copy to my local machine; then I need to use the command:

### git clone:
is cloning/ copying a repository/ project from a remote one into my local machine.

### git reset:
moving the Head to a specific commit.
### Types of rests:
### hard:
deletes whatever is in the WT and the index and keeps only the commited changes
### soft:
Leave my working tree files and the index unchanged.
### mixed (default):
Leaves my WT unchanged. Updates the index to match the new HEAD, so nothing will be staged.

### gitignore:
A gitignore file specifies intentionally untracked files that Git should ignore. Files already tracked by Git are not affected.

------------

## Lesson of the day:
I miss writing and I really should work on that Medium account that I never got around to.

## Advice:
This excersise should be at the end of every program (or every part of a program if it's a long one) to help make a personal resource that I can go back to and for others to do so as well. it also helped me realize how much information I was missing and how much I have gained.

## Lessons learned from this program (without going into too much detailes):
- Prospective
- educational institutians vs learning methods
- opinion vs facts
- creating pictures > consuming information
- Solid base first then go into the rest of the journey
- Concept --> Example --> Practice --> Feedback
repeat the process
- as a morally ok scientist would say: "The fact that you could, does not mean that you should"
- trust my instinct in that; I'm not slow, I'm just building a solid base

and sooooo much more

I know this might be just a git and github program from the outside, and the fact that I wasn't accepted into the program should be enough to not make me attend, but I'm so gratful that I evantually did attend because this was one of the better experiences in Tuwaiq Academy.

---

Author: Afnan Mohammed AlFaidi
Thank you!
