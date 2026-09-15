add_executable(ocl_hotspot
    hotspot.c
    OpenCL_helper_library.c
)
target_link_libraries(ocl_hotspot PRIVATE ocl_timing m)
