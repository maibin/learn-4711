# Frequently Asked Questions - Devops
COMP4711 - BCIT - Fall 2017

This FAQ addresses the most common problems encountered
trying to develop webapps as part of this course.

##Webapp testbed

It is possible to setup a testbed that closely matches
your deployment environment.

### VirtualBox with a VDI setup with Linux & Apache

Setup a VirtualBox, with a suitable Linux distro (eg CentOS6)

### Vagrant on top of VirtualBox

Vagrant is a tool that sits on top of VirtualBox. 
It makes the runnning VirtualBox easer, and has provision to setup your project
inside, for testing.

### Docker container

Docker is an emerging devops processing pipeline manager.
I don't know enough to help you with it, but plan to experiment.

## GPG Signing  

Some of the students are experiencing signing issues - "gpg failed to sign...".  
- Workaround: Until we get that resolved, you may use signed-off by messages, but make sure that 
your username matches your git login. 
- Caution: Be careful that your local and global user 
names and email are the same! 
- Solution? Some of the students were using out-of-date versions of gittool,
and I suggest upgrading to the most recent. Not sure if that will solve
all the problems, but it seems to help.

## Git deployment

I have an automatic deployment server that you can use to test your project
webapp. You configure your project on my server, and add
a webhook to your github repo.
Then, whenever you merge to your team repo, that triggers a git pull on my VPS
to deploy your webapp for testing :-/

##Repo Hiccups

### Does your IDE metadata appear in your repo?

You should git ignore the IDE metadata folder(s). That would be <code>nbproject</code>
in NetBeans, or <code>.idea</code> using PHPstorm. You need to do this before making
a commit that would include them, or else they will be a pain to git ignore later.

### Why don't my contributions get counted correctly?

If you see one or two commits with the proper avatar, and the rest have the avatar grayed out,
you need to make sure that your "signing name" matches your github user name.

Alternately, you could GPG-sign your commits, though that is not expected yet.

If you set your signing user name & email globally, you wont have to change it for
each project.
