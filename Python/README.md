# Python ressources

Virtual Environments https://www.youtube.com/watch?v=0f3moPe_bhk

String Formatting tutorial https://www.youtube.com/watch?v=ktOOKv6XJ7U

Advanced Python Mastery https://github.com/dabeaz-course/python-mastery.git


## Virtual Environments

### Virtualenv

```lsvirtualenv```

### Conda

```conda info --envs```

```conda create --name <my-env>```

```conda activate <my-env>```


## Packages

List all installed: ```pip list```

Clear cache: ```python -m pip cache purge```


## Requirements

Export ```pip freeze > requirements.txt```

 ```pip install -r requirements.txt```


## Datatypes (most used)

Simple: String, Float, Integer, Boolean

Composed:

Lists: ```[ "val1", "val2", "val3" ]```

Dictionaries: 

```
{ "key1":"val1", "key2":"val2", "key3":"val3" }
```

Sets (unmutable):

```
{ "val1", "val2", "val3" }
```

Tuples (unmutable): ```( "val1", "val2", "val3" )```

Range: ```range(10)```

To get a variable type: ```type(var)```


## Casting

To integer: ```int()```

To float: ```float()```

To string: ```str()```


## String Methods

Slicing: ```var_name[a:b]``` a = start, b = end (not included) or ```var_name[a:]``` or ```var_name[:b]```

Replace: ```var_name.replace("search", "replaceby")```

Split and Join: ```var_name.split("sep")``` and ```"sep".join(iterable)```

Remove whitespaces: ```var_name.strip()``` also ```var_name.lstrip()``` and ```var_name.rstrip()```

F-Strings: ```print(f"some text {var_name}")``` (also can do math operations inside)

Search: ```var_name.index()``` and ```var_name.find()``` (find() method returns -1 if the value is not found)

Check if: ```var_name.isdecimal()``` or ```var_name.isnumeric()``` (if all the characters are numeric)


## Loops

Loop over a collection of items while keeping track of the current item’s index
```python
names = ['Bob', 'Alice', 'Guido']
for index, value in enumerate(names):
    print(f'{index}: {value}')
```

## Functions

```python
def my_function(arg1,arg2="default"):
  print("Demo")
```

Also Supports: Arbitrary Arguments (*args), Keyword Arguments, Arbitrary Keyword Arguments (**kwargs)


## Lambda

A lambda function is a small anonymous function. It can take any number of arguments, but can only have one expression.

```python
lambda arguments : expression
```

## Error Fixing

Pip SSL error https://www.youtube.com/watch?v=g9AeWgZJTZA



