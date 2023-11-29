cmake_minimum_required(VERSION 3.12)

project(HelloOpenGL VERSION 1.0.0 LANGUAGES C)

# Add source files
file(GLOB_RECURSE SOURCE_FILES "src/*.c")

# Add header files
include_directories(include)

# Add Glad
add_library(glad STATIC "include/glad/glad.c")

# Add GLFW
add_subdirectory(external/glfw)

# Create executable
add_executable(${PROJECT_NAME} ${SOURCE_FILES})

# Link libraries
target_link_libraries(${PROJECT_NAME} PRIVATE glfw glad)

# Copy shaders to build directory
# file(COPY shaders DESTINATION ${CMAKE_BINARY_DIR})

