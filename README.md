# nvidia-virtualgl-selenium-node-base
Base selenium node forked from selenium/node-base to be running with nvidia-docker and VirtualGL on Ubuntu 16.04.

*This image is not intended to be run directly!*
Please use derived images to run a selenium node of a specific browser.
Tested on nvidia-docker 1.0.0 https://github.com/NVIDIA/nvidia-docker/releases

# Launch commands
```bash
xhost +local:root
nvidia-docker run -d \
     --env="DISPLAY" \
     --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" \
     plumbee/nvidia-virtualgl-selenium-node-base
xhost -local:root # resetting permissions
```

# Resources
- selenium git repo https://github.com/SeleniumHQ/docker-selenium
- selenium on docker hub https://hub.docker.com/u/selenium/
- nvidia-docker project https://github.com/NVIDIA/nvidia-docker
- VirtualGl project http://www.virtualgl.org/
