add_executable(omp_nn
    nn_openmp.c
)

target_link_libraries(omp_nn PRIVATE m)
