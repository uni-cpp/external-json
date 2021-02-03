project( json )

set( HEADERS
    "include/nlohmann/json.hpp"
)

set( SOURCES
    ""
)

add_library( ${PROJECT_NAME} INTERFACE
)

target_sources( ${PROJECT_NAME} INTERFACE
    "${SOURCE_DIR}/external/json/include/nlohmann/json.hpp"
)

target_include_directories( ${PROJECT_NAME}
    INTERFACE
        ${SOURCE_DIR}/external/json/include
)

# The trailing slash is important
install( DIRECTORY ${CMAKE_INSTALL_INCLUDEDIR}/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
)
