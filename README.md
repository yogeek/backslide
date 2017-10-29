# Backslide

Backslide tool for HTML presentation in docker
https://github.com/sinedied/backslide

## Workflow

```
$ # Init new project
$ mkdir app
$ cd !$
$ docker run -it --rm -v $(pwd):/app -w /app yogeek/baskslide bs init
Presentation initialized successfully
$ # You can now edit presentation.md on your host...

$ # Start a development server with live reload (on port 4100 in this example)
$ docker run -it --rm  -v $(pwd):/app -w /app -p 4100:4100 yogeek/baskslide bs serve
[Browsersync] Access URLs:
 --------------------------------
    Local: http://localhost:4100
 External: http://172.17.0.2:4100
 --------------------------------
[...]
$ # Open http://localhost:4100 in your browser
$ # or http://$(docker-machine ip):4100 if using docker-machine

$ # Export slides as HTML
$ docker run -it --rm -v $(pwd):/app -w /app yogeek/baskslide bs export

$ # Export slides as PDF
$ docker run -it --rm -v $(pwd):/app -w /app yogeek/baskslide bs pdf
```

