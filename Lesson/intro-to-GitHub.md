# Introduction to Version Control and GitHub

These materials are inspired and partially based on Software Carpentry's lesson on [Version Control with Git](http://swcarpentry.github.io/git-novice/). 

## Contents

- [Motivation](#motivation)
- [What is version control and why to use it?](#vcs-idea)
- [What is GitHub?]()
- [Resources](#resources)

##<a name='motivation'></a> Familiar?  

![Motivation for version control](../img/version_control_motivation_comics.png)

_Source: “Piled Higher and Deeper” by Jorge Cham_, http://www.phdcomics.com 

**Wouldn't it be nice to learn how to avoid this situation!?!?**

We’ve all been in this situation before: it seems ridiculous to have multiple nearly-identical versions of the same document. 
Some word processors let us deal with this a little better, such as Microsoft Word’s “Track Changes”.

##<a name='vcs-idea'></a> What is version control and why to use it?

###What is it?

[Version control](https://en.wikipedia.org/wiki/Version_control) is used to track and store changes in your files without losing the history of your past changes. 

Version control systems start with a base version of the document and then save just the changes you made at each step 
of the way. You can think of it as a tape: if you rewind the tape and start at the base document, then you can play back 
each change and end up with your latest version.

![Illustration of committing changes](../img/play-changes.PNG)

A version control system is a tool that keeps track of these changes for us and helps us version our files 
_([and merge](https://en.wikipedia.org/wiki/Merge_(version_control) )_- not covered in this course). 
It allows you to decide which changes make up the next version, called a commit, and keeps useful metadata about them. 
The complete history of commits for a particular project and their metadata make up a repository (such as our course material repositories). 
Repositories can be kept in sync across different computers facilitating also collaboration among different people.

There are multiple different Version Control Systems (VCS) (i.e. a software for doing version control) but one of the most popular one is [Git](https://en.wikipedia.org/wiki/Git_(software)
that was created by Linus Torvalds in 2005.  

###Why to use it?

One of the most obvious reasons why to use version control is to avoid the situation illustrated in the [comics above](#motivation), i.e. to keep track of the full 
history of your changes in a systematic way without the need to have multiple versions of the same file. One of the most useful features of version control is the 
ability to "go back in time", i.e. if something goes wrong, you can start from some earlier version of the file when everything was still working. You can also compare
the differences between versions and see what has changed. In addition aforementioned aspects, version control makes possible for multiple people to
work on the same file or project at the same time while still keeping track of their own changes to the files. 
 
###Some basic vocabulary of Version Control

Few basic terms that are used often when discussing about version control (not exhaustive).  

 - **Repository** = a location where all the files for a particular project are stored, usually abbreviated to “repo.” 
 Each project will have its own repo, which is usually located on a server and can be accessed by a unique URL (a link to GitHub page for example).
 
 - **Commit** = To commit is to write or merge the changes made in the working copy back to the repository. 
 The terms 'commit' or 'checkin' can also be used as nouns to describe the new revision that is created as a result of committing.
 
 - **Revision / version** = A revision or a version is any change in made in any form to a document(s). 
  
 - **Clone** = Cloning means creating a repository containing the revisions from another repository. This is equivalent to pushing or pulling 
 into an empty (newly initialized) repository. As a noun, two repositories can be said to be clones if they are kept synchronized, and contain the same revisions.
 
 - **Pull / push** = Copy revisions from one repository into another. Pull is initiated by the receiving repository, while push is initiated by the source. 
 Fetch is sometimes used as a synonym for pull, or to mean a pull followed by an update.
 
 - **Merge** = A merge or integration is an operation in which two sets of changes are applied to a file or set of files.

##<a name='resources'></a> Resources

- [Screencast series in Youtube for learning GitHub](https://www.youtube.com/playlist?list=PL4Q4HssKcxYsTuqUUvEHJ8XxOVOHTSmle) 
- [Tutorial on few extra features of GitHub not (most probably) covered in this course (e.g. branch, pull-request, merge)](https://guides.github.com/activities/hello-world/)