file(GLOB SOURCES *.c *.cu )

add_executable(cuda_kmeans ${SOURCES})
