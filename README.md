## Rodinia Benchmark Suite 3.1

This is an enhanced version of the Rodinia Benchmark Suite that has been updated to use **CMake** as the build system, replacing the original Makefile-based approach. 

### Build Instructions

1. **Prerequisites**
   - CMake 3.10 or higher
   - CUDA Toolkit (for CUDA benchmarks)
   - OpenMP support (for OpenMP benchmarks)
   - GCC/Clang compiler

2. **Building the Benchmarks**
   ```bash
   mkdir build
   cd build
   cmake ..
   make
   ```

3. **Selecting Build Targets**
   - CUDA benchmarks: Built by default
   - OpenMP benchmarks: Built by default
   - OpenCL benchmarks: Currently a work in progress (TODO)

4. **Running Benchmarks**
   After building, executable binaries will be available in the `build/bin/` directory.

### Note
OpenCL support is currently under development and will be added in a future update.
