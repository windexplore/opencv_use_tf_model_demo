cmake_minimum_required(VERSION 2.10)

project(ssd)


set(SRC main.cpp)

set(CV_ROOT /usr/local/opencv4)


include_directories(
    ${CV_ROOT}/include/opencv4
)

link_directories(
    ${CV_ROOT}/lib
)

add_executable(ssd ${SRC})


target_link_libraries(
    ssd
    opencv_calib3d
    opencv_core
    opencv_dnn
    opencv_features2d
    opencv_flann
    # opencv_gapi
    opencv_highgui
    opencv_imgcodecs
    opencv_imgproc
    opencv_ml
    opencv_objdetect
    opencv_photo
    opencv_stitching
    opencv_videoio
    opencv_video
)



