project(Test)

# Compile gtest
add_subdirectory(gtest)
include_directories(gtest)


#add_executable(test ...)
target_link_libraries(test gtest)

