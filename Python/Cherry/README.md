# CherryPy

Lightweight Web Framework for Python



## Virtual Environments

### Basic App

```python

import cherrypy

class WebApp(object):
    @cherrypy.expose
    def index(self):
        return "Welcome to CherryPy!"

cherrypy.quickstart(WebApp())
```

## Packages

List all installed: ```pip list```

Clear cache: ```python -m pip cache purge```


## Requirements

Export ```pip freeze > requirements.txt```

 ```pip install -r requirements.txt```





