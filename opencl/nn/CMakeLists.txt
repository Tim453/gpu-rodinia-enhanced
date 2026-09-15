add_executable(ocl_nn
    nearestNeighbor.cpp
    clutils.cpp
    utils.cpp
)
target_link_libraries(ocl_nn PRIVATE ocl_timing OpenMP::OpenMP_CXX)
