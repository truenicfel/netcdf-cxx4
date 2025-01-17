set(CXX_HEADERS
  include/ncAtt.h
  include/ncByte.h
  include/ncChar.h
  include/ncCheck.h
  include/ncCompoundType.h
  include/ncDim.h
  include/ncDouble.h
  include/ncEnumType.h
  include/ncException.h
  include/ncFile.h
  include/ncFill.h
  include/ncFilter.h
  include/ncFloat.h
  include/ncGroup.h
  include/ncGroupAtt.h
  include/ncInt.h
  include/ncInt64.h
  include/ncOpaqueType.h
  include/ncShort.h
  include/ncString.h
  include/ncType.h
  include/ncUbyte.h
  include/ncUint.h
  include/ncUint64.h
  include/ncUshort.h
  include/ncVar.h
  include/ncVarAtt.h
  include/ncVlenType.h
)

set(CXX_SOURCES
  src/ncAtt.cpp
  src/ncByte.cpp
  src/ncChar.cpp
  src/ncCheck.cpp
  src/ncCompoundType.cpp
  src/ncDim.cpp
  src/ncDouble.cpp
  src/ncEnumType.cpp
  src/ncException.cpp
  src/ncFile.cpp
  src/ncFill.cpp
  src/ncFilter.cpp
  src/ncFloat.cpp
  src/ncGroup.cpp
  src/ncGroupAtt.cpp
  src/ncInt.cpp
  src/ncInt64.cpp
  src/ncOpaqueType.cpp
  src/ncShort.cpp
  src/ncString.cpp
  src/ncType.cpp
  src/ncUbyte.cpp
  src/ncUint.cpp
  src/ncUint64.cpp
  src/ncUshort.cpp
  src/ncVar.cpp
  src/ncVarAtt.cpp
  src/ncVlenType.cpp
)

find_package(netCDF QUIET)

add_library(netcdf-cxx4 ${CXX_SOURCES})

target_include_directories(netcdf-cxx4 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_include_directories(netcdf-cxx4 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src)
target_include_directories(netcdf-cxx4 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include/netcdf-cxx)

target_link_libraries(netcdf-cxx4 PUBLIC netCDF::netcdf)

if(NCXX_BUILD_TESTS)
	add_subdirectory(test)
endif(NCXX_BUILD_TESTS)



