add_executable(ocl_euler3d
    euler3d.cpp
)
target_link_libraries(ocl_euler3d PRIVATE ocl_timing)
