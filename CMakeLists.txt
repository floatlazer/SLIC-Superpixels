cmake_minimum_required(VERSION 2.6)
project(SLIC-Superpixel)

find_package(OpenCV REQUIRED
            PATHS /usr/local/Cellar/opencv@2/2.4.13.6_2
            NO_DEFAULT_PATH)

message("${OpenCV_CONFIG}")

add_executable(test_slic slic.cpp test_slic.cpp)

target_link_libraries(test_slic ${OpenCV_LIBS})
