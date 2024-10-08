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


## Headers

```python
        cherrypy.response.headers['Content-Type'] = 'application/pdf'
        cherrypy.response.headers['Content-Disposition'] = 'attachment; filename="generated_file.pdf"'
```

## JSON

### Decoding (json_in)

```python
@cherrypy.expose
    @cherrypy.tools.json_in()
    def index(self):
        data = cherrypy.request.json
```

### Encoding (json_out)

```python
@cherrypy.expose
    @cherrypy.tools.json_out()
    def index(self):
        return {'key': 'value'}

```

## Configuration

```python
cherrypy.config.update({'server.socket_host': '127.0.0.1',
                        'server.socket_port': 8080,
                       })
```


 





