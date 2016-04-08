# My course records of Python for Everybody Specialization (except Capstone) for free.

# Extra Information about Python
```
Source: http://stackoverflow.com/questions/17130975/python-vs-cpython
```
## CPython
CPython is the original Python implementation. It is the implementation you download from Python.org. People call it CPython to distinguish it from other, later, Python implementations, and to distinguish the implementation of the language engine from the Python programming language itself.

The latter part is where your confusion comes from; you need to keep Python-the-language separate from whatever runs the Python code.

CPython happens to be implemented in C. That is just an implementation detail really. CPython compiles your python code into bytecode (transparently) and interprets that bytecode in a evaluation loop.

CPython is also the first to implement new features; Python-the-language development uses CPython as the base, other implementations follow.

## What about Jython, etc.
Jython, IronPython and PyPy are the current 'other' implementations of the Python programming language; these are implemented in Java, C# and RPython (a subset of Python), respectively. Jython compiles your Python code to Java bytecode, so your Python code can run on the JVM. IronPython lets you run Python on the Microsoft CLR. And PyPy, being implemented in (a subset of) Python, lets you run Python code faster than CPython, which rightly should blow your mind. :-)

## Actually compiling to C
So CPython does not translate your Python code to C by itself. It instead runs a interpreter loop. There is a project that does translate Python-ish code to C, and that is called Cython. Cython adds a few extensions to the Python language, and lets you compile your code to C extensions, code that plugs into the CPython interpreter.
