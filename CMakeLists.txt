cmake_minimum_required(VERSION 3.13)
project(macdeploycheck)
find_package(Qt6 6.4 COMPONENTS Core REQUIRED)
add_executable(macdeploycheck macdeploycheck.cpp)
target_link_libraries(macdeploycheck PUBLIC "-framework AppKit" Qt${QT_VERSION_MAJOR}::Core)
install(TARGETS macdeploycheck RUNTIME DESTINATION bin)
