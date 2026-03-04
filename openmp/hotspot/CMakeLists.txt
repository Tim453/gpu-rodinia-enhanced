add_executable(omp_hotspot
    hotspot_openmp.cpp
)

target_link_libraries(omp_hotspot PRIVATE m)
