SET(geometry_SRCS 
    point.cpp 
) 

ADD_LIBRARY(flirtlib_geometry SHARED ${geometry_SRCS})
INSTALL(TARGETS flirtlib_geometry DESTINATION lib/)
INSTALL(DIRECTORY . DESTINATION include/flirtlib/geometry
  FILES_MATCHING PATTERN "*.h"
  PATTERN ".svn" EXCLUDE)
