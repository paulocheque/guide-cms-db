#### Table of Contents

1. ##### Introduction
 - What are docstrings
 - Why would we use them
 - When should we use them
 - How to write them
2. ##### Formatting
 - Docstring Styles
 - Sections
 - Optimizing readability
3. ##### Documentation
 - How to document a class
 - How to document a function

<br><br>
#### What are docstrings
---
Okay, so many of you may be asking "What is a docstring, I've never heard of it", (if you have, then all the better). Well, docstrings are rather like comments e.g. `# This be a comment`. However, as you may know well, trying to explain what a `function` or `class` does in a one-line comment can be quite difficult. Here's an example of what can happen if you do

```python
def lowerfirst(string):
    # This function takes an input string, and if the string is equal to the word "I", it will simply return that word
    # However, if the string is not equal to "I", it will attempt to lower the first letter by assigning it to a temporary
    # variable, tmp, and will then append all following letters to it, returning this value once finished
    # WARNING: This will break if the word given is only 1 letter long and not equal to "I"
    if string == "I":
        return string
    else:
        tmp = string[0].lower()
        for i in range(1,len(str)):
            tmp += i
        return tmp
```

#### When should we use them
----
Docstrings should generally be used only where a one-line comment just doesn't do the trick. One should also refrain from putting docstrings outside of a function or class, as without context, they are just about useless. We will go over this in more detail in [How to write them](#how-to-write-them)

#### Why should we use them
---

As you can see, even for a relatively simple function, documenting using comments quickly makes it unpleasant and difficult to read. So, to solve this, the docstring was introduced. A docstring is simply a multi-line string, that is not assigned to anything, e.g.

```python
"""Here be a docstring
It can have multiple lines
                            Or spaces.
You can even include stuff like 
print("This is a docstring"), and it won't cause problems
"""
```

Using this method, our documentation of `lowerfirst()` becomes far more tidy

```python
def lowerfirst(string):
    """
    This function takes an input string, and if the string is equal to the word "I", it will simply return that word.
    This function takes an input string, and if the string is equal to the word "I", it will simply return that word
    However, if the string is not equal to "I", it will attempt to lower the first letter by assigning it to a temporary
    variable, tmp, and will then append all following letters to it, returning this value once finished
    
    WARNING: This will break if the word given is only 1 letter long and not equal to I
    """
    
    """
    fix this markdown hates python docstrings, so I have to do this to fix it in the meantime
    """
    
    
    if string == "I":
        return string
    else:
        tmp = string[0].lower()
        for i in range(1,len(str)):
            tmp += i
        return tmp
```

As you can see, it considerably easier to read. However, you maybe wondering, "Well, sure, it's easier, but why do it when it's nearly identical to a comment. To answer that, you should keep reading

#### How to write them
----


Uses
***

While docstrings can be used as a kind of glorified comment, there is actually a lot more to them. In example, docstrings are often used by documentation generators, such as [Sphinx](http://www.sphinx-doc.org/en/stable/), and [DocUtils](http://docutils.sourceforge.net/), among many others. Another function is unit tests, something that is extremely helpful when working on a large scale project. These tests take the form of the output of the interactive Python console, making it easy to not only write the test yourself, but also can be copy pasted directly from a python prompt. 

For example:

```python
    def lowerfirst(string):
    """
    This is an example unittest docstring
    
        >>> lowerfirst("I")
            "I"
        >>> lowerfirst("Hello")
            "hello"
        >>> lowerfirst("A")
            Traceback (most recent call last):
                File "<input>", line 1, in <module>
            IndexError: string index out of range
        >>>

    """
    
    """
    fix this markdown hates python docstrings, so I have to do this to fix it in the meantime
    """
    
    
    if string == "I":
        return string
    else:
        tmp = string[0].lower()
        for i in range(1,len(str)):
            tmp += i
        return tmp
```

The above will be used by test systems, such as `nose` and `unittests`. These tools use these embedded tests to run a test, taking the user input, (sections labeled with `>>>`), and execute it. If the returned value doesn't match the one below, the test will fail. This also doubles as an example of usage for other developers. 

Another immensely useful functionality for documentation is the fact that docstrings use [ReStructuredText](http://docutils.sourceforge.net/rst.html), or ReST, to allow for formatting. While bearing similarities to Markdown, it can do alot more. This is where docstrings really come into their own. As well as allowing you to just write, you can also specify what arguments it takes, what it returns amongst several other sections. While easy to read in raw, tools like Sphinx, will use these for formatting. 

Here are some examples:

```python
def lowerfirst(string):
    """Returns the given string with the first letter lowered
    This is the documentation for the `lowerstring()` function, it will include the use of all common ReST sections
    Args:
        string (str): the string to process
    
    Returns:
        tmp (str): The string processed and lowered as necessary
    
    """
    
    """
    fix this markdown hates python docstrings, so I have to do this to fix it in the meantime
    """
    
    
    if string == "I":
        return string
    else:
        tmp = string[0].lower()
        for i in range(1,len(str)):
            tmp += i
        return tmp
```

So, what does the above do. Well, in the given example there are several elements at play. I will explain these now

Elements of this docstring:
- \``localstring()`\`: The `, or backtick, is used just like in Markdown, to mark inline code highlighting
- `Returns:`: This marks the beginning of return values and type specification. 

