cmake_minimum_required(VERSION 2.6 FATAL_ERROR)

project(PrincipalCurvaturesEstimation)

find_package(PCL 1.0 REQUIRED COMPONENTS io)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable(PrincipalCurvaturesEstimation PrincipalCurvaturesEstimation.cpp)

target_link_libraries(PrincipalCurvaturesEstimation
pcl_io
pcl_common
pcl_features
pcl_search
pcl_filters
pcl_kdtree
pcl_surface
pcl_keypoints
)