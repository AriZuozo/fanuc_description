#fanuc_description

1) Open a new shell in catkin_ws

2) Now you can build your progect with: catkin build

3) source devel/setup.bash

5) At this point, you can visualize your product with this command in RVIz:
  roslaunch urdf_tutorial display.launch model:=src/fanuc_description/robot/fanuc_m20ia.urdf



# Fanuc M20iA Config.

1) Open a new shell in catkin_ws

2) Now you can build your progect with: catkin build

3) source devel/setup.bash

4) Open the Moveit assistant config:
  roslaunch moveit_setup_assistant setup_assistant.launch
  
5) When the program is opened, open ' fanuc_m20ia_config.urdf" in fanuc_description/robot


# tf_listener_fanuc

1) Open a new shell in catkin_ws

2) Now you can build your progect with: catkin build

3) source devel/setup.bash

4) Launch the node master: 
  rosrun 
  
5) Open another shell and make the source: 
  source devel/setup.bash
  
6) Now launch the node listener:
  rosrun name_package name_node 
