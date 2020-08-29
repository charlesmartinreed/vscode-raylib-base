cmake_minimum_required(VERSION 3.0.0)
project(derp VERSION 0.1.0)

include(CTest)

INCLUDE_DIRECTORIES(
C:/dev/vcpkg/installed/x86-windows/include
)
LINK_DIRECTORIES(
   C:/dev/vcpkg/installed/x86-windows/lib
) 

add_executable(main main.cpp)
TARGET_LINK_LIBRARIES(main
SDL2 raylib
)
enable_testing()

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
