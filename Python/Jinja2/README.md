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


### Rendering

```print(template.render(the="variables", go="here"))```

render() can also take a dictionary as argument


## Advanced

### Loops

```
<ul>
{% for row in rows %}
  <li class="{{ loop.cycle('odd', 'even') }}">{{ row }}</li>
{% endfor %}
</ul>
```

Inner loops:

```
<table>
{% for row in table %}
  <tr>
  {% set rowloop = loop %}
  {% for cell in row %}
    <td id="cell-{{ rowloop.index }}-{{ loop.index }}">{{ cell }}</td>
  {% endfor %}
  </tr>
{% endfor %}
</table>

```

### Conditions

```
<h1>Conditionals in Jinja2</h1>
<h2>Basic Comparisons</h2>

{% if company == "Apple" %}
    <h3>Available {{ company }} Products</h3>
    <ul>
        <li>iPhone</li>
        <li>iPad</li>
        <li>iMac</li>
    </ul>

{% elif company == "Microsoft" %}
    <h3>Available {{ company }} Products</h3>
    <ul>
        <li>Windows Phone</li>
        <li>Surface Pro</li>
        <li>Surface Book</li>
    </ul>

{% else %}
    No {{ company }} products available.

{% endif %}
```

### Inline expressions

```
{% set x = 'apples' if 13 is even else 'oranges' %}
{{ x }}
```

### Base Template

```
<!DOCTYPE html>
<html lang="en">
<head>
    {% block head %}
    <link rel="stylesheet" href="style.css" />
    <title>{% block title %}{% endblock %} - My Webpage</title>
    {% endblock %}
</head>
<body>
    <div id="content">{% block content %}{% endblock %}</div>
    <div id="footer">
        {% block footer %}
        &copy; Copyright 2008 by <a href="http://domain.invalid/">you</a>.
        {% endblock %}
    </div>
</body>
</html>
```

### Child Template

```
{% extends "base.html" %}
{% block title %}Index{% endblock %}
{% block head %}
    {{ super() }}
    <style type="text/css">
        .important { color: #336699; }
    </style>
{% endblock %}
{% block content %}
    <h1>Index</h1>
    <p class="important">
      Welcome to my awesome homepage.
    </p>
{% endblock %}
```
