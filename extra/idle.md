# Entering Code

If learning python seemed daunting enough (hopefully by now we've dispelled this myth!) then you might be even more overwhelmed to learn that there are many ways to input your code into python! Try not to be, it doesn't matter how you input your code, however in this document we'll try to teach you some alternative (but equivalent!) ways to make your lives easier.

Below we list two methods to:
* Use the interpreter; the interpreter is where you can directly type in python code and quickly play around with the language. This is a great way to start using many languages, get a feel for them, and try out new code ideas.
* Write scripts; scripts let you save code you've worked hard on so you can use it later. This is especially important when your projects become fairly large and you don't want to have to remember and retype your code each time. It's also a good practice to start writing most code in script form when you're comfortable.

To begin, first ensure you've installed python by following the steps in our `preparation.md` document.

## The terminal

If you've followed our preparation instructions, this is probably how you're currently interfacing with python. Knowing how to use the terminal is a very valuable skill, and you don't need to know much in order to use it effectively. However, there are quite a few new concepts so if you want a more familiar approach feel free to skip to the IDLE section below!

### Windows

In Windows, the terminal is called the 'command prompt', 'command line' or 'cmd'. To launch it, you can search for it in your start menu/start screen in new versions of windows. In older versions of Windows, you can navigate to Start, All Programs, Accessories and click 'Command Prompt'.

The command prompt is another way to interface with the files and (some) programs on your computer. The main programs we're going to want to use here are `cd`, `dir` and `python`.

#### Getting used to the command prompt

* `cd` is a command used to find out where you are in your files and folders and to navigate between them
* `dir` is a command used to list what files are in the current folder

First, let's try finding out where we are, just type `cd` and press enter (note that terminals, like programming languages, are fairly strict on how you type things because they're stupid; remember to type things exactly as you see them!). You should find you're somewhere like `C:\Users\Me` (it varies across versions of windows so don't worry too much if it's nto exactly the same).

Now let's find where we can go; type `dir` and press enter to give some information about where we are, especially a list of what files and folders there are in the current folder (also known as a 'directory'). You'll notice that entries are listed line by line with a date and time, a column that says whether something is a folder or not (`<DIR>`), a column for filesizes, and the actual file/folder name.

Let's try navigating to the desktop, you should see `Desktop` listed amongst the entries; To go there, just type `cd Desktop` and press enter. Assuming everything went well you'll now be on your desktop! Try running `dir` again to see what's in there.

You may have noticed some strange `.` and `..` entries near the top of the `dir` output. These are special folders and correspond to the current folder and 'parent' folder respectively. The parent folder is the folder one level above where you are, so by typing `cd ..` you can go up one level!

Practice finding your way around your files for a bit.

#### Running the python interpreter

