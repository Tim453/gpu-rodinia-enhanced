# The CPU reference path (mummergpu_gold.cpp) is OpenMP-parallel and is always
# compiled in, so this benchmark cannot be built without OpenMP.
if(NOT OpenMP_CXX_FOUND)
    message(STATUS "Skipping cuda/mummergpu: OpenMP not found")
    return()
endif()

add_executable(cuda_mummergpu
	src/mummergpu_main.cpp
	src/mummergpu.cu
	src/mummergpu_gold.cpp
	src/suffix-tree.cpp
	src/PoolMalloc.cpp
)

# mummergpu.cu pulls in common.cu / mummergpu_kernel.cu with angle brackets
target_include_directories(cuda_mummergpu PRIVATE src)

# cuMemGetInfo() comes from the driver API
target_link_libraries(cuda_mummergpu PRIVATE CUDA::cuda_driver OpenMP::OpenMP_CXX)
