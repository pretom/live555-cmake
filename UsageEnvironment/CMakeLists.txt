
#project name
PROJECT(UsageEnvironment)


#head file path
INCLUDE_DIRECTORIES(
    ../UsageEnvironment/include
    ../groupsock/include
    ${PROJECT_SOURCE_DIR}/include 
)


file( GLOB SRC_FILES  ./*.cpp )

ADD_LIBRARY(libUsageEnvironment ${SRC_FILES} )

