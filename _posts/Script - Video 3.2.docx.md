**Slide - Video Introduction**

Welcome to the video - Working with threads to stream stock prices
(threading/urllib)

In this video, we will learn about how to create threads and write a
multi-thread application in Python. We shall see how to create threads
using the thread class in Python style and also in Java style

-   Pythonic Style

-   Java Style

**Slide – Creating threads:**

We use the threading module's Thread class to create threads in a
python's multi-threaded application.

The \_\_init\_\_ method for the Thread class is shown here. This is
taken from the threading.py module source.

As you can see the Thread constructor takes following parameters

-   Group – is not used currently and is reserved for future use.

-   Target – should be defined and should be set to a callable object
    like a method that is to be run as a separate thread.

-   Name – name of the thread. By defualt the thread is given a Thread -
    &lt;integer&gt; if the thread name is not provided.

-   Args – this is the tuple corresponding to the arguments passed onto
    the target method. We should always make sure the arguments to
    target and this tuple have correct mapping.

-   Kwargs – this is a dictinory of *keyword arguments for the target*\
    *invocation*

*The way to create a thread is to instansite the Thread class with
suitable arguments we just defined and then call start() method on the
object.*

*Another way, the Java way, is to create a sub-class of the Thread class
and override the run() method that defines what the thread has to do
like the target method we just described. *

*In such cases, if the sub-class overrides the \_\_init\_\_ method, we
have to make sure that the \_\_init\_\_ method of the Thread class is
called before anything is done in the constructor of the sub-class.*

*Let us look at both these ways of creating threads in a couple of
demos. *

*I just want to point out the slopiness in the documenation of
threading.py. There is an argument daemon that you can specify when
creating the thread but is not documented here. This arguement dictates
if the thread should be a daemon thread. We shall discuss about this and
what a dameon thread is a little later in the next video.*

**Slide – Demo**

For this demo, we are going to consider a simple application. The aim of
this application is to fetch the content of a list of urls and write the
contents of the same into a local file.

We use the urllib3 module for reading the url content.

Import urllib3

We shall also disable all the warnings about untrusted certificates.

**Let us write a simple method to read the url and write its contents
into a file**

def download\_url(file\_name, url):

> print("Downloading the contents of {} into {}".format(url,
> file\_name))\
> http = urllib3.PoolManager()\
> \
> response = http.request(method="GET", url=url)\
> with open(file\_name, "wb") as f:
>
> f.write(response.data)\
> \
> print("Download of {} done".format(url))

Let us try to download a list of urls. We shall define a dictionary for
this url list as a mapping between file names and URLs.

test\_dict = {\
"Google": "http://www.google.com",\
"Python": "http://www.python.org",\
"Bing": "http://www.bing.com",\
"Yahoo": "http://www.yahoo.com"\
}

Let us invoke the download\_url for each of the URLs.

for key in test\_dict:

Download\_url(key, test\_dict\[key\])

Lets run the program.

As you can see, the webpages are downloaded one after the other into
respective files.

Now, let us make this program multi-threaded by using the
threading.Thread class

Import threading

We will also define a list of threads that we create.

Threads = \[\]

As we go through each of the item in the test\_dict, we shall create a
different thread to fetch each URL independently. Also, let us start
these threads.

thread = threading.Thread(target=download\_url, name=key, args=(key,
test\_dict\[key\]))\
threads.append(thread)\
thread.start()

We shall wait for each of the threads to complete before main thread
continues to execute.

for thread in threads:\
thread.join()

I will also add a few print statements to this program to track the
execution.

print("Main thread starting execution...")

print("Main thread continuing execution...")

print("Main thread exiting...")

Lets change the download\_url to also print out the thread name.

print("Downloading the contents of {} into {} in thread {}".format(url,
file\_name, threading.current\_thread().name))

**Observe how quickly the download completed when compared to running
the same in a single thread. I**

**That is it. We have created a multi-thread application in Python. What
we just saw is more pythonic way of creating threads.**

**Now, let us see how to create threads in Java style and do the same
URL fetch in a multi-threaded way.**

**First thing we have to do is same as before import the modules and
disable urllib3 warnings**

**We will create a new class that inherits the Thread class. **

class URLDownload(Thread):\
def \_\_init\_\_(self, file\_name, url):\
Thread.\_\_init\_\_(self)\
self.file\_name = "Thread\_" + file\_name\
self.url = url

As we showed in the previous slide, we have to call the Thread's init
method first before anything and that is what we have done here too.

We will move the download\_url() we created before into a special method
called run().

print("Downloading the contents of {} into {}".format(self.url,
**self.file\_name**))\
http = urllib3.PoolManager()\
\
response = http.request(method="GET", url=self.url)\
with open(self.file\_name, "wb") as f:\
f.write(response.data)\
\
print("Download of {} done".format(self.url))

When we create a thread and start a thread, it is the code in this run
method that is run in each thread

Lets do the same thing we did before of starting multiple theads. We
will copy the code from before and modify it.

threads = \[\]\
test\_dict = {\
"Google": "http://www.google.com",\
"Python": "http://www.python.org",\
"Bing": "http://www.bing.com",\
"Yahoo": "http://www.yahoo.com"\
}\
\
print("Main thread starting execution...")\
for key in test\_dict:\
thread = URLDownload(key, test\_dict\[key\])\
threads.append(thread)\
thread.start()\
\
print("Main thread continuing execution...")\
for thread in threads:\
thread.join()\
\
print("Main thread exiting...")

So, instead of calling the threading. Thread constructor, we create an
object of URLDownload class and then call the start method on that. This
will start the thread and run its run method.

Let us run the program now.

See, it does the same thing the previous program did!

**Slide – Next Video**

This concludes this video. In this video, we learned about how to create
threads in python and write a multi-thread application in

-   Pythonic Style

-   Java Style

In the next video we will see how to get started with When threads break
(problem solving)

**------------------------------End--------------------------------**
