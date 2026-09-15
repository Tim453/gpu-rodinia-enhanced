# kernel/*_kernel.c hold OpenCL kernel text, not host code; only the wrapper is
# compiled (see the upstream Makefile's object list).
add_executable(ocl_srad
    main.c
    kernel/kernel_gpu_opencl_wrapper.c
    util/graphics/graphics.c
    util/graphics/resize.c
    util/opencl/opencl.c
    util/timer/timer.c
)
target_link_libraries(ocl_srad PRIVATE ocl_timing m)
