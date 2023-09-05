cmake_minimum_required (VERSION 3.27.0)
project(cpp_base VERSION 0.1.0)
# this needs to be straight after project specification
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/out/bin)

find_package(spdlog CONFIG REQUIRED)
find_package(glm CONFIG REQUIRED)
find_package(glfw3 CONFIG REQUIRED)

add_subdirectory(external/glad)

file(GLOB_RECURSE SRC_FILES "src/*.cpp")
add_executable(${PROJECT_NAME} src/main.cpp ${SRC_FILES})
target_link_libraries(${PROJECT_NAME} spdlog::spdlog glm::glm glfw glad)

