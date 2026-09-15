# main.cpp is self-contained: it defines its own cl_mem-based rgbToComponents(),
# nStage2dDWT(), writeLinear() and writeNStage2DDWT(). components.cpp and
# dwt.cpp are unported leftovers from the CUDA version (dwt.cpp still calls into
# a dwt_cuda:: namespace that does not exist here), which is why the upstream
# Makefile builds main.cpp alone.
add_executable(ocl_dwt2d
    main.cpp
)
target_compile_definitions(ocl_dwt2d PRIVATE OUTPUT)
target_link_libraries(ocl_dwt2d PRIVATE ocl_timing m)
