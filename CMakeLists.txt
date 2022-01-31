cmake_minimum_required(VERSION 3.0.0)
project(CPPCraft VERSION 0.1.0)

add_executable(CPPCraft main.cpp)

###################
# GLFW
###################
set(GLFW_BUILD_EXAMPLES "")
set(GLFW_BUILD_TESTS "")
set(GLFW_BUILD_DOCS "")
add_subdirectory(libs/GLFW)

target_link_libraries(${PROJECT_NAME} glfw)

###################
# GLAD
###################
add_subdirectory(libs/glad)
target_link_libraries(${PROJECT_NAME} glad)

###################
# GLM
###################
add_subdirectory(libs/glm)
target_link_libraries(${PROJECT_NAME} glm)