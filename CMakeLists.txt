cmake_minimum_required(VERSION 3.20.0)
project(Rodinia VERSION 0.1.0 LANGUAGES CUDA CXX C)


set(CXX_STANDARD 17)
set(C_STANDARD 17)
set(CUDA_STANDARD 17)

include_directories(common)

option(SHARED_CUDART "Shared cudart library" ON)

find_package(CUDAToolkit)
find_package(OpenMP)
find_package(OpenCL)

if(CUDAToolkit_FOUND)
    add_subdirectory(cuda)
endif()

if(OpenMP_FOUND)
    add_subdirectory(openmp)
endif()

if(OpenCL_FOUND)
    add_subdirectory(opencl)
endif()


set(FETCHCONTENT_QUIET OFF)
include(FetchContent)

FetchContent_Declare(
    rodinia_data
    URL https://www.dropbox.com/s/cc6cozpboht3mtu/rodinia-3.1-data.tar.gz
    SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/data
    URL_HASH SHA256=B90994D5208EC5A0A133DFB9AB7928A1E8A16741503A91D212884B9E4FCE8CD8
)

FetchContent_MakeAvailable(rodinia_data)