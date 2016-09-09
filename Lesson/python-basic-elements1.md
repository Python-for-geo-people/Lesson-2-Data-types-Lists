# Introduction to some basic elements of Python (part I)

## Overview

- [Data types](#dtypes) (5 minutes) - DW
- [Lists and indices](#lists) (15 minutes) - DW
- [Concept of objects](#objects) (5 minutes) - DW

##<a name='dtypes'></a> Data types revisited
1. We can start by defining a few variables.
    ```python
    ...
    ```

2. One of the nice options in IPython is that you can see which variables are in memory by typing `%whos`.

```python
>>> %whos
Variable                  Type      Data/Info
---------------------------------------------
TemperatureInFahrenheit   float     59.0
temp_celsius              float     20.0
```

3. There are 4 basic *data types* in Python as shown in the table below.

    | Data type name | Data type            | Example         |
    | -------------- | -------------------- | --------------- |
    | `int`          | Whole integer values | `4`             |
    | `float`        | Decimal values       | `3.1415`        |
    | `str`          | Character strings    | `'Hot'`         |
    | `bool`         | True/false values    | `True`          |
The data types are displayed when using `%whos`, but can also be found using the `type()` function. As you will see, the data types are important because some are not compatible with one another.

    ```python
    >>> WeatherForecast = 'Hot'
    >>> type(WeatherForecast)
    str
    >>> type(TemperatureInFahrenheit)
    float
    >>> TemperatureInFahrenheit = TemperatureInFahrenheit + 5.0 * WeatherForecast
    ---------------------------------------------------------------------------
    TypeError                                 Traceback (most recent call last)
    <ipython-input-21-7046bdc97a54> in <module>()
    ----> 1 TemperatureInFahrenheit = TemperatureInFahrenheit + 5.0 * WeatherForecast

    TypeError: can't multiply sequence by non-int of type 'float'
    ```

##<a name='lists'></a> Lists and indices

##<a name='objects'></a> The concept of objects
