add_executable(omp_lud
    omp/lud.c
    omp/lud_omp.c
    common/common.c
)

target_link_libraries(omp_lud PRIVATE m)
