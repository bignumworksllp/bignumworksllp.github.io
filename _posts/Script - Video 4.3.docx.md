**Slide - Video Introduction**

Welcome to the video - Distributing your program using pyinstaller

In this video, we will learn …

**Slide - Demo**

**Browser - https://github.com/pyinstaller/pyinstaller**

Let’s suppose you have a python program that uses certain libraries.

Now, what if you want to release your program without training or
requiring your users to install each module?

This is where pyinstaller comes in handy.

PyInstaller bundles a Python application and all its dependencies into a
single package. The user can run the packaged app without installing a
Python interpreter or any modules.

yInstaller reads a Python script written by you. It analyzes your code
to discover every other module and library your script needs in order to
execute. Then it collects copies of all those files -- including the
active Python interpreter! -- and puts them with your script in a single
folder, or optionally in a single executable file.

**Command line**

You can install it through pip:

pip install pyinstaller

Basic usage is very simple, just run it against your main script:

pyinstaller /path/to/yourscript.py

**Atom Code Editor**

For example, let’s look at this python program.

Here we are importing some modules, somewhat of which will not be
available by default on user’s machine.

We can use pyinstaller to make this into a standalone distribution.

This creates,

-   a script.spec file, analogous to a make file

-   a build folder, that holds some log files

-   a dist folder, that holds the main executable script, and some
    > dependent Python libraries,

all in the same folder as script.py. PyInstaller puts all the Python
libraries used in script.pyinto the dist folder, so when distributing
the executable, distribute the whole dist folder.

The script.spec file can be edited to [*customise the
build*](http://pythonhosted.org/PyInstaller/#spec-file-operation), with
options such as

-   bundling data files with the executable

-   including run-time libraries (.dll or .so files) that PyInstaller
    > can’t infer automatically

-   adding Python run-time options to the executable,

Now script.spec can be run with pyinstaller (instead of
using script.py again):

\$ pyinstaller script.spec

To create a standalone windowed OS X application, use
the --windowed option

\$ pyinstaller --windowed script.spec

This creates a script.app in the dist folder. Make sure to use GUI
packages in your Python code, like *PyQt* or *PySide*, to control the
graphical parts of the app.

There are several options in script.spec related to Mac OS X app
bundles [*here*](http://pythonhosted.org/PyInstaller/spec-files.html#spec-file-options-for-a-mac-os-x-bundle).
For example, to specify an icon for the app, use
the icon=\\path\\to\\icon.icns option.

In this video, we learned ….

This also concludes the current section. In this section we learned how
to Parse user arguments and config files using modules argparse and
ConfigParser. We learned how to Package our python code using setup.py
(setuptools). And we learned how to Distribute our programs using
pyinstaller

**------------------------------End--------------------------------**
