add_executable(ocl_particlefilter_naive  ex_particle_OCL_naive_seq.cpp)
add_executable(ocl_particlefilter_double ex_particle_OCL_double_seq.cpp)
add_executable(ocl_particlefilter_single ex_particle_OCL_single_seq.cpp)

foreach(target ocl_particlefilter_naive ocl_particlefilter_double ocl_particlefilter_single)
    target_link_libraries(${target} PRIVATE ocl_timing m)
endforeach()
