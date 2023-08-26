cmake_minimum_required (VERSION 3.27.0)
project(cpp_base VERSION 0.1.0)
# this needs to be straight after project specification
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/out/bin)

find_package(spdlog CONFIG REQUIRED)
add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} spdlog::spdlog)

