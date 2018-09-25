# Introduction

In this article, we are going to learn how to use argparse module to parse
user arguments. We will learn how to use module config parse to read and
access configuration files. And we will run a demo of these two modules.

## Argparse

Argparse is the recommended command-line parsing module in the Python
standard library.

## ConfigParser

The configparser module in Python is used for working with configuration files. It is much similar to Windows INI files. You can use it to manage user-editable configuration files for an application. The configuration
files are organized into sections, and each section can contain name-value pairs for configuration data. Config file sections are identified by looking for lines starting with \[ and ending with \]. The value between the square brackets is the section name, and can contain
any characters except square brackets. Options are listed one per line
within a section. The line starts with the name of the option, which is
separated from the value by a colon (:) or equal sign (=). Whitespace
around the separator is ignored when the file is parsed.

## sample config file

A sample configuration file with section “bug\_tracker” and three
options would look like:

```
[bug_tracker]
url = http://localhost:8080/bugs/
username = packt
password = SECRET
```
The most common use for a configuration file is to have a user or system administrator edit the file with a regular text editor to set application behavior defaults, and then have the application read the file, parse it, and act based on its contents. Use the **read()** method
of **SafeConfigParser** to read the configuration file.

This code reads the bug.ini file from the previous section and prints
the value of the **url** option from the **bug\_tracker** section.

**slide - Next Video**

This concludes this video. In this video, we learned how to use argparse
module to parse user arguments. We will learn how to use module config
parse to read and access configuration files. And we will run a demo of
these two modules.

In the next video, we will learn to Package our code using setup tools.

**------------------------- end ---------------------**
