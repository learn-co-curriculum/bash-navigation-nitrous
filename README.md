# Navigating with BASH - Nitrous

## Objectives

1. Understand how to navigate your files using Nitrous Console.
2. Use `pwd` to identify the current directory of your  Nitrous Console session.
3. Use `ls` to list the files in the current directory of your  Nitrous Console session.
4. Use `cd` and `cd ..` to change directories of your  Nitrous Console session.

## Overview

When you open a file on your computer, you locate it in by navigating through the directories on your computer' file system using Finder. Even files on your Desktop that you click on are stored in your computer's file system, your hard drive.

When you open an application from your Finder or Desktop, it always happens from the context of a "Working Directory" - the directory of your computer you were in when you executed the program. When you click on a file on your Desktop or Open an application from Your Dock or Applications directory, you are still opening a file in a directory. The Dock and Desktop are just abstractions for that directory to make them easy to access.

We're used to navigating and operating on these files using our GUI, our Graphical User Interface, provided by OSX or whatever operating system we're using (Windows).

Your Nitrous environment is no different, it is a computer in the cloud (aka the internet) and instead of a classical operating system like on your home computer, you access it via a Web Interface in your browser. Without a classical GUI, you have to learn to navigate your files and directories with the Nitrous Console.

**Note: We will begin referring to your Nitrous Console as your Terminal for consistency across curriculum and because a local Terminal and your Nitrous Console are equivalents.**

Our Terminal provides us with a Command Line Interface to navigate and operate on the files and folders in our Nitrous computer. As programmers, the Terminal is our workbench, not the GUI.

Let's learn to navigate the files and folders on your Nitrous using the Terminal Command Line Interface.

## `pwd` and Working Directories

When you open Nitrous, your Terminal is open to a location within a directory of the file system on your Nitrous. Whatever programs you execute or work you do in your Terminal, like when you click on things in your GUI, that action happens in the context of a "Working Directory."

A "Working Directory" just means wherever on your Nitrous' hard drive you are when you execute a program by running a command in your Terminal like `learn hello`. You did that from somewhere. We call that somewhere, wherever you currently are, a "Working Directory".

Open a Terminal and you'll be at your Command Line prompt, where your computer is waiting for instructions.

### What's a Command Line Prompt

Our Command Line prompt, and maybe yours if you configured you environment through Learn, is represented by:

```
➜  ~
```

The first character, `➜` is just telling us we're at a Command Line prompt. The `~` is your current working directory, `~`, which means our Home directory, the default directory for you. We'll explain that idea of a home directory or `~` in a moment.

More generally, the command line prompt is represented by a `$`.

If you've read other tutorials, you might be familiar with seeing command line instructions with a `$` to represent the prompt. We try to follow this convention in our instructions but you might sometimes see `// ♥` in images or code samples.

What can you do from a command line prompt? Everything and anything. A command line prompt is the most powerful interface in the world, from which every computer and piece of software can be created, controlled, molded, manipulated, and used.

### `pwd` - Print Working Directory

Let's run our second Command Line program (our first was when you ran `learn hello`).

Type `pwd` from your prompt. You should see something like:

```
➜ ~ pwd
/home/nitrous
➜ ~
```

From my home directory, `~`, my Terminal presented me a prompt, `➜`. I typed `pwd` and pressed Enter on my keyboard. My terminal responded with `/home/nitrous` and returned me to my home directory, `~` and gave me a new prompt, `➜`.

That's the standard procedure when you execute anything in Terminal, you enter a command from a prompt in a working directory, see output, and are returned to a new prompt in your working directory.

The `pwd` command is an acronym for "Print Working Directory." The `pwd` command prints the working directory of your Terminal session, the folder you are currently "in."

Knowing what directory you are working within is crucial when using your Terminal. You are opening files and running programs that live in directories and you need to make sure you're in the right directory for your task.

You never need to guess. If you're ever curious where you are or if you need to confirm you are where you think you are, type `pwd`.

#### `~` - Your Home Directory

When you open a new Terminal session, you start in a default location in your file system called your Home Directory.

On Nitrous, your home directory is within a folder `home` in the root, or top level, main directory, of the Nitrous hard drive, represented by `/`.

'/' means the main directory of your hard drive. Every file and folder on your Nitrous lives somewhere inside of `/`.

The `~` (tilde) character is just a shortcut for your home directory, whatever it may be. Whenever you see your working directory or a file system path with a `~`, you're home.

There's no place like `~`.
![No Place Like Home](http://learn-co-videos.s3.amazonaws.com/learn-co-orientation/no-place-like-home.gif)

## `ls` - Listing Files in a Directory

Within a directory, one thing you're probably curious about is "what files are in this directory?". You can list files within your working directory by executing `ls`:

```
➜ ~ ls
code   		    
```

When we type `ls` in Terminal, we're asking our Terminal to list the files and folders in the current working directory.

In my home directory, `~` (which is really `/home/nitrous`), I have 1 directory, `code`. You might have more.

## `cd` - Changing Directories

When you open a new Terminal session, you'll be in a working directory, probably your home directory, `~`. But how do we move around to other directories and change our working directory? You can use the `cd` command, which stands for Change Directory.

From your home directory, try:

```
➜  ~ cd code
➜  code
```

From within `~`, our home directory, at our prompt `➜`, we type `cd code`. Our terminal will change the directory and enter our `code` folder and our prompt will now indicate that our working directory is `code`. Your prompt might look a little different but you'll be in your `code` directory. Confirm with: `➜ pwd` (remember don't actually type `➜`). `pwd` should output something like: `/home/nitrous/code`, the full path to your code directory.

Once your working directory is `code`, try `ls` and have your Terminal list any files that are in that directory (probably is empty).

### `..` and `.`

How do you move from `code` back up to your home directory? You can always move out of the current folder and back into the parent folder by typing `cd ..`. Just like `~` is a shortcut for home directory, `..` is a shortcut that always means "the directory above" or the "parent directory" of the current. Your file system is a tree like structure, with directories being inside other directories:

```
├── home
    ├── nitrous
       └── code
```

`code` is within `nitrous` which is within `home` which is at the top of my hard drive, the root, `/`. The path to your `code` is: `/home/nitrous/code`. From within `code`, you would refer to the parent directory, `nitrous` as `..`.

### cd `~`

You can also change directory back to your home directory from anywhere via `cd ~`. Remember that `~` is a shortcut that means home so if you type `cd ~` you are telling your terminal to change the working directory to your home directory.

### Hint: Tab Autocomplete

When you're in Terminal, to autocomplete a directory or a command, start typing and then press TAB.
