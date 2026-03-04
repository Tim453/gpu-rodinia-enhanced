add_executable(omp_streamcluster
    streamcluster_omp.cpp
)

target_link_libraries(omp_streamcluster PRIVATE m)
