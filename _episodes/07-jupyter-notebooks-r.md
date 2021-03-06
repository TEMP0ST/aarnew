---
title: "Working in Jupyter Notebooks with R"
permalink: /07-jupyter-notebooks-r
teaching: 20
exercises: 20
questions:
- "How do I get started in R?"
objectives:
- "Use some basic commands in R"
activity:
 - "Create a sequence, use the sum command, then create a vector and a matrix"
 - "Understand the difference between a matrix and a dataframe, create and add to a dataframe"
keypoints:
 - "Coding is all about little steps. Let's start at the beginning!"
---

# Working in Jupyter Notebooks with R

Now we are going to start using the code cells. We selected the kernel for R when
 we opened the notebook. This means that the code we write using R can be run in the notebook.

It's important to know here that you do not need to be a programmer to use Jupyter Notebooks.
 It is absolutely fine to know just a little bit - what you need - to get to do the
  tasks you want to do. Lots of people find this is a great way to start, and as you
   find better and faster ways of doing things you will gain the motivation to learn
    more about the language.

But for now, what we are doing is showing you a couple of commands that can help
 you automate certain tasks, and all you have to do is copy and paste!

## Create a new cell

Add a new cell using the 'plus' icon. This time we can leave it as a default 'code' cell.

## Comments

If you want to add a comment within the code cell, you can do this if you like.
Just place a hash in front of the comment.

Type

~~~
# For comments inside the code cell use a hash
~~~
{: .language-r}

Click on 'Run' or use the  shortcut **Shift+Enter** to execute the cell.
You can see that the text remains in the cell, which shows 'In' and the number of
 the line next to it. This helps you see that it is a code cell, not a Markdown cell.

## Sequence

Now let's create a sequence of numbers, or integers:

In a new cell, type

~~~
 1:19
~~~
{: .language-r}

Click on 'Run' or use the  shortcut **Shift+Enter** to execute the cell.
See how quickly you can create a sequence, automating a task that you might
otherwise have to do manually?

## Sum

This next bit of code adds up that sequence.

In a new cell, type

~~~
sum(1:19)
~~~
{: .language-r}

Click on 'Run' or use the  shortcut **Shift+Enter** to execute the cell.
This command has added up all of the numbers in the sequence.

## Vector

This sounds 'mathsy' and can go in the 'jargon' type of list that we looked at initially.
 Sometimes you will come across some terms that look unfamiliar or remind you
 of a bad experience in a high school maths class! Fear not! We are here to help.

A vector is a sequence of data elements of the same basic type.  
A vector in programming is a type of list for storing and structuring data.  
Here we are going to assign to `x` the combination of four different components (3, 5, 8, and 9).
 This creates then a shortcut for any manipulation of that sequence of elements.

In this exercise, the letter 'c' is a generic function which combines values in a list,
or vector (the numbers in between the round brackets, separated by commas).
Think of 'c' as in 'combine'.

In a new cell, type

~~~
x = c(3, 5, 8, 9)
sum(x)
~~~
{: .language-r}

Click on 'Run' or use the  shortcut **Shift+Enter** to execute the cell.
This command has added up all of the components of the array.

You can create vectors using different kinds of data.
Let's try some text and see how we can isolate one component of the array:

In a new cell, type

~~~
y = c("Jack", "Queen", "King")
y [1]
~~~
{: .language-r}

Click on 'Run' or use the  shortcut **Shift+Enter** to execute the cell.
This command shows you just the first component of the array.

## Matrix

A matrix is an list of lists, made up of collections of the same data types.  
A matrix in R is like a mathematical matrix, containing all the same type of thing.
Put really simply, it's like data in a table, with rows and columns but all columns
 in a matrix must have the same data type.

In a new cell, type

~~~
matrix(y, 2, 3, byrow=T)
~~~
{: .language-r}

In this example, 'y' is the list of words Jack, Queen, King.
The command 'byrow=T' indicates that the matrix should be filled by rows.

Click on 'Run' or use the  shortcut **Shift+Enter** to execute the cell.
This command shows you all of the components of the list as a matrix.
The '2' is the number of rows. The '3' is the number of columns.


> ## Activity
>
> 1. Create your own sequence, changing the numbers so you can see how you can create
 long sequences of numbers.
> 2. Use the sum command on the sequence you created.
> 3. Create a new vector using numbers, and use the sum command to calculate the sum of
all components.
> 4. Create a new vector using text, and use square brackets to select any single element
of the list (selecting different positions in that list).
> 5. Have a go at manipulating the matrix data display. Can you change it to one column
 and three rows? Three columns and ten rows?
{: .challenge}

## Dataframe

A dataframe combines features of matrices and lists. All columns in a matrix must have the same
 data type (numeric, character, etc.). A dataframe is more general than a matrix, in that
  different columns can have different types of data (numeric, character, factor, etc.).
  Just like a table in a database or an Excel spreadsheet.

Let's create a dataframe, with column headings.

In a new cell, type

~~~
employee <- c("Juanita Lopez", "Peter Gynn", "Jolie Talofa")
salary <- c(81000, 83400, 96800)
startdate <- as.Date(c("2010-11-1", "2008-3-25", "2007-3-14"))
~~~
{: .language-r}

In these commands we are assigning the data to a heading.
The `<-` symbol is used to assign a value to a variable in R.

Note: **<** and **-** should be used together and be written without using a space.

Continue in the same cell. Type

~~~
employ.data <- data.frame(employee, salary, startdate)
employ.data <- data.frame(employee, salary, startdate, stringsAsFactors = FALSE)
employ.data
~~~
{: .language-r}

In these commands we are assigning each of the data groups to the main employee dataset.

Click on 'Run' or use the  shortcut **Shift+Enter** to execute the cell.
This group of commands shows you all of the components of the array as a table with headings for each column.
The '2' is the number of rows. You have also assigned the dates a machine readable date format.


> ## Activity
>
> Add a new employee, salary and start date to this dataframe.
>
{: .challenge}

> ## Matrix vs dataframe
>
> The difference between a matrix and a dataframe can be hard to understand -
this article might help (might not!):
>
> [What is the difference between a matrix and a dataframe in R?](https://www.quora.com/What-is-the-difference-between-a-matrix-and-a-dataframe-in-R)
{: .callout}


