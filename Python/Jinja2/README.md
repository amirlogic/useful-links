# Jinja2

Jinja uses a central object called the template Environment. Instances of this class are used to store the configuration and global objects, and are used to load templates from the file system or other locations. Even if you are creating templates from strings by using the constructor of Template class, an environment is created automatically for you, albeit a shared one.

## Basics

### Init

```python
from jinja2 import Environment, FileSystemLoader, select_autoescape
env = Environment(
    loader=FileSystemLoader(''),
    autoescape=select_autoescape()
)
```

### Loading a template

```template = env.get_template("mytemplate.html")```


## Rendering

```print(template.render(the="variables", go="here"))```



