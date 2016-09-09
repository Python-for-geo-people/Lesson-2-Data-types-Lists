# Introduction to Version Control and GitHub

These materials are inspired and partially based on Software Carpentry's lesson on [Version Control with Git](http://swcarpentry.github.io/git-novice/). 

## Contents

- [Motivation](#motivation)
- [What is version control and why to user it?](#vcs-idea)
- [What is GitHub?]()
- [Resources](#resources)

##<a name='motivation'></a> Familiar?  

![Motivation for version control](../img/version_control_motivation_comics.png)

_Source: “Piled Higher and Deeper” by Jorge Cham_, http://www.phdcomics.com 

**Wouldn't it be nice to learn how to avoid this situation!?!?"

We’ve all been in this situation before: it seems ridiculous to have multiple nearly-identical versions of the same document. 
Some word processors let us deal with this a little better, such as Microsoft Word’s “Track Changes”.

##<a name='vcs-idea'></a> What is version control and why to use it?

Version control is used to track and store changes in your files without losing the history of your past changes. 

Version control systems start with a base version of the document and then save just the changes you made at each step 
of the way. You can think of it as a tape: if you rewind the tape and start at the base document, then you can play back 
each change and end up with your latest version.

![Illustration of committing changes](../img/play-changes.svg)

A version control system is a tool that keeps track of these changes for us and helps us version our files (_and merge_ - not covered in this course). 
It allows you to decide which changes make up the next version, called a commit, and keeps useful metadata about them. 
The complete history of commits for a particular project and their metadata make up a repository (such as our course material repositories). 
Repositories can be kept in sync across different computers facilitating also collaboration among different people.


##<a name='resources'></a> Resources

- [Screencast series in Youtube for learning GitHub](https://www.youtube.com/playlist?list=PL4Q4HssKcxYsTuqUUvEHJ8XxOVOHTSmle) 
- [Tutorial on few extra features of GitHub not covered in this course (e.g. branch, pull-request, merge)](https://guides.github.com/activities/hello-world/)