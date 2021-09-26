
#project name
PROJECT(proxyServer)

#head file path
INCLUDE_DIRECTORIES(
    ../BasicUsageEnvironment/include
    ../WindowsAudioInputDevice
    ../UsageEnvironment/include
    ../groupsock/include
    ../liveMedia/include
    ./include
    ./
)


file( GLOB SRC_FILES  ./*.cpp )
#set environment variable

SET(LIBRARIES 
libBasicUsageEnvironment
libgroupsock
libliveMedia
libUsageEnvironment
)
#add executable file
ADD_EXECUTABLE(proxyServer ${SRC_FILES})

#add link library
TARGET_LINK_LIBRARIES(proxyServer ${LIBRARIES})
