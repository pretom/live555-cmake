
#project name
PROJECT(groupsock)


#head file path
INCLUDE_DIRECTORIES(
    ../UsageEnvironment/include
    ../groupsock/include
    ${PROJECT_SOURCE_DIR}/include 
)
#source directory
AUX_SOURCE_DIRECTORY(src DIR_SRCS)

file( GLOB SRC_FILES  ./*.cpp ./*.c)

ADD_LIBRARY(libgroupsock ${SRC_FILES} )

TARGET_LINK_LIBRARIES(libgroupsock libBasicUsageEnvironment)
