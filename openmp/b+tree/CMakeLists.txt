add_executable(omp_b+tree 
    main.c
    kernel/kernel_cpu_2.c
    kernel/kernel_cpu.c
    util/num/num.c
    util/timer/timer.c
)

# Link the math library for functions like log() and pow()
target_link_libraries(omp_b+tree PRIVATE m)
