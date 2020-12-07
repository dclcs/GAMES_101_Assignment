cmake_minimum_required(VERSION 3.17)
project(ass1)

set(CMAKE_CXX_STANDARD 14)

find_package(OpenCV REQUIRED)
# 添加头文件
set(GLEW_H /usr/local/Cellar/glew/2.2.0/include/GL)
set(GLFW_H /usr/local/Cellar/glfw/3.3.2/include/GLFW)
set(EIGEN_H /usr/local/Cellar/eigen/3.3.8_1/include/eigen3)
set(OPENCV_H /usr/local/Cellar/opencv@2/2.4.13.7_11/include)
include_directories(${GLEW_H} ${GLFW_H} ${EIGEN_H} ${OPENCV_H})
# 添加目标链接
set(GLEW_LINK /usr/local/Cellar/glew/2.2.0/lib/libGLEW.2.2.0.dylib)
set(GLFW_LINK /usr/local/Cellar/glfw/3.3.2/lib/libglfw.3.3.dylib)
set(OPENCV_LIB /usr/local/Cellar/opencv@2/2.4.13.7_11/lib )
link_libraries(${OPENGL} ${GLEW_LINK} ${GLFW_LINK} )
link_directories(${OPENCV_LIB})


add_executable(ass1 main.cpp rasterizer.hpp rasterizer.cpp Triangle.hpp Triangle.cpp)
target_link_libraries(ass1 ${OpenCV_LIBS})

