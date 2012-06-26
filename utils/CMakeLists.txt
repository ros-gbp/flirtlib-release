SET(utils_SRCS
    Regression.cpp
    SimplePeakFinder.cpp
    SimpleMinMaxPeakFinder.cpp
    PoseEstimation.cpp
)

ADD_LIBRARY(flirtlib_utils SHARED ${utils_SRCS})
INSTALL(TARGETS flirtlib_utils DESTINATION lib/)
INSTALL(DIRECTORY . DESTINATION include/flirtlib/utils
  FILES_MATCHING PATTERN "*.h"
  PATTERN ".svn" EXCLUDE)
