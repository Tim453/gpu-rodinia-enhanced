add_executable(cuda_lud_cuda 
	cuda/lud_kernel.cu
	cuda/lud.cu
	common/common.c
)
target_include_directories(cuda_lud_cuda PRIVATE common)