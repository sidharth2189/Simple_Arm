# Simple_Arm
ROS project to demonstrate use of nodes

 1.simple_mover node publishes joint angle commands to simple_arm
 
 2.arm_mover node provides a service called safe_move, which allows the arm to be moved to any position within its workspace which has been deemed to be “safe”. The safe zone is bounded by minimum and maximum joint angles, and is configurable via the ROS’ parameter server.
 
 3.look_away node subscribes to a topic where camera data is being published.
 When the camera detects an image with uniform color, meaning it’s looking at the sky, the node will call the safe_move service to move the arm to a new position.
