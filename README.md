# val_grasping
Test of grasping controllers for valkyrie

~~~
# after build and install
roslaunch val_grasping val_grasping.launch &

rostopic pub --once /right_hand_position_controller/command std_msgs/Float64MultiArray '{ data: [1.4, 0, 0, 0, 0] }'
rostopic pub --once /right_hand_position_controller/command std_msgs/Float64MultiArray '{ data: [1.4, 0.55, 1.1, 0.9, 1.0] }'

rostopic pub --once /left_hand_position_controller/command std_msgs/Float64MultiArray '{ data: [1.4, 0, 0, 0, 0] }'
rostopic pub --once /left_hand_position_controller/command std_msgs/Float64MultiArray '{ data: [1.4, -0.55, -1.1, -0.9, -1.0] }'
~~~
