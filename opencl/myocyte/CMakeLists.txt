# kernel/{solver,embedded_fehlberg_7_8,master,kernel_fin}.c are #included by
# kernel_gpu_opencl_wrapper.c, so they must not be compiled on their own.
add_executable(ocl_myocyte
    main.c
    kernel/kernel_gpu_opencl_wrapper.c
    util/file/file.c
    util/num/num.c
    util/opencl/opencl.c
    util/timer/timer.c
)
target_link_libraries(ocl_myocyte PRIVATE ocl_timing m)
