### This does not work?

```python
def lowerfirst(string):
	"""
	This function takes an input string, and if the string is equal to the word I, it will simply return that word.
	This function takes an input string, and if the string is equal to the word I, it will simply return that word
	However, if the string is not equal to I, it will attempt to lower the first letter by assigning it to a temporary
	variable, tmp, and will then append all following letters to it, returning this value once finished
	WARNING: This will break if the word given is only 1 letter long and not equal to I
	"""

	if string == "I":
		return string
	else:
		tmp = string[0].lower()
		for i in range(1,len(str)):
			tmp += i
		return tmp
		
```

### This does work:

```python
def lowerfirst(string):
	"""
	This function takes an input string, and if the string is equal to the word I, it will simply return that word.
	This function takes an input string, and if the string is equal to the word I, it will simply return that word
	However, if the string is not equal to I, it will attempt to lower the first letter by assigning it to a temporary
	variable, tmp, and will then append all following letters to it, returning this value once finished
	WARNING: This will break if the word given is only 1 letter long and not equal to I
	"""
	
	"""
	fix
	"""

	if string == "I":
		return string
	else:
		tmp = string[0].lower()
		for i in range(1,len(str)):
			tmp += i
		return tmp
		
```