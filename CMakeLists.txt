cmake_minimum_required(VERSION 3.15)
project(opengl_start)

set(CMAKE_CXX_STANDARD 20)
set(SOURCE_FILES src/main.cpp)

# add include directories
# include dir for glfw3
include_directories(${PROJECT_SOURCE_DIR}/dependencies/glfw3/include)
# include dir for glew2
include_directories(${PROJECT_SOURCE_DIR}/dependencies/glew2/include)

# add library directories
# lib dir for glfw3
link_directories(${PROJECT_SOURCE_DIR}/dependencies/glfw3/lib-mingw)
# lib dir for glew3
link_directories(${PROJECT_SOURCE_DIR}/dependencies/glew2/lib/Release/Win32)

# main thing
add_executable(opengl_start ${SOURCE_FILES})

# link libs
target_link_libraries(opengl_start glfw3 glew32s gdi32 opengl32 )

add_compile_definitions(GLEW_STATIC)