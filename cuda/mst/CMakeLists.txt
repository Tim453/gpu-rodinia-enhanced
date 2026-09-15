# main.cu is the hand-written LonestarGPU 2.0 Boruvka MST. Its framework headers
# (Graph, ComponentSpace, KernelConfig, GlobalBarrier, ...) are vendored under
# lonestargpu/ -- see lonestargpu/README.md.
add_executable(cuda_mst main.cu)
target_include_directories(cuda_mst PRIVATE lonestargpu)
