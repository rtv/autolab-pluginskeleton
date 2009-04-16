

# create a plugin called <PROJECT_NAME>.so
SET( TARGET ${PROJECT_NAME} )

SET( SOURCES 
	  # your source code files
)

# build a runtime loadable shared library (.so / .dll )
ADD_LIBRARY( ${TARGET} MODULE ${SOURCES} )

# delete the "lib" prefix from the plugin library
SET_TARGET_PROPERTIES( ${TARGET} PROPERTIES PREFIX "" )

# install in <CMAKE_INSTALL_PREFIX>/lib
INSTALL(TARGETS ${TARGET} DESTINATION lib )


