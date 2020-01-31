cmake_minimum_required(VERSION 3.5)
project(display)

add_compile_options(-std=c++11)


find_package(OpenCV)

include_directories(
      include
      ${OpenCV_INCLUDE_DIRS}
)



add_executable(${PROJECT_NAME} display.cpp)


target_link_libraries(${PROJECT_NAME}
     ${OpenCV_LIBRARIES}
)
