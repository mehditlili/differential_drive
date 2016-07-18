cmake_minimum_required(VERSION 2.8.3)
project(differential_drive)

find_package(catkin REQUIRED)

catkin_package()

file(GLOB py_files "scripts/*.py")
install(PROGRAMS ${py_files}
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY launch/
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
        FILES_MATCHING PATTERN "*.launch")
