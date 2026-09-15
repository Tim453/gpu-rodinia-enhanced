add_executable(ocl_streamcluster
    streamcluster.cpp
)
target_link_libraries(ocl_streamcluster PRIVATE ocl_timing m)
