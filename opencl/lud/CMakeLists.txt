add_executable(ocl_lud
    ocl/lud.cpp
    common/common.c
)
target_include_directories(ocl_lud PRIVATE common)
target_link_libraries(ocl_lud PRIVATE ocl_timing m)
