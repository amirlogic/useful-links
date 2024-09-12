# CherryPy

Lightweight Web Framework for Python



## Basic App (Hello World)

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


## Configuration

```python
cherrypy.config.update({'server.socket_host': '127.0.0.1',
                        'server.socket_port': 8080,
                       })
```

Export ```pip freeze > requirements.txt```

 





