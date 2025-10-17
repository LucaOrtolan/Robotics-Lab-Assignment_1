Open terminator.

In one terminal, run rViz with the following line:

`ros2 launch interbotix_xsarm_moveit xsarm_moveit.launch.py robot_model:=rx200 hardware_type:=actual`

Change hardware_type to `fake` to run on rViz, `gz_classic` to run on simulation.

Open another terminal, move to this directory, and run the following lines:

`colcon build`

`source install/setup.bash`

`ros2 run rx200_moveit_control rx200_moveit_client`

Make sure the ROS_DOMAIN_ID is the same for both terminals. To ensure so run:

`echo $ROS_DOMAIN_ID`

To modify it run:

`export ROS_DOMAIN_ID={number}`

In my case {number} = 13