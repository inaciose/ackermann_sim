# ackermann_sim

+ Gazebo ackermann_simulation with teleop

+ Required distro packages

sudo apt install ros-noetic-ros-controllers

sudo apt-get install ros-noetic-ackermann-msgs

+ core simulation launch (waiting for /ackermann_vehicle/ackermann_cmd)

roslaunch ackermann_vehicle_gazebo ackermann_vehicle.launch

rostopic pub /ackermann_vehicle/ackermann_cmd ackermann_msgs/AckermannDriveStamped "header:
  seq: 0
  stamp:
    secs: 0
    nsecs: 0
  frame_id: ''
drive: {steering_angle: 1.0, steering_angle_velocity: 1.0, speed: 3.0, acceleration: 3.0,
  jerk: 0.0}"


+ Teleop simulation with twist converted to ackermann messages

roslaunch ackermann_vehicle_gazebo vehicle_sim.launch

roslaunch ackermann_vehicle_gazebo teleop.launch


http://docs.ros.org/en/api/ackermann_msgs/html/index-msg.html


