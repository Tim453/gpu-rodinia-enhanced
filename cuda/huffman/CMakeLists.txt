add_executable(cuda_pavle 
    main_test_cu.cu 
    stats_logger.cpp
    vlc_kernel_sm64huff.cu 
    scan.cu 
    pack_kernels.cu 
    cpuencode.cpp)

