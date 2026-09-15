add_executable(ocl_lavaMD
    main.c
    kernel/kernel_gpu_opencl_wrapper.c
    util/num/num.c
    util/opencl/opencl.c
    util/timer/timer.c
)
target_link_libraries(ocl_lavaMD PRIVATE ocl_timing m)