As mentioned in the preparation document, running python should be as simple as typing `python` and pressing enter. Some lines will be printed, including the version of python. This should be 3.something, though in some cases (such as if you've got multiple versions installed), it may be a smaller number, e.g. 2.7. If this is the case, try exiting (type `exit()` or press ctrl-Z) and running `py -3` instead.

Now you should be presented with a `>>> ` 'prompt', where you can type in python code and have it run (after pressing enter). You are now ready to go on with the workshop!

#### Writing scripts

As mentioned earlier, writing scripts allows you to save all your hard work! Script files are plain text files, which means you can't use Microsoft Word or similar to create them, nor can you use things such as bold or italics or any other 'rich formatting'. First, let's open up a text editor:

* You already have one installed, called Notepad. You can launch this from the start menu/screen by searching for it or navigating to All Programs, Accessories, Notepad. 
* A much better text editor is called 'Sublime Text'. It has nice features like syntax highlighting, which colour-codes your code to make it easier to read, most programmers will use a more advanced text editor like this. You can download it from <http://www.sublimetext.com/2>

Now you can type any python code you want (note it won't be executed!) and then save it when you're done using File, Save. For consistency, it's good if you name your files ending with `.py` and not `.txt` to distinguish them from 'regular' text files. It's also recommended to not use spaces and make it as simple as possible to type in the command prompt.

Once you've saved your code (make a note of where exactly you've saved it!) it's time to run the code. Go back to the command prompt (open a new one if you've closed it) and navigate to the folder where your code is. Use `dir` to verify that you've indeed found your script. You should now be able to run all the code in the script at once using `python myscript.py` or `py -3 myscript.py` (depending on how you launched python earlier and what you named your script). Now you'll either see the output of your code (note that you don't get any more helpful hints like variable contents anymore unless you explicitly use `print()` or something similar), or an error.

If you get an error, don't worry! This is one of the other main advantages of writing scripts, in that you can just go back to the text editor, fix your mistake (this can take a few rounds of trial and error), and run your script again. Try to lose your fear of errors, as they're more a reflection of the computer not understanding you.

### Mac and Linux

Mac and Linux are 'POSIX' systems, which means they have a lot in common and have a fairly consistent terminal interface. Note that when running the following you may occasionally encounter errors. These happen for the reason as in python - the computer is very strict because it's stupid and doesn't always understand what you mean unambiguously, so you'll need to rephrase what you're asking of it/fix any typos!

* In Mac, the terminal can be accessed from the Applications folder under 'Utilities'. Alternatively, you can press cmd+space, type terminal and press enter.
* Opening a terminal in linux will vary a lot. In many cases there may be a terminal icon somewhere on your desktop/app bar/menu bar to click (it'll probably look like a black rectangle). If you're unsure ask one of us!

The terminal is another way to interface with the files and (some/many in the case of linux) programs on your computer in a textual input/output way. The main programs (or 'commands') we're going to want to use here are `cd`, `pwd`, `ls`, and `python`.

#### Getting used to the terminal

* `pwd` stands for 'print working directory' (a directory is just a folder) and tells you where you are
* `cd` stands for 'change directory' and lets you navigate between folders
* `ls` stands for 'list' and lists what what files and folders are in the current folder

Firstly you probably want to know where you are. Try typing `pwd` and pressing enter. You'll probably see something like `/Users/Me` or `/home/me` which indicates you're in your 'home' directory.

Now let's find where we can go; type `ls` and press enter to list the files and folders in the current directory. Hoepfully these look familiar to you! 

You can try navigating to one of the folders using `cd my-folder` where `my-folder` is the name of your directory. If this worked, you should notice that `pwd` now says `/home/me/my-folder` or similar, and that `ls` lists the appropriate files and folders.

There are a couple special directories known as `.` and `..`; these correspond to your current directory and 'parent' directory respectively. The parent directory is one level above the current, so can be used to go 'back' by typing `cd ..`.

Practice finding your way around your files for a bit.

#### Running the python interpreter

As mentioned in the preparation document, running python should be as simple as typing `python` and pressing enter. Some lines will be printed, including the version of python. This should be 3.something, though in some cases (such as if you've got multiple versions installed), it may be a smaller number, e.g. 2.7. If this is the case, try exiting (type `exit()` or press ctrl-D) and running `python3` instead.

Now you should be presented with a `>>> ` 'prompt', where you can type in python code and have it run (after pressing enter). You are now ready to go on with the workshop!

#### Writing scripts

As mentioned earlier, writing scripts allows you to save all your hard work! Script files are plain text files, which means you can't use Microsoft Word, OpenOffice, or similar to create them, nor can you use things such as bold or italics or any other 'rich formatting'. First, let's open up a text editor:

* If you're on mac, you'll already have one installed known as 'TextEdit'. Though this can be used, it's setup in a rich text way and has annoying quote autoreplacement rules that can give very confusing errors unless setup in a particular way. It's probably best not to use this!
* If you're on linux, you'll also have some preinstalled. This varies a lot though so there's not one recommendation here! You could look for 'gedit' or 'kate'... You can also consider 'vim' or 'emacs', though these are for very advanced users!
* If you want a recommendation, a very good text editor is called 'Sublime Text'. It has nice features like syntax highlighting, which colour-codes your code to make it easier to read, most programmers will use an advanced text editor like this. You can download it from <http://www.sublimetext.com/2>

Now you can type any python code you want (note it won't be executed!) and then save it when you're done using File, Save. For consistency, it's good if you name your files ending with `.py` and not `.txt` to distinguish them from 'regular' text files. It's also recommended to not use spaces and make it as simple as possible to type in the command prompt.

Once you've saved your code (make a note of where exactly you've saved it!) it's time to run the code. Go back to the command prompt (open a new one if you've closed it) and navigate to the folder where your code is. Use `ls` to verify that you've indeed found your script. You should now be able to run all the code in the script at once using `python myscript.py` or `python3 myscript.py` (depending on how you launched python earlier and what you named your script). Now you'll either see the output of your code (note that you don't get any more helpful hints like variable contents anymore unless you explicitly use `print()` or something similar), or an error.

If you get an error, don't worry! This is one of the other main advantages of writing scripts, in that you can just go back to the text editor, fix your mistake (this can take a few rounds of trial and error), and run your script again. Try to lose your fear of errors, as they're more a reflection of the computer not understanding you.

## IDLE

Getting used to the terminal and text editors is good practice if you want to use more programming languages, but at this stage there's really no compelling reason to battle through it if you're finding it tough to learn. Instead, we can use a user-friendly 'IDE' that comes preinstalled with python, known as IDLE.

After installing python, you should be able to find the IDLE application in your normal program directory (e.g. start menu, Applications folder, etc). Launch it.

### Using the python interpreter

When you first launch IDLE you'll be gievn a window with a menu bar and a big white rectangle. The rectangle is /analagous/ to using a terminal but with all the commands taken care of automatically. At the moment, it should contain the python interpreter. You can check this because it should report the python version (again, make sure this says something like 3.5, if it's smaller than 3 (like 2.7) then close IDLE and look for an IDLE3 or similar), and also have `>>> ` on a line on its own at the bottom.

The `>>> ` is known as a prompt, and you can type your code here as instructed in the workshops!

### Writing scripts

To write a script is as simple as clicking File, New! A new window will open where you can type your code. You'll notice that it's not automatically run as you type lines, but that it does have nice colour-coding to make your code easier to read. Put whatever code you want to run in this file, and save it using File, Save. You can then run the code all at once by clicking Run, Run Module in the menu bar. As simple as that!

Now you'll either see the output of your code in the interpreter window (note that you don't get any more helpful hints like variable contents anymore unless you explicitly use `print()` or something similar), or an error.

If you get an error, don't worry! This is one of the other main advantages of writing scripts, in that you can just go back to the text editor, fix your mistake (this can take a few rounds of trial and error), and run your script again. Try to lose your fear of errors, as they're more a reflection of the computer not understanding you.
