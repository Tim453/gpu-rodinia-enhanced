add_executable(omp_kmeans_omenmp
    kmeans_openmp/kmeans.c
    kmeans_openmp/cluster.c
    kmeans_openmp/getopt.c
    kmeans_openmp/kmeans_clustering.c
)

target_link_libraries(omp_kmeans_omenmp PRIVATE m)


add_executable(omp_kmeans_serial
    kmeans_serial/kmeans.c
    kmeans_serial/cluster.c
    kmeans_serial/getopt.c
    kmeans_serial/kmeans_clustering.c
)

target_link_libraries(omp_kmeans_serial PRIVATE m)
