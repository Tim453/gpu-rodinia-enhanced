add_subdirectory(meschach_lib)

add_executable(ocl_leukocyte
    OpenCL/detect_main.c
    OpenCL/avilib.c
    OpenCL/find_ellipse.c
    OpenCL/find_ellipse_opencl.c
    OpenCL/track_ellipse.c
    OpenCL/track_ellipse_opencl.c
    OpenCL/misc_math.c
    OpenCL/OpenCL_helper_library.c
)
target_link_libraries(ocl_leukocyte PRIVATE ocl_meschach_lib m)
