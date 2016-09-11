# Introduction to some basic elements of Python (part I)

## Overview

- [Data types](#data-types-revisited) (5 minutes) - DW
- [Lists and indices](#lists-and-indices) (15 minutes) - DW
- [Concept of objects](#the-concept-of-objects) (5 minutes) - DW

## Data types revisited
1. We saw a bit about variables and their values in the lesson last week, and we continue today with some variables related to rock samples collected on a recent field excursion.
For a given rock sample, the standard for assigning a sample identification value is to use the format `PE-LO-NU-YR`, where `PE` is for the first and last initials of the person that collected the sample, `LO` is a two-letter abbreviation for the sample location, `NU` is the sample number on that excursion, and `YR` is the last two digits of the year in which the sample was collected.
We can store this information and some additional information about the samples in Python as follows:

    ```python
    SampleID = 'DW-NP-48-16'
    SampleNumber = 48
    SampleMassLbs = 6.89
    SampleRockType = 'Mica schist'
    ```
Here we have 4 values assigned to variables related to a single rock sample.
Each variable has a unique name and they can store different types of data.

2. We can explore the different types of data stored in variables usint the `type()` function.
There are 4 basic *data types* in Python as shown in the table below.

    | Data type name | Data type            | Example         |
    | -------------- | -------------------- | --------------- |
    | `int`          | Whole integer values | `4`             |
    | `float`        | Decimal values       | `3.1415`        |
    | `str`          | Character strings    | `'Hello'`       |
    | `bool`         | True/false values    | `True`          |
As you will see, the data types are important because some are not compatible with one another.

    ```python
    >>> type(SampleNumber)
    int
    >>> type(SampleMassLbs)
    float
    >>> type(SampleRockType)
    str
    ```

3. Ok. So we can get the data types for variables in Python using the `type()` function, but why does this matter?
The main reason is that some types of data are compatible with one another, while others are not.

    ```python
    >>> SampleMassLbs * 25     # Estimate mass of 25 samples
    172.25
    >>> SampleMassLbs / 2.2    # Calculate sample mass in pounds
    3.1318181818181814
    ```
In Python 3 is it generally not a problem to multiply or divide `int` and `float` variables.
As you might expect, you can also multiply them by themselves.

    ```python
    >>> SampleMassLbs * SampleMassLbs
    47.4721
    ```
The trouble can arise when trying to use mathematical operations with incompatible data types.

    ```python
    >>> SampleMassLbs + SampleID
    ---------------------------------------------------------------------------
    TypeError                                 Traceback (most recent call last)
    <ipython-input-20-75e50db6ddf4> in <module>()
    ----> 1 SampleMassLbs + SampleID

    TypeError: unsupported operand type(s) for +: 'float' and 'str'
    ```
Here we get a `TypeError` because Python does not know how we are expected to combine a string of characters (`SampleID`) with a decimal value number (`SampleMassLbs`).

4. Interestingly, some operations combining numbers and `str` values will work.

    ```python
    >>> SampleID * 3
    'DW-NP-48-16DW-NP-48-16DW-NP-48-16'
    ```
Here the values in the `SampleID` variable are simply repeated 3 times.

5. One of the nice options in IPython is that you can see which variables are in memory and their values by typing `%whos`.

    ```python
    >>> %whos
    Variable         Type     Data/Info
    -----------------------------------
    SampleID         str      DW-NP-48-16
    SampleMassLbs    float    6.89
    SampleNumber     int      48
    SampleRockType   str      Mica schist
    ```
`%whos` is an IPython magic command that will not work in a standard Python interpreter window.
We will see other magic commands as we learn more Python.
They're useful!

## Lists and indices
As we've seen above, my recent field excursion involved collecting (at least) 48 rock samples.
Rather than having individual variables for each of those samples, we can store many related values in a *collection*.
The simplest type of *collection* in Python is a **list**.

1. Let's first create a list of selected `SampleID` values.

    ```python
    >>> SampleIDs = ['DW-NP-03-16', 'DW-NP-12-16', 'DW-NP-33-16', 'DW-NP-48-16']
    >>> print(SampleIDs)
    ['DW-NP-03-16', 'DW-NP-12-16', 'DW-NP-33-16', 'DW-NP-48-16']
    >>> type(SampleIDs)
    list
    ```
Here we have a list of 4 `SampleID` values in a list called `SampleIDs`.
As you can see, the `type()` function recognizes this as a list.
Lists can be created using the square brackets (`[` and `]`), with commas separating the values in the list.
2. To access an individual value in the list we need to use an **index value**.
An **index value** is a number that refers to a given position in the list.
Let's check out the first value in our list as an example:

    ```python
    >>> print(SampleIDs[1])
    'DW-NP-12-16'
    ```
Wait, what?
This is the second value in the list we've created, what is wrong?
As it turns out, Python (and many other programming languages) start values stored in collections with the index value 0.
Thus, to get the value for the first item in the list, we must use index 0.

    ```python
    >>> print(SampleIDs[0])
    'DW-NP-03-16'
    ```
OK, that makes sense now, but it may take some getting used to...
3. We can find the length of a list using the `len()` function.

    ```python
    >>> len(SampleIDs)
    4
    ```
Just as expected, there are 4 values in our list and `len(SampleIDs)` returns a value of 4.
4. If we know the length of the list, we can now use it to find the value of the last item in the list, right?

    ```python
    >>> print(SampleIDs[4])
    ---------------------------------------------------------------------------
    IndexError                                Traceback (most recent call last)
    <ipython-input-34-946b174fe444> in <module>()
    ----> 1 print(SampleIDs[4])

    IndexError: list index out of range
    ```
What, an `IndexError`?
    

## The concept of objects
