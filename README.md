# Navigating with BASH - Nitrous

## Objectives

1. Understand how to navigate your files using Terminal.
2. Use `pwd` to identify the current directory of your Terminal session.
3. Use `ls` to list the files in the current directory of your Terminal session.
4. Use `cd` and `cd ..` to change directories of your Terminal session.
5. Use `open .` to open the current directory of your Terminal session in Finder.
6. Use `subl .` to open the current directory in Sublime Text.

## Overview

When you open a file on your computer, you locate it in by navigating through the directories on your computer' file system using Finder. Even files on your Desktop that you click on are stored in your computer's file system, your hard drive.

When you open an application from your Finder or Desktop, it always happens from the context of a "Working Directory" - the directory of your computer you were in when you executed the program. When you click on a file on your Desktop or Open an application from Your Dock or Applications directory, you are still opening a file in a directory. The Dock and Desktop are just abstractions for that directory to make them easy to access.

We're used to navigating and operating on these files using our GUI, our Graphical User Interface, provided by OSX. Our Terminal provides us with a Command Line Interface to navigate and operate on the files and folders of our computer, just like the GUI. As programmers, the Terminal is our workbench, not the GUI.

Let's learn to navigate our computer using the Terminal Command Line Interface.

## `pwd` and Working Directories

When you open a Terminal session, you are placed within a directory of your file system. Whatever programs execute or work you do in your Terminal, like when you click on things in your GUI, that action happens in the context of a "Working Directory."

A "Working Directory" just means wherever on your computer's hard drive you are when you execute a program, again, whether through clicking on an icon in your GUI or running a command in your Terminal like `learn hello`. You did that from somewhere. We call that somewhere, wherever you currently are, a "Working Directory".

Open a Terminal and you'll be at your Command Line prompt, where your computer is waiting for instructions.

### What's a Command Line Prompt

Our Command Line prompt, and maybe yours if you configured you environment through Learn, is represented by:

```
[16:19:43] ~
// ♥
```

The first line, `[16:19:43] ~` is telling us the current time, so expect that part to be different for you, and our current working directory, `~`, which means our Home directory, the default directory for you. We'll explain that idea of a home directory or `~` in a moment.

The next line, `// ♥` is our command line prompt, where we can type instructions and commands for our computer to execute. `// ♥` is a customized prompt that you got by setting up your environment through Learn. To us the symbols `// ♥` remind us of the way, '//', of love, '♥'. That's our mantra when we're programming. And we think it looks pretty cool given how much time we spend in our Terminal.

More generally, the command line prompt is represented by a `$`.

If you've read other tutorials, you might be familiar with seeing command line instructions with a `$` to represent the prompt. We try to follow this convention in our instructions but you might sometimes see `// ♥` in images or code samples.

What can you do from a command line prompt? Everything and anything. A command line prompt is the most powerful interface in the world, from which every computer and piece of software can be created, controlled, molded, manipulated, and used.

### `pwd` - Print Working Directory

Let's run our second Command Line program (our first was when you ran `learn hello`).

Type `pwd` from your prompt. You should see something like:

```
~
 $ pwd
/Users/avi
~
$
```

From my home directory, `~`, my Terminal presented me a prompt, `$`. I typed `pwd` and pressed Enter on my keyboard. My terminal responded with `/Users/avi` and returned me to my home directory, `~` and gave me a new prompt, `$`.

That's the standard procedure when you execute anything in Terminal, you enter a command from a prompt in a working directory, see output, and are returned to a new prompt in your working directory.

The `pwd` command is an acronym for "Print Working Directroy." The `pwd` command prints the working directory of your Terminal session, the folder you are currently "in."

Knowing what directory you are working within is crucial when using your Terminal. You are opening files and running programs that live in directories and you need to make sure you're in the right directory for your task.

You never need to guess. If you're ever curious where you are or if you need to confirm you are where you think you are, type `pwd`.

#### `~` - Your Home Directory

When you open a new Terminal session, you start in a default location in your file system called your Home Directory. When you use your computer, you are logged in under a user account, you're familiar with this as OS X asks you for your user's password occasionally.

Every user on your computer is given a "Home Directory" for their files. Your operating system, OS X, uses this "Home Directory" to keep your files private from other users that might share your computer.

On OS X, user home directories are stored within a folder `Users` in the root, or top level, main directory, of your harddrive, represented by `/`.

'/' means the main directory of your hard drive. Every file and folder on your computer lives somewhere inside of `/`.

`/Users` is the main `Users` directory in OS X. Within `/Users`, there is a folder for your username, the name of the account you use to login to your computer. My username is `avi` so my home directory is: `/Users/avi`. Yours will be different and you can see it by opening a new Terminal session and typing `pwd`.

The `~` (tilde) character is just a shortcut for your home directory, whatever it may be. Whenever you see your working directory or a file system path with a `~`, you're home.

There's no place like `~`.
![No Place Like Home](http://learn-co-videos.s3.amazonaws.com/learn-co-orientation/no-place-like-home.gif)

## `ls` - Listing Files in a Directory

Within a directory, one thing you're probably curious about is "what files are in this directory?". You can list files within your working directory by executing `ls`:

```
~
$ ls
Applications  Development   Desktop
Documents     Downloads     Public        		    
```

When we type `ls` in Terminal, we're asking our Terminal to list the files and folders in the current working directory.

In my home directory, `~` (which is really `/Users/avi`), I have 6 directories, `Applications`, `Development`, `Desktop`, `Documents`, `Downloads`, and `Public`. You probably have more.

## `cd` - Changing Directories

### `..` and `.`

## `open ` - Opening Folders and Files

## `subl` - Opening Folders and Files in Sublime Text
