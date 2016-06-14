# Markdown tutorial by example

Read this if you need to check the Markdown syntax. 

> **Disable the live tutorial to go back to your article**.



# Headers 

## Header's Subsection 

### Header's Subsection 

#### Header's Subsection 

##### Header's Subsection 


# Text Format 

normal, *italic*, **bold**, __bold__, _emphasis_, ~~strikethrough~~, ùníçõd&, `code`, *escaping special chars*, &copy; 

## Bloquote 

> You can put some warning or important messages in blockquotes. 
Check that a blockquote can have multiple lines. 


# Code 

```
print('test')
```

```javascript
$(function(){
  $('div').html('I am a div.');
});
```


# Lists

## Unordered list

- item 1
- item 2

or

* item 1
* item 2

## Ordered list

1. item 1
1. item 2

or

1. item 1
2. item 2

## Nesting

1. item 1
  1. item 1.1
  2. item 1.2
    - subitem 1
    - subitem 2
2. item 2

## Task Listing

- [ ] item 1
- [x] item 2


# Tables

First Column Header | Second Column Header | Third Column
------------------- | -------------------- | ------------
Content from cell 1 | | Content from cell 3
Another cell 1 | Another cell 2


# Links

* [text of the link](http://hackguides.org)
* http://hackguides.org


# Images and Files

![alt text](http://tutorials.pluralsight.com/static/img/dark-logo.png 'Logo Title')


# Horizontal rules

------------------------

or

* * *

or

*****
```python
@requires_authorization
def somefunc(param1='', param2=0):
    r'''A docstring'''
    if param1 > param2: # interesting
        print 'Gre\'ater'
    return (param2 - param1 + 1 + 0b10l) or None

class SomeClass:
    pass
```

```ruby
# The Greeter class
class Greeter
  def initialize(name)
    @name = name.capitalize
  end

  def salute
    puts "Hello #{@name}!"
  end
end

g = Greeter.new("world")
g.salute
```

```javascript
function $initHighlight(block, cls) {
  try {
    if (cls.search(/\bno\-highlight\b/) != -1)
      return process(block, true, 0x0F) +
             ` class="${cls}"`;
  } catch (e) {
    /* handle exception */
  }
  for (var i = 0 / 2; i < classes.length; i++) {
    if (checkCondition(classes[i]) === undefined)
      console.log('undefined');
  }
}

export  $initHighlight;
```

```python
    import time
    import bumpy
    import pandas


    def main():
        df = pandas.DataFrame()

        # We're only dealing with a single column in our profiling but assume we're
        # dealing with code where we get passed a big data frame
        df['a'] = numpy.random.random_integers(0, 10, size=1000000)
        df['b'] = numpy.random.random_integers(0, 10, size=1000000)
        df['c'] = numpy.random.random_integers(0, 10, size=1000000)

        s = time.time()
        df['a'] == 5
        print 'Time for DF slice', time.time() - s

        s = time.time()
        df['a'].values == 5
        print 'Time for ndarray slice', time.time() - s

        # This is also applicable if you want to get the union of several columns.
        # Save the lining up of the indexes, etc. until the last step instead of
        # incurring that overhead on each slice.
        s = time.time()
        df_slices = df[(df['a'] == 1) & (df['b'] == 1) & (df['c'] == 1)]
        print 'Time for DF slice', time.time() - s

        s = time.time()
        slice_a = df['a'].values == 1
        slice_b = df['b'].values == 1
        slice_c = df['c'].values == 1
        nd_slices = df[slice_a & slice_b & slice_c]
        print 'Time for ndarray slice', time.time() - s

        # Just double check that both methods returned same data
        pandas.util.testing.assert_frame_equal(df_slices, nd_slices)

    if __name__ == '__main__':
        main()
```
