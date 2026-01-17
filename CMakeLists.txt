cmake_minimum_required(VERSION 4.2)
project(cpp_startup)

add_subdirectory(engine)

set(INSTALL_DIR ${CMAKE_CURRENT_SOURCE_DIR}/bin)
install(TARGETS cpp_startup_engine DESTINATION ${INSTALL_DIR})