---
layout: post
title: Working with text files in Python
author: Harish Garg
date:   2018-09-08 13:32:30 +0530
categories: Python
tags: [Python]
published: true
---
# Introduction

In this post, we are going to learn how to work with text files using python. We will learn how to read and write text file using python. We will also see how to best work with a csv
file from within python code.

## Reading and writing text files

Let’s start with reading and writing text files.

When working with normal text files, you don’t need to import any python
library. It’s handed natively in python.

Before you can read or write to a file, you have to open it. To open a
file you use python’s open function.

The most simplest way to use the open function with a single argument
i.e. the file name we want to open.

```python
f = open(“test.txt”)
```

We receive a file handle that we are assigning to a variable f here.

We can use this file handle to do the file operations on this file.

For example, to read the contents of this file, you can use the function
read like this.

```python
print(f.read())
```

However, the most common way to open a file handle is with two
arguments – filename and the mode. Mode here refers to whether the want
to open the file for reading or writing.

For example, if we just want to file to be opened in read mode, we can
pass the argument r after the fil name like this.

```python
file = open(“test.txt”, “r”)
```

Now let’s see how to write a file.

To write a file, you need to pass the mode argument as w

```python
file = open(“myfile.txt”, “w”)
```

We can now use this file handle to write to the file like this.

```python
file.write(“I am writing this with python.”)
```

If you want to write another line, you can just call write function
again.

```python
file.write(“This is the second line.”)
```

Once, we are done with the file, we can close the file with close
method.

```python
file.close()
```

We saw the modes read and write that work separately.

There are few other modes, like a that stands for appending mode. And r+
mode that is for both read and write while working with a file.

## More read file functions

We saw that we can read the contents using read method. It prints the
complete contents of the file in one line of code.

However, there are lot of other ways to read the contents of the file.

`Rreadline` method gives the content line by line.

```python
## Open the file.
file = open("contents.txt", "r")

# printing lines.
print(file.readline())
```

We can also get all the lines in a list by using method `readlines`.

```python
# getting all lnes as a list
print(file.readlines())
```

Using this technique, we can then can split the whole text content into
separating words, like this,

```python
# splitting the words
data = file.readlines()
for line in data:
    words = line.split()
    print(words)
```

Next, we look at how to best work with csv file from within python.

### Reading csv files in Python

Best module to work with csv files Is called pandas.

To start using it, we first import it.

```python
import pandas as pd
```

We have a csv file which we have saved in the same location.

We can import this csv file in python using pandas read csv method

```python
data = pd.read_csv("data.csv")
```

Read csv method gives us a tabular data object that is called a
dataframe. We are saving this dataframe in a variable data.

We can see the full data like this here.

```python
print(data)
```

Pandas has very useful methods that can be used to do lot of operations
on this data now.

For example , we can use head method to get first few lines of this
data. Default is 5.

```python
print(data.head())
```

`tail` gives us rows from bottom

```python
print(data.tail())
```

`info` will give us nice useful information about this data like type of
data in each columns, missing data, etc.

```python
print(data.info())
```

Columns method will gives us the names of columns in a list.

```python
print(data.columns)
```

To get a single column’s data, we can just call it like this.

```python
print(data['Age'])
```

We can do some statistical operations on this data also.

For example to get the mean age for all records, we can do this.

```python
print(data['Age'].mean())
```

## Conclusion

In this article, we saw how to work with text files in Python. We saw how to read contents. We saw how to write to a text file. And we also saw how to read in data from csv files into Python.