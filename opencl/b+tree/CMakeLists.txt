add_executable(ocl_b+tree
    main.c
    kernel/kernel_gpu_opencl_wrapper.c
    kernel/kernel_gpu_opencl_wrapper_2.c
    util/num/num.c
    util/opencl/opencl.c
    util/timer/timer.c
)
target_link_libraries(ocl_b+tree PRIVATE m)
