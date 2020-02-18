cmake_minimum_required(VERSION 3.5.0)
project(ridgeback_description)

if($ENV{ROS_VERSION} VERSION_EQUAL "1")

  find_package(catkin REQUIRED)

  catkin_package()

else()

  find_package(ament_cmake REQUIRED)

  ament_package()

endif()

install(DIRECTORY meshes/
  DESTINATION ${PROJECT_NAME}/share/meshes
)

install(DIRECTORY urdf/
  DESTINATION ${PROJECT_NAME}/share/urdf
)
