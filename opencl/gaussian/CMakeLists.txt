add_executable(ocl_gaussian
    gaussianElim.cpp
    clutils.cpp
    utils.cpp
)
target_link_libraries(ocl_gaussian PRIVATE ocl_timing OpenMP::OpenMP_CXX)
