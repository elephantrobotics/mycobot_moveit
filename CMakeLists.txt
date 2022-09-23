cmake_minimum_required(VERSION 2.8.3)
project(mycobot_moveit)

find_package(catkin REQUIRED
	actionlib
	moveit_msgs
)

catkin_package(

	CATKIN_DEPENDS actionlib moveit_msgs
)

install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  PATTERN "setup_assistant.launch" EXCLUDE)
install(DIRECTORY config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
