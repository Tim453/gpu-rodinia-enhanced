
file(GLOB SOURCES src/*.c src/*.cu)

add_executable(cuda_leukocyte ${SOURCES})
target_link_directories(cuda_leukocyte PRIVATE lib)
target_link_libraries(cuda_leukocyte PRIVATE meschach)

target_include_directories(cuda_leukocyte PRIVATE include)

