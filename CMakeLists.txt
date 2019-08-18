# minimun version
cmake_minimum_required(VERSION 3.0.0)

# project name
project(simBats VERSION 0.1.0)

# search all the source file in the dir
# and store them in DIR_SRCS 
# aux_source_directory(<dir> <variable>)
aux_source_directory(include DIR_SRCS) # one folder multi sources

# 添加 math 子目录
add_subdirectory(include)

# get the executable file
# add_executable(example src/ff-test.cpp) # one folder one source
# add_executable(example ${DIR_SRCS}) # one folder multi sources
# add_executable(example ${DIR_SRCS}) # one folder multi sources
add_executable(simBats simBats.cpp ${DIR_SRCS}) # one folder multi sources


# 添加链接库
# target_link_libraries(example echo)
# target_link_libraries(example ff)


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
