**Video 1.4**

**Slide - Video Introduction**

Welcome to the video - Grouping and splitting your data

In this video, we will learn about using groupby method to split and
aggregate data in groups

We will explore how groupby method works by breaking it into its pieces

We will demonstrate groupby with statistical and other methods

We will learn how to do interesting things through groupby by iterating
over the grouped data.

**Slide – Demo**

***Jupyter Notebook***

We start with importing pandas module in our jupyter notebook

We then read in our csv dataset.

Let’s start with asking a question and see if pandas groupby method can
help us get the answer.

We want to get the mean price for every State.

We have used groupby method for aggregating data on states and getting
the mean price per state

In the background, groupby method splits the data into groups

And then we applied a function on this split data

And result was put together and displayed

let's break this code into it's individual pieces to see how it happens.

First, splitting into groups

We selected a subset of data that has only State and Price columns.

We then called groupby method on this data and passed it the column
State as that's the column we want the data to be grouped on

We stored the data in a object

Let's print out this data using list method

Now we have data groups based on State

Next we apply a function on the split data and display the combined
result

We use the method mean to get the mean of the prices.

After the data is split into groups, we can use pandas methods to get
some interesting information on these groups.

For example , here we are getting descriptive statistical information on
each state separately

We can also groupby on multiple columns

For example, here we group on State and Region Name columns

Here we are getting the number of records per state through groupby and
size methods.

All the code we demonstrated in this video so far we grouped on rows.

However, we can also group on columns

Here we are doing this by passing the axis parameter set to 1

We can also iterate over the split groups and do interesting things with
it.

here we are iterating over the grouped data by state and publishing the
result with state as heading followed by table of all the records from
that state.

**Slide - Next Video**

This concludes this video. In this video, we learned about using groupby
method to split and aggregate data in groups

We explored how groupby method works by breaking it into its pieces

We demonstrated groupby with statistical and other methods

We learned how to do interesting things through groupby by iterating
over the grouped data.

In the next video, we will learn about Data serialization with json and
pickles

**------------------------- end ---------------------**
