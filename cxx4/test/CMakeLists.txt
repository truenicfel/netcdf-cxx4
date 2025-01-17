macro(ncxx_add_test TEST_NAME SOURCE_FILE)
	add_executable(${TEST_NAME} ${SOURCE_FILE})
	target_link_libraries(${TEST_NAME} PRIVATE netcdf-cxx4)
	target_include_directories(${TEST_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
	add_test(NAME ${TEST_NAME} COMMAND ${TEST_NAME})
	message(STATUS "Added test ${TEST_NAME}!")
endmacro(ncxx_add_test)

ncxx_add_test(ncxx_test_att test_att.cpp)
ncxx_add_test(ncxx_test_classic test_classic.cpp)
ncxx_add_test(ncxx_test_dim test_dim.cpp)
ncxx_add_test(ncxx_test_filter test_filter.cpp)
ncxx_add_test(ncxx_test_group test_group.cpp)
ncxx_add_test(ncxx_test_ncFile_Flags test_ncFile_Flags.cpp)
ncxx_add_test(ncxx_test_open_close test_open_close.cpp)
ncxx_add_test(ncxx_test_type test_type.cpp)
ncxx_add_test(ncxx_test_type2 test_type2.cpp)
ncxx_add_test(ncxx_test_type3 test_type3.cpp)
ncxx_add_test(ncxx_test_type4 test_type4.cpp)
ncxx_add_test(ncxx_test_type5 test_type5.cpp)
ncxx_add_test(ncxx_test_var test_var.cpp)
ncxx_add_test(ncxx_test_var2 test_var2.cpp)
ncxx_add_test(ncxx_test_2 test2.cpp)





