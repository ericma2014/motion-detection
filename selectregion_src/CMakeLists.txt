cmake_minimum_required(VERSION 2.4)

PROJECT(SELECT_REGION)
# paths 
INCLUDE_DIRECTORIES(src)
INCLUDE_DIRECTORIES(/usr/local/include)
LINK_DIRECTORIES(/usr/local/lib)
LINK_DIRECTORIES(/usr/lib)
SET(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)
SET(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)
SET(CMAKE_CXX_FLAGS "-o3 -w")
SET(CMAKE_CXX_LINK_FLAGS "-pg")
SET(OpenCV_LIBRARIES opencv_core opencv_highgui opencv_imgproc opencv_video)

ADD_EXECUTABLE(selectregion src/selectregion.cpp)
TARGET_LINK_LIBRARIES(selectregion ${OpenCV_LIBRARIES})
SET(CMAKE_BUILD_TYPE Release)