**Video 1.6**

**Slide - Video Introduction**

Welcome to the video - Data compression with zipfile, tarfile and zlib

In this video, we are going to learn some data compression techniques
using python. We will learn this using some of the python data
compression modules like zipfile, tarfile and zlib.

**Slide – Demo**

Let’s start with an example of zlib

The zlib library provides us with the compress function, which can be
used to compress a string of data. The syntax of this function is very
simple, taking only two arguments:

Here the argument data contains the bytes to be compressed, and level is
an integer value that can take the values -1 or 0 to 9. This parameter
determines the level of compression, where level 1 is the fastest and
yields the lowest level of compression. Level 9 is the slowest, yet it
yields the highest level of compression. The value -1 represents the
default, which is level 6. The default value has a balance between speed
and compression. Level 0 yields no compression.

And the result is this compressed data.

We can also use the compress() function to compress the data in a file.
The syntax is the same as in the first example. In the example below we
are compressing a text file containing all the text from us
constitution.

he zlib.compress(...) line uses the constant Z\_BEST\_COMPRESSION,
which, as the name suggests, gives us the best compression level this
algorithm has to offer. The next line then calculates the level of
compression based on the ratio of length of compressed data over length
of original data. As we can see, the file was compressed by 67%.

The only difference between this example and our first one is the source
of the data. However, I think it is important to show so you can get an
idea of what kind of data can be compressed, whether it be just an ASCII
string or binary image data. Simply read in your data from the file like
you normally would and call the compress method.

Now let’s look at compression with tarfile module

To create a tar flle tarfile module, we first import the tarfile module.

We then open a new tarfile

Next up is we take a list of files and we add them to the tarfile one by
one and then close the tar file.

Thus our tar file is ready.

Next up is zipfile module.

Again, we start importing the module.

We then create a zip file constructor and pass it the name of the
archive we want to create.

We then call write method on this constructor to add the files we want
added to the archive.

Once, we are done adding the files, we can close the constructor,

And our archive is ready.

**Slide - Next section**

This concludes this video. In this video, we learned some data
compression techniques using python. We learned this using some of the
python data compression modules like zipfile, tarfile and zlib.

This also concludes this section. In this section, we learned how to
work with text based files using python. We learned how to manage data
in databases. We also learned how to acquire data from the web. We
learned how to group and split our data and how to work with data
serialization with json and pickles. And we learned some tricks for
working with data compression in python.

In the next section, we will learn some Simple GUI Recipes with tkinter

**------------------------- end ---------------------**
