# Specify the minimum CMAKE version required
cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
cmake_policy(VERSION 3.1)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake")

set(NAME LoupGarouExia)

# Your project's name
project(${NAME})

# Make your header file accessible to the compiler


# Debug flags
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -Wall")
if(CMAKE_COMPILER_IS_GNUCXX)
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -Wextra -Wundef")
endif(CMAKE_COMPILER_IS_GNUCXX)

# Add all files from the source/ folder to CMake
file(GLOB_RECURSE SRC
    "src/*.cpp"
    "src/*.h"
    "src/*.hpp"
)

file(GLOB_RECURSE SRC_BEGIN
    "src/begin/*.cpp"
    "src/begin/*.h"
    "src/begin/*.hpp"
)

# Define the executable
add_executable(${PROJECT_NAME} ${SRC} ${SRC_BEGIN})

source_group("Begin" FILES ${SRC_BEGIN})

# Enable C++ 14
if (NOT UNIX)
	set_target_properties(${PROJECT_NAME} PROPERTIES
	    CXX_STANDARD 14
	    CXX_STANDARD_REQUIRED ON
	    CXX_EXTENSIONS OFF
	)
else()
	add_definitions(-std=c++14)
endif()

