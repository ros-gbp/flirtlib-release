SET(sensors_SRCS 
    AbstractReading.cpp 
    LaserReading.cpp
) 

ADD_LIBRARY(flirtlib_sensors SHARED ${sensors_SRCS})
TARGET_LINK_LIBRARIES(flirtlib_sensors flirtlib_geometry)
INSTALL(TARGETS flirtlib_sensors DESTINATION lib/)
INSTALL(DIRECTORY . DESTINATION include/flirtlib/sensors
  FILES_MATCHING PATTERN "*.h"
  PATTERN ".svn" EXCLUDE)