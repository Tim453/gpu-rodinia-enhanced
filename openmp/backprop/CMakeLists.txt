add_executable(omp_backprop
    backprop_kernel.c
    backprop.c
    facetrain.c
    imagenet.c
)

# Link the math library for functions like log() and pow()
target_link_libraries(omp_backprop PRIVATE m)
