project( json )

set( HEADERS
    "include/nlohmann/json.hpp"
)

set( SOURCES
    ""
)

add_library( ${PROJECT_NAME} INTERFACE
    ${HEADERS}
    ${SOURCES}
)

target_include_directories( ${PROJECT_NAME}
    INTERFACE
        ${SOURCE_DIR}/external/json/include
)

install( TARGETS ${PROJECT_NAME}
    ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)

# The trailing slash is important
install( DIRECTORY ${CMAKE_INSTALL_INCLUDEDIR}/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
)
