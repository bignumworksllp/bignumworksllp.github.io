---
layout: post
title: Getting started with Bitcoin Using Python
author: Harish Garg
date:   2018-09-07 08:00:00 +0530
categories: Python, Bitcoin
tags: [Python, Bitcoin]
published: true
---

Introduction
------------

In this tutorial, we are going to introduce Bitcoin using Python. We
will be using Python’s [*bitcoin*](https://pypi.python.org/pypi/bitcoin)
library, conveniently called bitcoin.

![Cover Image](/assets/images/bitcoin-python-blog-title.png)


Prerequisites
-------------

To get started with Bitcoin using Python, we need,

-   A Computer which can run Python programming environment

-   A basic knowledge of Python or another scripting language

-   Ability to run commands and programs from a command line program

Setup your Computer
-------------------

### Install Python

Download and install python from
[*http://www.python.org/*](http://www.python.org/) Make sure to download
the Python 3.x as that’s the one we are going to be using in this
tutorial.

### Install bitcoin python library

After you finish installing Python, open your command line program and
execute below command to install bitcoin python library

> pip install bitcoin

Hello Bitcoin - Generate a Private key
--------------------------------------

We will start with a writing a “Hello World” equivalent of Bitcoin in
Python. To write your python, you can need a code or text editor which
supports writing in ASCII format. You cannot use MS Word of Wordpad for
this. You could use Notepad, but we recommend using [*Atom Code
Editor*](https://atom.io/), a free code editor.

Open your favorite editor and type in below code. In this code, we are
first importing the bitcoin library. We are then generating a private
key using ***random\_key*** function and we are then displaying the
private key on the screen.

> from bitcoin import \*
>
> my\_private\_key = random\_key()
>
> print(my\_private\_key)

Save it as a .py file and then open your command line program and run
the above program like this.

> python &lt;program location and name&gt;

This will print out a private key.

Generate a Public Key
---------------------

Next we generate a public key. We do this by passing the private key we
generated to ***privtopub*** function

> from bitcoin import \*
>
> my\_private\_key = random\_key()
>
> my\_public\_key = privtopub(my\_private\_key)
>
> print(my\_public\_key

Create a bitcoin address
------------------------

In the previous programs we generated private and public keys. Now, we
are going to real bitcoin part. In the below code, we are generating a
bitcoin address by passing the public key we generated to
***pubtoaddr*** function.

> from bitcoin import \*
>
> my\_private\_key = random\_key()
>
> my\_public\_key = privtopub(my\_private\_key)
>
> my\_bitcoin\_address = pubtoaddr(my\_public\_key)
>
> print(addr)

Create a Multi-signature Address
--------------------------------

Next, we create a multi-signature bitcoin address. Multi-signature
address is an address that is associated with more than one private key.
So, we first create 3 public and private keys. We then create a
multi-sig by passing the 3 public keys to ***mk\_multisig\_script***
function. Finally, the resulting multi-sig is passed to ***scriptaddr***
function to create the multi signature bitcoin address.

> from bitcoin import \*
>
> my\_private\_key1 = random\_key()
>
> print('Private Key 1: ' + my\_private\_key1)
>
> my\_public\_key1 = privtopub(my\_private\_key1)
>
> print('Public Key 1: ' + my\_public\_key1)
>
> my\_private\_key2 = random\_key()
>
> print('Private Key 2: ' + my\_private\_key2)
>
> my\_public\_key2 = privtopub(my\_private\_key2)
>
> print('Public Key 2: ' + my\_public\_key2)
>
> my\_private\_key3 = random\_key()
>
> print('Private Key 3: ' + my\_private\_key3)
>
> my\_public\_key3 = privtopub(my\_private\_key3)
>
> print('Public Key 3: ' + my\_public\_key3)
>
> my\_multi\_sig = mk\_multisig\_script(my\_private\_key1,
> my\_private\_key2, my\_private\_key3, 2,3)
>
> my\_multi\_address = scriptaddr(my\_multi\_sig)
>
> print('Multi-Address: ' + my\_multi\_address)

View address transaction history
--------------------------------

We can also look at pre-existing bitcoin addresses’ transactional
history. We do this passing a valid bitcoin address to function
***history***.

> from bitcoin import \*
>
> print(history(a\_vaid\_bitcoin\_address))

If you don’t have an address, you can look one up from
[*Blockchain*](https://blockchain.info).

Conclusion
----------

In this tutorial, we introduced bitcoin with python. We saw how to get
setup with python for bitcoin. We saw how to generate private key,
public key and a bitcoin address. We also saw how to create a multi
signature bitcoin address and how to look at transactional history of a
bitcoin address.

If you would like to dig deeper into Bitcoin and Blockchain Concepts using Python, check it out my [Video Course on Packt](https://www.packtpub.com/application-development/getting-started-python-bitcoin-programming-video)
