cmake_minimum_required(VERSION 2.8.3)
project(rosjava_dynamic_reconfigure)

find_package(catkin REQUIRED
  rosjava_build_tools

  dynamic_reconfigure
)

catkin_rosjava_setup(publishMavenJavaPublicationToMavenRepository)

catkin_package()

install(DIRECTORY ${CATKIN_DEVEL_PREFIX}/${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rosjava/${PROJECT_NAME}/
        DESTINATION ${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rosjava/${PROJECT_NAME})
