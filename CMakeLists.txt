cmake_minimum_required(VERSION 2.6)

# change this to your project name - sets the variable PROJECT_NAME
PROJECT(autolab-libskeleton)

# version numbers
SET( V_MAJOR 0 )
SET( V_MINOR 1 )
SET( V_BUGFIX 0 )

# your release version
SET( VERSION ${V_MAJOR}.${V_MINOR}.${V_BUGFIX} )

# your API version - the library will be named using this value
SET( APIVERSION ${V_MAJOR}.${V_MINOR} )

ADD_DEFINITIONS(-g -Wall -O2)
ADD_SUBDIRECTORY(src)

# Create and install the pkgconfig file from the .in template
# you must rename and edit the file autolab-skeleton.pc.in for your project
SET( PKGFILE ${CMAKE_CURRENT_SOURCE_DIR}/${PROJECT_NAME}.pc )
CONFIGURE_FILE( ${PKGFILE}.in ${PKGFILE} @ONLY)
INSTALL( FILES ${PKGFILE} DESTINATION lib/pkgconfig/)
