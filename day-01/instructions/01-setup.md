# 🐍 Setting up a Python stack 🐍

There are a lot of ways to get a working Python installation and even more ways to write and run code in Python.

Browser-based, remote environments like [Google Colab](https://colab.research.google.com/) or [Dartmouth's JupyterHub](https://jhub.dartmouth.edu/) are excellent options for teaching and learning, but actual research or project work needs a more persistent and centralized environment that includes not just your code, but also the data you work with, documentation, results, and even the manuscript of a write-up of the project.

For such projects, it is generally beneficial to work on your local computer, as opposed to the cloud. Even so, there are still many options to choose from.

Our recommended set of tools for Python project work (also known as the _Python tech stack_) are the official Python distribution and the versatile, yet simple code editor Visual Studio Code.

There are good reasons to use other distributions and tools, but this minimal and therefore comprehensible setup is great for novice Python programmers and experienced developers alike.

## Installing Python

### Instructions for MacOS Ventura or later
- Using a browser of your choice, navigate to [www.python.org](www.python.org)
- In the `Downloads` menu, click on the gray button to dowload latest stable version of Python
- Install the downloaded `pkg` file with the default settings
- In the `Finder` window that pops up after installation, double-click the file `Install Certificates.command`
- Close the `Finder` window and the installer
- Move the `pkg` file to the Trash
- Open the `Terminal` application (found under `Other` on the Launchpad)
- Enter the command `python3` into the terminal and hit `return`
- The terminal will show the version of Python we just installed and a command prompt starting with `>>>` (the so-called Read-Eval-Print Loop, or REPL)

### Instructions for Windows 11
- Using a browser of your choice, navigate to [www.python.org](www.python.org)
- In the `Downloads` menu, click on the gray button to dowload latest stable version of Python
- Start the downloaded installer:
  - Check the box next to `Add python.exe to PATH`
  - Click `Install Now` and wait for installation to finish
  - Click `Disable path length limit`
  - Close the installer
- From the start menu, open the Python executable (e.g., `Python 3.12 (64-bit)`)
- The terminal will show the version of Python we just installed and a command prompt starting with `>>>` (the so-called Read-Eval-Print Loop, or REPL)



## Exploring the REPL (optional)
We can enter Python code in the REPL. The REPL will then _read_ the code, _evaluate_ it (i.e., execute it) using Python, and then _print_ the final result of the execution. Then the command prompt `>>>` returns and the process can start again in a _loop_.

Let's try some simple mathematical computations: Enter `4 + 3` into the REPL and hit `return`.

Q: What happens?
A: The result is calculated and printed, then the prompt returns.


Now let's write an equation and assign the result to a variable `x` by entering `x = 6 * 7 + 12` (submit with `return`).
Q: What do you see now?
A: Nothing is printed, because the assignment to a variable does not return anything.

We can see the value of the variable `x` by using the `print()` function: `print(x)`.

You can exit the REPL by holding down `Ctrl+D` or entering `quit()` (and hitting `return`).

The REPL is great if we want to do a quick calculation or test a line of code or two. However, most of the time we want to run an entire program consisting of potentially many lines of code. We also want to be able to save code and re-run it at a later time, so we don't always have to start from scratch.

Since code is just text, we can write a text file that contains our code and then have Python execute that file line by line. In theory, we could use any kind of text editor to write such code files, but a dedicated _code editor_ has a lot of convenient, specialized functionality that a raw text editor does not have. The code editor that we at [Research Data Services](https://www.library.dartmouth.edu/research-data-services) currently recommend is called _Visual Studio Code_.

## Installing Visual Studio Code
_Visual Studio Code_, or _VS Code_, is a code editor developed by Microsoft and available on all major platforms (Linux, macOS, Windows). It is entirely free and largely open-source. Essentially a text editor with superpowers, it supports not just Python but many programming languages and is incredibly versatile thanks to a plethora of optional extensions. Since it can open, display, or run all kinds of different files, you rarely have to leave the program when working on a project, which makes it a great _Integrated Development Environment_ (IDE).


### Instructions for MacOS Ventura or later
- Navigate to [code.visualstudio.com](https://code.visualstudio.com)
- Download the latest stable version
- Open your `Downloads` folder
- Drag and drop the dowloaded file `Visual Studio Code` onto your `Applications` folder on the left pane


### Instructions for Windows 11
- Navigate to [code.visualstudio.com](https://code.visualstudio.com)
- Download the latest stable version
- Open the downloaded installer
  - Follow the instructions and click `Next` three times
  - When prompted, select (or leave selected) all checkboxes under `Other:`
  - Click `Install`

## Intro to Visual Studio Code
When you open VS Code for the first time, you will be greeted by a Welcome screen. For now, choose a theme that you like and close it.

VS Code works best if you open a folder that contains everything related to the project you want to work on:
- Select the `Explorer` tab at the top of the Primary Side Bar to the left
- Click `Open Folder` and choose the folder with the workshop materials (most likely `software-carpentry-python-main`)
- Choose to trust the authors of the folder when prompted


> ℹ️ **Note:** On Windows 11, you can also right-click a folder in the Explorer and choose `Show more options` followed by `Open with Code`. On macOS, this is unfortunately not available by default, but you can create such a shortcut by following the instructions in this [Stack Overflow answer](https://stackoverflow.com/a/64065309),

- Explore the workshop folder structure by clicking through the directories on the left and selecting various files. Note the following:
  - Selecting a file with a single click opens it in a new tab, but close it again if you switch to another file (note the name in italics on the tab)
  - Selecting a file with a double click opens it in a new tab and keeps it open until you close the tab (note the non-italicized name on the tab)
  - Some file extensions that VS Code recognizes will cause a notification to popup recommending an extension. **While those can be useful, let's stay focused on the main concepts here and ignore these notifications**
  - Right-clicking a file or folder will bring up additional options:
    - Many file-management operations can be done this way (cut, copy, paste, ...)
    - `Reveal in Finder` (macOS) or `Reveal in File Explorer` (Windows 11) can be useful for things that cannot be done inside of VS Code
    - Some files can be previewed as a rendered version by clicking `Open Preview` (e.g. `*.md` files)
  - Some files cannot be displayed or previewed within VS Code out-of-the box, but support can be added through extensions (e.g. `*.pdf` or `*.csv` files)
  - Open tabs can be arranged by dragging and snapping them into position:
    - Example: preview of this file side-by-side with the raw text.


## Installing the Python extension
As mentioned above, you can add a lot of functionality to VS Code through extensions. While you definitely should explore the huge collection of exntensions out there, today we will focus on the bare minimum that allows us to write Python code.

Theoretically, you would not need any extension to write a text file in VS Code and then have Python execute the commands in that text file. However, the Python extension offfers a lot of additional functionality that greatly simplifies the development and debugging process.

To install the extension:
- Choose the `Extensions` tab on the Primary Side Bar
- The Python extension should be listed under the `Popular` heading, otherwise type `Python` into the search box
- Click on `Install`
- Close the `Welcome` tab that popped up after the installation

To check that it works, we will write some Python code to a file and execute it:
- On the left, navigate to the folder `day-01/my_code` and highlight it
- Right-click the folder and select `New File...` or click on `New File...` at the top of the side bar
- Enter `hello_world.py` and hit return
- In the tab that opened up, enter the following lines of code:
  ```{python}
  4 + 3
  x = 6 * 7 + 12
  print("Hello world!")
  ```
- Now let's run the code by clicking the ▶️ icon in the top right
  - Q: What do you observe?
    A: Only the line with the `print` statement is printed to the console
-

