# Joint Client Python Implementation

<br>

## Joint Client creation

Open a terminal inside scripts folder and create a file name joint_client.py.
Copy the content from joint_client.txt and paste. Open a terminal in the same location and Run

```sh
chmod +x joint_client.py
```

to enable execute permission.

<br>

## CMakeLists.txt file modifications

Open lab_4_jointspacecontrol/CMakeLists.txt and add following lines to the bottom of the file.

```sh
catkin_install_python(PROGRAMS scripts/joint_client.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

```

## Build the code 

Go to root of the workspace

```sh
cd ~/robotics/
```
```sh
catkin build
```
or
```sh
catkin_make
```

## Run the Joint Client

Go to root of the workspace and run

```sh
roscore
```

Go to root of the workspace and on a new terminal

```sh
cd ~/robotics/
```
```sh
source devel/setup.bash
```
```sh
rosrun lab_4_jointspacecontrol joint_client.py
```

[<< Back to Main menu](../README.md)