SET(sensorstream_SRCS 
    CarmenLog.cpp 
    LogSensorStream.cpp
) 

SET(sensorstream_LIBS
    flirtlib_sensors
)

ADD_LIBRARY(flirtlib_sensorstream SHARED ${sensorstream_SRCS})
TARGET_LINK_LIBRARIES(flirtlib_sensorstream ${sensorstream_LIBS})
INSTALL(TARGETS flirtlib_sensorstream DESTINATION lib/)
INSTALL(DIRECTORY . DESTINATION include/flirtlib/sensorstream
  FILES_MATCHING PATTERN "*.h"
  PATTERN ".svn" EXCLUDE)


