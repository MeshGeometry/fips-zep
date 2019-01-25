#
# project: zep
#

cmake_minimum_required(VERSION 3.0)
set_property(GLOBAL PROPERTY USE_FOLDERS ON)
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

if (FIPS_IMPORT)
        add_definitions(-DZEP_SINGLE_HEADER_BUILD)
        include_directories(zep/src)
endif()