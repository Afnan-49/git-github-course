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
on the outside git is usaully a blank screen, but internally I view it as a labyrinth.
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
It's where the files move when I am done with editing them. to use the taught analogy; it's like placing my groceries in a basket/ trolly, after each choice was made to pick up a product I would collect them in one basket, so that I can check them out all at once.

.git:
Is where the "checkout" happens. 
