# Material Starter Environment on Docker

Whats in the box?

* Base install of Node - including `http-server`
* Sublime Text
* tmux
* Clone of [Angular Material Starter](https://github.com/angular/material-start)

Building the image
```bash
  docker build -t robtec/node-materials-devbox .
```
Running the container
- OSX using the `socat` workaround for x11 - [source](https://github.com/docker/docker/issues/8710)
```bash
  docker run -it -e DISPLAY=192.168.59.3:0 -p 8080:8080 robtec/node-materials-devbox
```

After running the container, you will be dropped into the cloned project as `dev`

Serve the `app` on `http://<docker-host>:8080` using `http-server app/`

Use Sublime to edit the source - `subl app/`
