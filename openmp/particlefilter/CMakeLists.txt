add_executable(omp_particlefilter
    ex_particle_OPENMP_seq.c
)

target_link_libraries(omp_particlefilter PRIVATE m)
