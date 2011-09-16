if(GLIB_FOUND AND SNDFILE_FOUND)
  set(CMAKE_C_FLAGS "")  # suppress warnings
  add_executable(r128-test-library tests.c)
  target_link_libraries(r128-test-library ebur128 ${SNDFILE_LIBRARIES})
  add_test(test1 ${EXECUTABLE_OUTPUT_PATH}/r128-test-library)
endif()