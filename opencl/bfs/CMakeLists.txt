add_executable(ocl_bfs
    bfs.cpp
    timer.cc
)
target_link_libraries(ocl_bfs PRIVATE ocl_timing OpenMP::OpenMP_CXX)
