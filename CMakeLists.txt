#---------------------------------------------------------------------------------------------------
# CMake Build Configuration for the Ray Tracing Weekend Series
#
# See README.md for guidance.
#---------------------------------------------------------------------------------------------------

cmake_minimum_required ( VERSION 3.1.0 )

project ( RTWeekend
  VERSION 3.0.0
  LANGUAGES CXX
)

# Set to c++11
set ( CMAKE_CXX_STANDARD 11 )

# Source
set ( COMMON_ALL
  src/common/color.h
  src/common/vec3.h
)

set ( SOURCE_ONE_WEEKEND
  ${COMMON_ALL}
  src/InOneWeekend/main.cc
)


# Executables
add_executable(inOneWeekend      ${SOURCE_ONE_WEEKEND})

include_directories(src/common)
