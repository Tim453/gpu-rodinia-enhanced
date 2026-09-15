set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin/opencl)

link_libraries(
    OpenCL::OpenCL
)

# These benchmarks are C++03-era: their CLHelper.h headers use dynamic exception
# specifications (removed in C++17) and some declare globals that collide with
# C++17's std::data. Build the whole tree as C++14.
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Nearly every benchmark compiles ../util/timing.c with -I../util -DTIMING (see
# their Makefiles); expose that as a single target for them to link.
add_library(ocl_timing STATIC util/timing.c)
target_include_directories(ocl_timing PUBLIC util)
target_compile_definitions(ocl_timing PUBLIC TIMING)

add_subdirectory(b+tree)
add_subdirectory(backprop)
add_subdirectory(bfs)
add_subdirectory(cfd)
add_subdirectory(dwt2d)
add_subdirectory(gaussian)
add_subdirectory(heartwall)
add_subdirectory(hotspot)
add_subdirectory(hotspot3D)
add_subdirectory(hybridsort)
add_subdirectory(kmeans)
add_subdirectory(lavaMD)
add_subdirectory(leukocyte)
add_subdirectory(lud)
add_subdirectory(myocyte)
add_subdirectory(nn)
add_subdirectory(nw)
add_subdirectory(particlefilter)
add_subdirectory(pathfinder)
add_subdirectory(srad)
add_subdirectory(streamcluster)
