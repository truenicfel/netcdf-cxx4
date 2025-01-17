# This is a CMake file, part of Unidata's netCDF-CXX4 package.

##################################
# Set Project Properties
##################################

#Minimum required CMake Version
cmake_minimum_required(VERSION 3.21.0)

#Project Name
PROJECT(NCXX C CXX)
set(PACKAGE "netcdf-cxx4" CACHE STRING "")

################################
# Set CTest Properties
################################

ENABLE_TESTING()
INCLUDE(CTest)


FIND_PACKAGE(netCDF QUIET)

ADD_SUBDIRECTORY(cxx4)
ADD_SUBDIRECTORY(examples)

