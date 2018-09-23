**Video 1.5**

**Slide - Video Introduction**

Welcome to the video - Data serialization with json and pickles

In this video, we will learn about data serialization with python. We
will learn about modules pickles and json and we will see examples of
data serialization with these modules.

**Slide – Demo**

**Jupyter Notebook**

Data serialization is the concept of converting structured data into a
format that allows it to be shared or stored in such a way that its
original structure to be recovered. In some cases, the secondary
intention of data serialization is to minimize the size of the
serialized data which then minimizes disk space or bandwidth
requirements.

We start with importing the pickle module.

Here is a dictionary object with some data that we want to serialize.

We then pass this dict object to dumps method of pickle to convert the
object to a serialized string

By calling the type on this new object we can see that it is of bytes or
the serial object type.

We can also reverse this process by passing the serialized object to the
loads method from pickle to de-serialize an object

We can confirm that by checking the type of the de-serialized object we
created

Python’s in-built json module can be used to encode and decode json
data.

We start with importing the module.

To encode a data structure into json, we can use the dumps method from
json module, like this.

And this is how the output looks like.

**Slide - Next Video**

This concludes this video. In this video, we learned about data
serialization with python. We learned about modules pickles and json and
we will see examples of data serialization with these modules.

In the next video, we will learn about Data compression using
(zipfile/tarfile/zlib)

**------------------------- end ---------------------**
