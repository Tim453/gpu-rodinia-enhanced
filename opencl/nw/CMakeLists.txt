add_executable(ocl_nw
    nw.cpp
)
target_link_libraries(ocl_nw PRIVATE ocl_timing m)
