
#project name
PROJECT(WindowsAudioInputDevice)


#head file path
INCLUDE_DIRECTORIES(
    ../BasicUsageEnvironment/include
    ../WindowsAudioInputDevice
    ../UsageEnvironment/include
    ../groupsock/include
    ./include
)



file(GLOB SRC_FILES ./*.cpp ./*.c)

ADD_LIBRARY(libliveMedia ${SRC_FILES} )

TARGET_LINK_LIBRARIES(libliveMedia libgroupsock)

