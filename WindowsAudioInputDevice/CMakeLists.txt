
#project name
PROJECT(WindowsAudioInputDevice)


#head file path
INCLUDE_DIRECTORIES(
    ./
    ../UsageEnvironment/include
    ../groupsock/include
    ${PROJECT_SOURCE_DIR}/include 
    ../liveMedia/include
)
#source directory
AUX_SOURCE_DIRECTORY(src DIR_SRCS)

file( GLOB SRC_FILES  ./*.cpp )
#set environment variable

file(GLOB NOMIXER_LIB_FILES ./WindowsAudioInputDevice_common*.cpp ./WindowsAudioInputDevice_noMixer*.cpp)

file(GLOB MIXER_LIB_FILES ./WindowsAudioInputDevice_common*.cpp WindowsAudioInputDevice_mixer*.cpp)

ADD_LIBRARY(libWindowsAudioInputDevice_noMixer ${NOMIXER_LIB_FILES} )

ADD_LIBRARY(libWindowsAudioInputDevice_mixer ${MIXER_LIB_FILES} )

