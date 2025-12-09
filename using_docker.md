# Setting up docker in ubuntu

You code outside of docker and then set up docker to pull a directory from your computer


docker rm ros2-mavros

docker run -it \
  --name ros2-mavros \
  --net=host \
  -e DISPLAY=$DISPLAY \
  -v /tmp/.X11-unix:/tmp/.X11-unix \

  -v [Code directory you want to pull into docker]:/root/ros2_ws \
  ros2-mavros



# Opening docker

docker start -ai ros2-mavros

# Opening a new terminal with the same docker
docker exec -it ros2-mavros bash
 