add_executable(cuda_lavaMD 
	main.c
	kernel/kernel_gpu_cuda_wrapper.cu
	util/num/num.c
	util/timer/timer.c
	util/device/device.cu
)
