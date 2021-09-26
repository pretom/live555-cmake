
#project name
PROJECT(mediaServer)

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
libUsageEnvironment
libBasicUsageEnvironment
libgroupsock
libliveMedia

)
#add executable file
ADD_EXECUTABLE(mediaServer ${SRC_FILES})
#add link library
TARGET_LINK_LIBRARIES(mediaServer ${LIBRARIES})
