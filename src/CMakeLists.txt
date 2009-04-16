

SET( TARGET ${PROJECT_NAME} )

SET( HEADERS  
	  # your end-user header file, to be installed in <prefix>/include
)

SET( SOURCES 
	  # your source code
)

# build a shared library
ADD_LIBRARY( ${TARGET} SHARED ${SOURCES} )

# give the shared library a version number
SET_TARGET_PROPERTIES( ${TARGET} PROPERTIES
		       VERSION ${VERSION}
)

INSTALL(TARGETS ${TARGET}
		  LIBRARY DESTINATION lib )

INSTALL(FILES ${HEADERS}
        DESTINATION include/${PROJECT_NAME}-${APIVERSION}
)
