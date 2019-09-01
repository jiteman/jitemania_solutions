cmake_minimum_required( VERSION 3.7.1 )

project( jitemania_solutions )

if ( NOT DEFINED JMSD_CMAKE_SETTINGS_PATH )
	set( JMSD_CMAKE_SETTINGS_PATH ${CMAKE_SOURCE_DIR}/_jmsd_cmake_settings/cmake )
endif()

if ( NOT DEFINED JMSD_PLATFORM_SOURCES )
	set( JMSD_PLATFORM_SOURCES ${CMAKE_SOURCE_DIR}/_jmsd_platform_support/sources )
endif()

if ( NOT DEFINED JMSD_EXTERNAL_PREBUILT_DEPENDENCIES_PATH )
	set( JMSD_EXTERNAL_PREBUILT_DEPENDENCIES_PATH ${CMAKE_SOURCE_DIR}/../_external_prebuilt_dependencies )
endif()

include( ${JMSD_CMAKE_SETTINGS_PATH}/set-all-settings.cmake )


JMSD_SHOW_PROJECT_GROUP_HEADER()


add_subdirectory( _jmsd_foreign_components )

add_subdirectory( library_subproject_template )
add_subdirectory( executable_template )


JMSD_SHOW_PROJECT_GROUP_FOOTER()
