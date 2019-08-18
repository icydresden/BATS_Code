
aux_source_directory(. DIR_LIB_SRCS) # one folder multi sources

# get the executable file
# add_executable(example src/ff-test.cpp) # one folder one source
# add_executable(example ${DIR_SRCS}) # one folder multi sources
# add_executable(example ${DIR_SRCS}) # one folder multi sources
add_library(ff ${DIR_LIB_SRCS}) # one folder multi sources
