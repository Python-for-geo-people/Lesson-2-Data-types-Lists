# Writing your own Python scripts

As you may be noticing by now, it isn't that convenient to type in all of the commands you would like to use in the IPython interpreter window. 
An alternative to typing in all of the commands you would like to run is the list them in a Python script file.
A Python script file is simple a file containing a list of the command you would like to run, with one command per line, 
and formatted in the same way as if you were to type them in.
Python script files traditionally use the `.py` file extension in their names.

## Getting started
1. To start creating and editing our Python script file, we'll need to open a text editor.
In our case, we'll be using the **gedit** basic editor, which can be launched by double clicking on the **Text editor** icon on the desktop of your computer instance.
2. The **gedit** window will appear shortly after double clicking, and it should open a new (blank) document by default.
You're now ready to proceed.

## The general concept of a `.py` script file
A Python script file is simply a list of commands that you might otherwise type into the IPython interpreter window.
As such, we can quite easily create a basic script file and test things out.

1. Start by copying and pasting the text below into your **gedit** window.

    ```python
    SampleID = "DW-NP-48-16"
    SampleWeightLbs = 6.89
    print("Sample", SampleID, "weighs", SampleWeightLbs, "pounds")
    ```
2. Save this script file as `sampleinfo.py` in your home directory `/home/geo' by clicking on **File -> Save** in the menu bar of the **gedit** window.
Click on the **Home** icon on the top left of the **Save As** window that appears, and enter the file name as `sampleinfo.py`.
Click the `Save` button on the lower right of the window to save the file.
3. Return to your IPython interpreter window (or start a new one if you have closed it), change the directory in IPython to the home directory by typing `cd`, and run the script using the `%run` magic command in IPython.
Before pressing enter on the second line, what do you expect to see as output when the script runs?

    ```python
    >>> cd
    >>> %run sampleinfo.py
    Sample DW-NP-48-16 weighs 6.89 pounds
    ```
No surprises here.
The script simply executes the commands exactly as you would have if you had typed them in to the IPython interpreter.
4. Now let's make a small change to the script.
Go back to **gedit** and edit the script so that it now reads

    ```python
    SampleID = "DW-NP-48-16"
    SampleWeightLbs = 6.89
    SampleRockType = "Mica schist"
    print("Sample", SampleID, "is a", SampleWeightLbs, "pound chunk of", SampleRockType)
    ```
Save your changes.
5. Once again, go back to the IPython interpreter and use the `%run` magic command to run the modified script.
Don't worry, we'll cover a much better way to edit and test scripts later in today's lesson.

    ```python
    >>> %run sampleinfo.py
    Sample DW-NP-48-16 is a 6.89 pound chunk of Mica schist
    ```

## Writing our scripts the "right" way
So we have an example above of a Python script that works, but there are a number of additions that could be made to improve even this simple script.
1. 

## General format
We should probably provide some kind of simple template here for writing **basic** Python scripts "the right way".
It could be a simplified version of [something like this](https://gist.github.com/nhoffman/3006600).
For me, this would include (at least):

1. A comment block at the start of the script using block comments (`'''`). This should give the basic information about what the script does in a semi-Pythonic way.
2. Inline comments (`#`) for the different sections of the code (and possibly on most lines) to clearly state how the code works.

To start, I think it would be good to avoid things like using a `main()` function and some of the other Python practices that might make it harder to understand how the script works in a simple way.
Avoiding `main()` is also nice because when students use **Spyder** they will be able to see the variable values in the variable browser.
