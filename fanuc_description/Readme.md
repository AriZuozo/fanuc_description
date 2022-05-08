# fanuc_description

This repository contains the xacro and the mesh files for the Fanuc M20iA/35M manipulator. These files are used by the MoveIt! Setup Assistant to generate the SRDF and other utility files.

The `robots` directory contains the following xacro files:

* `fanuc_m20ia_35m.xacro` contains the robot model. This description is built using the modified DH convention and taking the joint position and velocity limits from the official datasheet;

* `slide.model.xacro` contains the model of the slide on which the robot can be mounted;

* `slide.xacro` includes the slide model and connects it to the `world` link;

* `drilling_tool.model.xacro` contains the model of the tool that can be mounted at the robot end-effector;

* `fanuc_m20ia_35m.urdf.xacro` connects the robot to the world;

* `fanuc_m20ia_35m_on_slide.urdf.xacro` includes `fanuc_m20ia_35m.xacro`, `slide.model.xacro` to mount the robot on the slide and `drilling_tool.model.xacro` to  mount the tool at the end-effector.

The frames and the related DH parameters are reported here below. 

![image](doc/media/Fanuc_M20iA_35M_DH_frames.jpg)

|  Joint  | alpha<sub>i-1</sub>| a<sub>i-1</sub> | d<sub>i</sub> |   theta<sub>i</sub>   |
| ------- | ------------------ | --------------- | ------------- | --------------------- |
| Joint 1 |         0          |        0        |     0.525     |  q<sub>1</sub>        |
| Joint 2 |       -pi/2        |       0.15      |       0       |  q<sub>2</sub> - pi/2 |
| Joint 3 |         0          |       0.79      |       0       |  q<sub>3</sub>        |
| Joint 4 |       -pi/2        |       0.15      |     0.86      |  q<sub>4</sub>        |
| Joint 5 |        pi/2        |        0        |       0       |  q<sub>5</sub>        |
| Joint 6 |       -pi/2        |        0        |      0.1      |  q<sub>6</sub>        |
The application order of translations and rotations follows the order of the table columns.

The `meshes` directory contains collision and visual objects. Visual objects include .dae (COLLADA) meshes, used in the URDF visual tags, while collision objects include .stl meshes used in the URDF collision tags. Both visual and collision meshes have been exported from a CoppeliaSim scene built from CAD files.
