cmake_minimum_required(VERSION 3.5.0)
project(ridgeback_description)

if($ENV{ROS_VERSION} VERSION_EQUAL "1")
  find_package(catkin REQUIRED)
  install(DIRECTORY meshes urdf
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  )
  catkin_package()
else()
  find_package(ament_cmake REQUIRED)
  install(DIRECTORY 
    meshes urdf
    DESTINATION share/${PROJECT_NAME}/
  )
  ament_package()
endif()
