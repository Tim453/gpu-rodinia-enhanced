add_executable(omp_heartwall
    main.c
    AVI/avilib.c
    AVI/avimod.c
)

target_link_libraries(omp_heartwall PRIVATE m)
