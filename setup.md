---
layout: page
title: Setup
permalink: /setup/
root: ..
---

### Obtain lesson materials

1. Download [LaTeX_Guided_Course-buildingblocks.zip][buildingblocks].
2. Create a folder called `LaTeX-Intro` on your Desktop.
3. Move downloaded files into this newly created folder.
4. Unzip the files.

You should now see the new folder called `buildingblocks` in your `LaTeX-Intro` directory on your
Desktop.

&nbsp; <!-- vertical spacer -->

### Navigate to the `buildingblocks` folder

If you're using a Unix shell application, such as Terminal app in macOS, Console or Terminal in
Linux, or [Git Bash](https://gitforwindows.org/) on Windows, execute the following command:

~~~
$ cd ~/Desktop/LaTeX-Intro/buildingblocks
~~~
{: .source}

On Windows, you can use its native Command Prompt program.  The easiest way to start it up is by
pressing <kbd>Windows Logo Key</kbd>+<kbd>R</kbd>, entering `cmd`, and hitting <kbd>Enter</kbd>. In
the Command Prompt, use the following command to navigate to the `buildingblocks` folder:
~~~
$ cd /D %userprofile%\Desktop\LaTeX-Intro\buildingblocks
~~~
{: .source}

&nbsp; <!-- vertical spacer -->

### Option 1: Launch Plain Vanilla Text editor

To start working with LaTeX, we need to launch a program that will allow us to edit our LaTeX
commands. This will likely be the default text editor on your system.  In a unix terminal, we will
use the simple `nano` editor.
~~~
$ nano
~~~
{: .source}

To interpret the code we have written, we will need to execute code in the terminal.  We do this with
the `pdflatex` command.
~~~
$ pdflatex %ourTeXfile%
~~~
{: .source}

&nbsp; <!-- vertical spacer -->

### Option 2: Start Overleaf Project

[Overleaf](https://www.overleaf.com/) is an online service which allows for collaborative LaTeX document
creation and editing.  It is free to use for individuals.  On the website, register an account and/or log in.

Start a new document by clicking on `New Project` and choose `Blank Project`.  Enter a title like
`LaTeX-Intro`.

You can edit the document directly on the source page which comes up.  It will compile as you go along.

[zipfile1]: {{ page.root }}/buildingblocks/LaTeX_Guided_Course-buildingblocks.zip.zip
