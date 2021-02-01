cmake_minimum_required(VERSION 3.17)

project(2021_1_27)

set(CMAKE_CXX_STANDARD 20)

add_executable(2021_1_27 main.cpp)

# Where to find OpenCV

set(OpenCV_DIR "D:/opencv/mingw-build/install")

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")

find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})

# add libs you need

set(OpenCV_LIBS opencv_core opencv_imgproc opencv_highgui opencv_imgcodecs)

# linking

target_link_libraries(2021_1_27 ${OpenCV_LIBS})
