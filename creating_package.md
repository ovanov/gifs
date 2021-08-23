<h1 align="center">Creating Python package</h1>
<p align="center">Make your code installable</p>

The following text will show you how to take the necessary steps, in order to make your code installable and ready to use. The concept PyPi will be shown, but will not be elaborated upon. The concept of packaging is explained in detail in the [publishing article](https://packaging.python.org/tutorials/packaging-projects/).

## Clean up your code

### Remove print statements
Most of us debug our projects by using '`print`' statements all over the place. The first step in the creation of a package is to *remove all unnecessary '`print()`' statements*. This way, the user will not be bothered by random outputs. If you need to inform the user about certain code behaviour, use [logging](https://docs.python.org/3/library/logging.html). With a dedicated logging system, the user can use its contents when they want.

### Use classes and functions
Make sure that all of your code is used by a class or a function, otherwise the residual code pieces are run every time, when the package is imported. Example code can be included as a comment in the magic '`__main__`' function or in a dedicated example folder.


## Creating a package
In order to create a package, your file / direcory structure should also be as the official [packaging documentation](https://packaging.python.org/tutorials/packaging-projects/) suggests.

### Directory and file structure
Firstly, you should *create a folder with the same name as your package*. Secondy, place your python classes and scripts in the folder that you've created before. Lets assume that in our example we are creating a package that is called 'MyPack'. The directory structure should now look like the following:

    MyPack
    │
    ├── classA.py
    └── script1.py
    
Now, in order for python to recognize this directory as a module, you have to place an '`__init__`.py' in this directory. This special file will hold all the `import` statements from your scripts and classes. In our case, this would look like this: 

<script src="https://gist.github.com/ovanov/8ee4b13ff07571dfae49c3880de0b5e0.js"></script>



