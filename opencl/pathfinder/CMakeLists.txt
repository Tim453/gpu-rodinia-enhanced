add_executable(ocl_pathfinder
    main.cpp
    OpenCL.cpp
)
target_link_libraries(ocl_pathfinder PRIVATE ocl_timing m)
