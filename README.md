## Description
  
   This is the latest version of Horus 3D scanner software available here https://github.com/bqlabs/horus.
   
## How to run

  Before running this docker container you need to allow remote X11 connection on your X11 session :
```
fcr@nux-linux:~/> xhost +
```

  Then the container in privileged mode with X11 access :
   
```
docker run -it --rm 
    --name horus 
    --privileged 
    -e DISPLAY=$DISPLAY 
    -v /tmp/.X11-unix:/tmp/.X11-unix 
    --device=/dev/video0:/dev/video0:rwm 
    --device=/dev/ttyUSB0:/dev/ttyUSB0:rwm 
    -v ~/projects/horus-docker/horus:/root/.horus 
    horus:0.2
```

  Data is stored on your home directory like if horus is run in your computer.
    
Have fun !

