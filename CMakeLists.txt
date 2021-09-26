
PROJECT(live555)

ADD_SUBDIRECTORY(
    ./groupsock
)

ADD_SUBDIRECTORY(
    ./BasicUsageEnvironment
)



ADD_SUBDIRECTORY(
    ./UsageEnvironment
)

IF(WIN32)
ADD_SUBDIRECTORY(
    ./WindowsAudioInputDevice
)
ENDIF()

ADD_SUBDIRECTORY(
    ./liveMedia
)


ADD_SUBDIRECTORY(
    ./mediaServer
)

ADD_SUBDIRECTORY(
    ./proxyServer
)

