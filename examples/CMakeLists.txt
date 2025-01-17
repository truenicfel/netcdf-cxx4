################################################
# CMakeLists.txt: CMake Configuration file
# for the netcdf-cxx4 `examples` directory.
################################################

add_executable(simple_xy_write simple_xy_wr.cpp)

target_link_libraries(simple_xy_write PUBLIC netcdf-cxx4)
