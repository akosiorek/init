#
#   Source directory
#
find_package(Glog)

add_executable(main.bin main.cpp)
target_include_directories(main.bin
    PRIVATE ${GLOG_INCLUDE_DIRS}
)
target_link_libraries(main.bin
    PRIVATE ${GLOG_LIBRARIES}
)
target_compile_definitions(main.bin PUBLIC Wall)
