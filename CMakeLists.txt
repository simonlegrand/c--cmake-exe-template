cmake_minimum_required(VERSION 3.15)

project(template) # PROJECT_NAME is set with project argument.
set(CMAKE_CXX_STANDARD 17)

add_executable(${PROJECT_NAME})
# Add here source files of your target.
target_sources(
  ${PROJECT_NAME}
  PRIVATE src/main.cpp
)

enable_testing()
add_subdirectory(tests)

include(GNUInstallDirs)
install(TARGETS ${PROJECT_NAME}
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}/$<CONFIG>)

message(STATUS "${PROJECT_NAME} configured.")
