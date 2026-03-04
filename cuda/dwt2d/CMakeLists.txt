

add_executable(cuda_dwt2d 
    main.cu 
    dwt.cu 
    components.cu 
    dwt_cuda/fdwt53.cu
    dwt_cuda/fdwt97.cu
    dwt_cuda/common.cu
    dwt_cuda/rdwt97.cu
    dwt_cuda/rdwt53.cu)