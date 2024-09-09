set(TEST_NAME "simple_failing_test")

add_executable(${TEST_NAME} simple_failing_test.cpp)

set_target_properties(${TEST_NAME} PROPERTIES CXX_STANDARD 17 CXX_STANDARD_REQUIRED ON)

# Add project include directory
target_include_directories(${TEST_NAME}
  PRIVATE
  ${PROJECT_SOURCE_DIR}/src)

add_test(NAME ${TEST_NAME} COMMAND ${TEST_NAME})
