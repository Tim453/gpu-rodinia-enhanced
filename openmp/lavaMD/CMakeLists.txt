add_executable(omp_lavaMD
    main.c
    kernel/kernel_cpu.c
    util/num/num.c
    util/timer/timer.c
)

target_link_libraries(omp_lavaMD PRIVATE m)
