---
layout: post
title:  "Reading CSV Data into Julia"
categories: Julia, DataScience
tags: [Julia, Data Analysis, Data Science]
published: true
---

# Introduction

In this article, we will see how to read in csv data in julia.

# Install `CSV` package

We will be using a package called `CSV` to read in csv data into `julia`. We need to first install `CSV` first. To install or use a new julia package, you first need to tell julia explicitly to use the package manager `Pkg` like this.


```julia
using Pkg
```

Next, we install `CSV` package.

```julia
Pkg.add("CSV")
```

# Importing or reading in CSV Data into julia

```julia
using CSV

df = CSV.read("data.csv")
```
This is how it looks like in julia console.
![Data Output](/assets/images/julia-import-csv-data-output.png)
