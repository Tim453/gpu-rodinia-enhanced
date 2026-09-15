# bucketsort_kernel.cu, histogram1024_kernel.cu and mergesort_kernel.cu are
# #included by their host files, so they must not be compiled on their own.
add_executable(cuda_hybridsort
    main.cu
    bucketsort.cu
    mergesort.cu
    )
