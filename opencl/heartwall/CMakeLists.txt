add_executable(ocl_heartwall
    main.c
    kernel/kernel_gpu_opencl_wrapper.c
    util/avi/avilib.c
    util/avi/avimod.c
    util/file/file.c
    util/opencl/opencl.c
    util/timer/timer.c
)
target_link_libraries(ocl_heartwall PRIVATE ocl_timing m)
