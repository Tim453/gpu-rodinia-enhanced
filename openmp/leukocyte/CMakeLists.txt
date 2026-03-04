
add_subdirectory(meschach_lib)

add_executable(omp_leukocyte
    OpenMP/detect_main.c
    OpenMP/avilib.c
    OpenMP/find_ellipse.c
    OpenMP/track_ellipse.c
    OpenMP/misc_math.c
)

target_link_libraries(omp_leukocyte PRIVATE m pthread omp_meschach_lib)
