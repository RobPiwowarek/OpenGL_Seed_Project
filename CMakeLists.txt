cmake_minimum_required(VERSION 3.20)
project(myapp-clion)

# Including GLFW
add_subdirectory(glfw)
include_directories(glfw/include)

# Including GLEW
add_subdirectory(glew)
include_directories(glew/include)

# Including GLM
add_subdirectory(glm)
include_directories(glm/glm)

find_package(OpenGL REQUIRED)

add_executable(myapp-clion main.cpp)

target_link_libraries(myapp-clion glfw libglew_static glm)
