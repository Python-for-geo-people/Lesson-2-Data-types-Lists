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

## The concept of objects
