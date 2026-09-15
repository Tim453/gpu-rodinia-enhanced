add_executable(ocl_kmeans
    kmeans.cpp
    cluster.cpp
    getopt.cpp
    read_input.cpp
    kmeans_clustering.cpp
    rmse.cpp
)
target_link_libraries(ocl_kmeans PRIVATE ocl_timing m)
