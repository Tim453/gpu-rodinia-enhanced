add_executable(ocl_hybridsort
    hybridsort.c
    bucketsort.c
    mergesort.c
)
set_target_properties(ocl_hybridsort PROPERTIES C_STANDARD 99)
target_compile_options(ocl_hybridsort PRIVATE -fcommon)
target_link_libraries(ocl_hybridsort PRIVATE ocl_timing m)
