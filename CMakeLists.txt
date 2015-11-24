cmake_minimum_required(VERSION 2.8.3)
project(c2_ros_msgs)

find_package(catkin REQUIRED COMPONENTS 
	std_msgs 
	message_generation
	geometry_msgs
	)

# Generate messages in the 'msg' folder
add_message_files(FILES
   C2_BHV.msg
   MissionLeg.msg
   KeyValue.msg
   ActuatorControl.msg
   BHVProposer.msg
   State3D.msg
   Trajectory.msg
   C2_STATE.msg)

# Generate added messages and services with any dependencies listed here
generate_messages(DEPENDENCIES 
	geometry_msgs 
	std_msgs
	)

catkin_package(CATKIN_DEPENDS std_msgs message_runtime)