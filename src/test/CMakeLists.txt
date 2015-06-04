#
#   Test directory
#

add_subdirectory(gtest)

add_executable(test.bin test.cpp)
target_link_libraries(test.bin PRIVATE gtest_main)
add_custom_command(TARGET test.bin POST_BUILD COMMAND test.bin)
