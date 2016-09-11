# Writing your own Python scripts

As you may be noticing by now, it isn't that convenient to type in all of the commands you would like to use in the IPython interpreter window. 
An alternative to typing in all of the commands you would like to run is the list them in a Python script file.
A Python script file is simple a file containing a list of the command you would like to run, with one command per line, 
and formatted in the same way as if you were to type them in.

## General format
We should probably provide some kind of simple template here for writing **basic** Python scripts "the right way".
It could be a simplified version of [something like this](https://gist.github.com/nhoffman/3006600).
For me, this would include (at least):

1. A comment block at the start of the script using block comments (`'''`). This should give the basic information about what the script does in a semi-Pythonic way.
2. Inline comments (`#`) for the different sections of the code (and possibly on most lines) to clearly state how the code works.

To start, I think it would be good to avoid things like using a `main()` function and some of the other Python practices that might make it harder to understand how the script works in a simple way.
Avoiding `main()` is also nice because when students use **Spyder** they will be able to see the variable values in the variable browser.
