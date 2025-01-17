cmake_minimum_required(VERSION 3.21.0)

# Project Name
project(netcdf-cxx CXX)

# Options
option(NCXX_BUILD_TESTS "Build tests?" ON)
option(NCXX_BUILD_EXAMPLES "Build examples?" ON)

# Tests
if(NCXX_BUILD_TESTS)
	include(CTest)
endif(NCXX_BUILD_TESTS)

# Examples
if(NCXX_BUILD_EXAMPLES)
	add_subdirectory(examples)
endif(NCXX_BUILD_EXAMPLES)

# netcdf-cxx library
add_subdirectory(cxx4)


