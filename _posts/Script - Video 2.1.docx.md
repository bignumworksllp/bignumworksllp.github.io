**Slide - Section Introduction**

Welcome to Section - Simple GUI Recipes with tkinter

In this section we will get introduced to the python GUI library tkinter
and learn how to use it to build GUI apps and interact with the user via
dialogs, create and layout a graphical user interface.

**Slide - Video Introduction**

Welcome to the video - Welcome to Tkinter

In this video, we are going to introduce tkinter, how to setup up in
your development environment and we will write our first gui program
with python and tkinter.

**Slide - Demo**

**Browser - https://wiki.python.org/moin/TkInter**

Tk was developed as a GUI extension for the Tcl scripting language by
John Ousterhout. The first release was in 1991. Tk proved as extremely
successful in the 1990's, because it is easier to learn and to use than
other toolkits. So it is no wonder that many programmers wanted to use
Tk independently of Tcl. That's why bindings for lots of other
programming languages have been developed, including for Python called
Tkinter.

**Command line**

Tkinter is bundled with latest releases of Python. You can check it by
running import tkinter from the python intrepretor.

**https://www.activestate.com/activetcl/tcl-tk-modules**

If you don’t have it, you can download the installer from activate state
website from this url. You need to download and install the acticetcl
package that contains tkinter.

**Command line**

Here, we will demo how to create a label.

The tkinter module, containing the Tk toolkit, has always to be
imported. In our example, we imported tkinter by renaming it into tk,
which is the preferred way to do it:

import tkinter as tk

To initialize tkinter, we have to create a Tk root widget, which is a
window with a title bar and other decoration provided by the window
manager. The root widget has to be created before any other widgets and
there can only be one root widget.

root = tk.Tk()

The next line of code contains the Label widget. The first parameter of
the Label call is the name of the parent window, in our case "root". So
our Label widget is a child of the root widget. The keyword parameter
"text" specifies the text to be shown:

w = tk.Label(root, text="Welcome to Tkinter")

The pack method tells Tk to fit the size of the window to the given
text.

w.pack()

The window won't appear until we enter the Tkinter event loop:

root.mainloop()

Our script will remain in the event loop until we close the window.

**slide - Next Video**

This concludes this video. In this video, we introduced tkinter, how to
setup up in your development environment and we will write our first gui
program with python and tkinter.

In the next video, we will show how to use tkinter to display simple
popups

**------------------------- end ---------------------**
