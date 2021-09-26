
#project name
PROJECT(BasicUsageEenvironment)

#head file path
INCLUDE_DIRECTORIES(
    ../UsageEnvironment/include
    ../groupsock/include
    ${PROJECT_SOURCE_DIR}/include 
)
#source directory
AUX_SOURCE_DIRECTORY(src DIR_SRCS)

file( GLOB SRC_FILES  ./*.cpp ../groupsock/inet.c)
#set environment variable

ADD_LIBRARY(libBasicUsageEnvironment ${SRC_FILES} )

IF (WIN32)
TARGET_LINK_LIBRARIES(libBasicUsageEnvironment ws2_32)
ENDIF()

TARGET_LINK_LIBRARIES(libBasicUsageEnvironment libUsageEnvironment) 


