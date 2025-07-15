cmake_minimum_required(VERSION 2.8)
project(mediactl)

set(MEDIACTL_SRC
    mediactl.c
    v4l2subdev.c
)

add_library(mediactl SHARED ${MEDIACTL_SRC})

# If you have headers, you can add them here
target_include_directories(mediactl PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

install(TARGETS mediactl LIBRARY DESTINATION lib)
install(FILES mediactl.h DESTINATION include)
