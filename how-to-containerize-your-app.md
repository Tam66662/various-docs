# How To Containerize Your Application with Docker
So you wrote your amazingly simple console application in some language that you are vaguely familiar with (C#, nodejs, python)...and **IT WORKED!**  Yeah right.  Several tutorials online show you how to containerize these simple apps, but *yours* is a super-complicated service application, and nobody understands the nuances of the code better than the programmer you got it from.

But now you want to containerize it!  OK, let's get started.

## Assumptions
- Your code works.  It's running standalone from a command line interface (CLI) like DOS, Powershell, or Terminal.

## What You Will Need To Download:
- Docker
- Visual Studio Code (to make life easier)

## Let's Do This!

Before we get started, I just want to point out that this training works best if you don't know all the files I need to containerize. Hey, that's you!

For my example, I have a working NODE.js REST server application. Don't know what that is?  Well, good!  It's a headless console app, and runs from my CLI with no problems.  Here are the file contents which you have no clue what does what (again, that's good!):

![](todo:addimage)

Luckily for me, the programmer, I know what files I wrote and what files got automagically downloaded as libraries.  You really only need to containerize the files that are 100% necessary to launch your application.  If this means you *must* have these libraries in your container, then that's an understanding that makes you knowledgeable in your domain more than me!  For my case, I know I don't need these libraries because nodejs will automatically install them for me when I launch.

## Create Your Dockerfile

