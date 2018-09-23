**Video 1.3**

**Slide - Video Introduction**

Welcome to the video - Acquiring data from web (urllib/xmllib/json
recipes)

In this video, we are going to learn how to acquire data from web within
python code. We will see how to use urllib to get webpage data. We will
see how to use xmlilib to parse xml data. And we will see how to use
urllib and json modules together to get json data from web apis

**Slide – Demo**

**Jupyter Notebook**

Let’s talk about urllib module first. Urllib is a python library that
allows us to access websites and their content from inside our python
programs. Through urllib, you can access websites, download data, parse
data, modify your headers, and do any GET and POST requests you might
need to do.

Here is the first and easiest example of using urllib. We just need to
import urllib.requests. From there, we assign the opening of the url to
a variable, where we can finally use a .read() command to read the data.
The result is a massive mess, but we did indeed read the source code.

We can use regular exressions to clean up this data.

Next, sometimes, we want to put in values, or GET/POST, from/to a
URL. There are multiple ways to pass values through like this, you can
just hard-code them, or you can use urllib to do it. Let's show an
example of requests with urllib:

Here, we're defining the variables that we plan to POST to the url we
specify.

Then we encode to utf-8 bytes. We make our request, adding in one more
value, data, which is the encoded dictionary of keys and values, or
better understood in this scenario as variables and their values. Then
we open the url with the request that we've built, which we call a
response, since that's what we get with it. Finally, we read that
response with a .read().

If the website you are scraping for data, you need to be careful as lot
of websites specifically forbid scraping of data.

Next up is xmllib library.

Xmllib is used to parse xml data.

We start with importing the modules. We are going to be using the DOM
APIs to parse the data.

The data we have is in an xml file containing data about movies.

> Here is the easiest way to quickly load an XML document and to create
> a minidom object using the xml.dom module. The minidom object provides
> a simple parser method that quickly creates a DOM tree from the XML
> file.
>
> The sample phrase calls the parse( file \[,parser\] ) function of the
> minidom object to parse the XML file designated by file into a DOM
> tree object.

We get the results in a nodelist object.

We then loop through this object and get the values by the tag name like
this.

Next, let’s talk about how to get json data from the web.

Lot of the times, various companies provide their through API calls and
serve the data as JSON or avaScript Object Notation

We can use urllib modules together with json module to get the json
data.

We first import urllib requests module and json modules

Here for example we are opening the google geo data and getting the json
data.

This json data can be further parsed depending how do you want to use it
in your program.

**Slide - Next Video**

This concludes this video. In this video, we learned how to acquire data
from web within python code. We saw how to use urllib to get webpage
data. We saw how to use xmlilib to parse xml data. And we saw how to use
urllib and json modules together to get json data from web apis

In the next video, we will learn about Grouping and splitting your data
in python

**------------------------- end ---------------------**
