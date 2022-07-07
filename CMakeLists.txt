cmake_minimum_required(VERSION 3.13)
project (metro)

find_package(pybind11 REQUIRED)


file (GLOB HEADER_FILES "include/*.h")

set(SOURCES
        src/metro.cpp
	    include/wrap/ply/plylib.cpp)

pybind11_add_module(metro
	${SOURCES}
	${HEADER_FILES})

target_include_directories(metro PUBLIC include/)
target_link_libraries(metro PUBLIC )


install(TARGETS metro
  COMPONENT python
  LIBRARY DESTINATION "${CMAKE_CURRENT_SOURCE_DIR}/lib/"
  )
