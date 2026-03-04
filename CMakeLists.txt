cmake_minimum_required(VERSION 3.20.0)
project(Rodinia VERSION 0.1.0 LANGUAGES CUDA CXX C)


set(CXX_STANDARD 17)
set(C_STANDARD 17)
set(CUDA_STANDARD 17)

include_directories(common)

option(SHARED_CUDART "Shared cudart library" ON)
if(SHARED_CUDART)
    set(CMAKE_CUDA_RUNTIME_LIBRARY "Shared")
endif()

find_package(CUDAToolkit REQUIRED)
find_package(OpenMP REQUIRED)


add_subdirectory(cuda)
add_subdirectory(openmp)
