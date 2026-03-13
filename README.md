# git and GitHub course
What I Learned During the Course
Table of contents:
git
git Commands
GitHub
GitHub parallel commands to git
Lessons of each day!


What is git?
'git' is a program that stores a database,and is used to organize and manage files, used in inquery, and in communicating with other git databases.
How can I access git?
git is downloaded on every machine. the way you access it is through multiple choices of interfaces, such as the command line, GitHub, Visual Studio Code, and many others.
What will I find?
on the outside git is usaully a blank screen or an organized UI, but internally I view it as a labyrinth.
It starts with the .git file at the root, from there the project expands, if the .git file is not at the root of the project, then git doesn't "see" my project (the working tree).
How is git structured?
git can be maped in three core places or areas and an extra fourth one (so four really):
1- the Working Tree (WT) or the Working Directory (WD)
2- the Index or Stage
3- .git
4- Stash

WT/ WD:
This is the place where I would work on my files. I see it as an active playground in whitch I can minipulate the content of my files, and with each edit the working tree can be described as 'dirty', and when there are no modifications the working tree can be described as 'clean' (but to me it's never actually clean).

the Index/ Stage:
It's where the files move when I am done with editing them. to use the taught analogy; it's like placing my groceries in a basket/ trolly, after each choice was made to pick up a product I would collect them in one basket, so that I can check them out all at once. This is where I would use the command 'git add'

.git:
Is where the "checkout" happens. After adding my modified files in the Stage area, then I am ready to 'commit' them. Placing my files in the .git area (using the command "git commit"); forms let's say a finished product, that you can use with other commits to run a program for example.

Stash:
To me this is the most self-explanitory term, although I didn't know it existed (even when we all needed it). the stash is where I can.. well, stash my files away from the rest of the project and from the rest of the team if I were to be working with one.

To expand the picture of git further, let's place myself inside of that labyrinth and work from there: adding a commit into the .git area forms the "initial commit", and adding another after another commit forms a branch in the visual sense, but there is also a branch that points to the last commit formed (it's automatically called the main of master branch), on top of that branch there's a Head which points to that branch. each one of these commits refers to the one before, so if I want to start a different branch growing from one of the commits in the main branch, each commit there would refer to the one before it untill the root commit, but not the one after the base commit -the new branch from which it formed-.
before moving on to the next section, there are some details concerning commits, and branches; so each commit os named with hash number that is stored in the .git database, and each branch, like the main branch or branch X that moves with the last commit is just a name that helps the human using the machine remeber that branch's name, but to the machine that branch is just another commit with another hash number. It's also worth mentioning that one commit can have two named branches pointing at it, but only one head moves with one named branch at a time. so you can move the Head to the main branch or branch X, but it is the only one there in the entire project/ working tree.

The Objects of git
For us mere mortal humans, we have to name every little thing and signify it as something for us to remember and use it. but for git, it breaks all of the data that we work on into just four simple objects (talk about belittling your efforts, eh). Everthing that we store into git, internally it is just one of those four objects:
- a Commit
- a Tree
- a Blob (binary large object)
- a tag

the commit object:
I forgot to mention earlier that commits are basically a snapshot of my reposotory, since snapshots of my entire project are basically what builds my project, it is within it self an object for git.

the Tree object:
a tree object for git is what the directory or folder is for us. a single directory can store multiple files and multiple directories so in a sense it has many branches, hense why it's called a tree.

the Blob object:
a blob for git, is what a file is for us. whatever that file stores, it is still a blob for git.

the tag object:
I veiw that tag as a marker in a book; it signifies specific (usually important) points the repository's history. The most common use is to tag the latest release of a project.

One of the things that we have learned or relearned in this course, is that to make sure that we understand something and to explain that thing effectevly, it's better for us to come up with a picture that flows with the logic of the information and connects the concepts that we've learned together -because no knowladge or tool in the world is isolated.. so here is a simple picture (albeit from the git docs and not from me) that organizes the connection between each Object:



GitHub:
Github is one of many examples of a remote repository
