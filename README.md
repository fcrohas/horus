docker run -it --rm --name horus --privileged -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix --device=/dev/video0:/dev/video0:rwm --device=/dev/ttyUSB0:/dev/ttyUSB0:rwm horus:0.2 horus

