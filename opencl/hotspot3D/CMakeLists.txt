add_executable(ocl_3D
    3D.c
    CL_helper.c
)
target_link_libraries(ocl_3D PRIVATE ocl_timing m)
