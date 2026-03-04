add_executable(omp_mummergpu
    src/mummergpu_main.cpp
    src/mummergpu_gold.cpp
    src/smith-waterman.cpp
    src/suffix-tree.cpp
    src/PoolMalloc.cpp
)

target_link_libraries(omp_mummergpu PRIVATE m)
