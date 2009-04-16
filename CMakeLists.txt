cmake_minimum_required(VERSION 2.6)

# change this to your project name - sets the variable PROJECT_NAME
PROJECT(autolab-pluginskeleton)

# version numbers
SET( V_MAJOR 0 )
SET( V_MINOR 1 )
SET( V_BUGFIX 0 )

# your release version - you can use this in your code by generating a
# config.h fle (todo)
SET( VERSION ${V_MAJOR}.${V_MINOR}.${V_BUGFIX} )
SET( APIVERSION ${V_MAJOR}.${V_MINOR} )

# generate a config.h file so that the code can obtain compile-time
# info such as the project name and version numbers defined above
CONFIGURE_FILE(${CMAKE_CURRENT_SOURCE_DIR}/config.h.in 
					${CMAKE_CURRENT_SOURCE_DIR}/config.h @ONLY)

ADD_DEFINITIONS(-g -Wall -O2)
ADD_SUBDIRECTORY(src)
