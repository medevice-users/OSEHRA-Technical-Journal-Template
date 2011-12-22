cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(OSEHRA-Technical-Journal-Template)

set( CMAKE_RUNTIME_OUTPUT_DIRECTORY
  ${OSEHRA-Technical-Journal-Template}/bin
)

file(GLOB_RECURSE MUMPS_FILES "Source/*.RO")

add_subdirectory(Source)

option(BUILD_REPORT "Build the PDF Report." OFF)

if(BUILD_REPORT)
  add_subdirectory(ReportTemplate)
endif()
