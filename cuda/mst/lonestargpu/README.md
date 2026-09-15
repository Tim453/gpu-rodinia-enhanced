# Vendored LonestarGPU headers

`cuda/mst/main.cu` is the hand-written Boruvka minimum-spanning-tree benchmark
from LonestarGPU, and needs that project's framework headers. They are not part
of Rodinia, so they are vendored here.

Upstream: https://github.com/IntelligentSoftwareSystems/GaloisGPU
Commit:   31302b68c9a3fe619339c3e9ef61b694f7128955 (2019-11-11), `include/`
License:  3-Clause BSD, see LICENSE.txt

Files: `common.h`, `component.h`, `cuda_launch_config.hpp`, `gbar.cuh`,
`graph.h`, `kernelconfig.h`, `list.h`, `lonestargpu.h`.

They have been modified to build against CUDA 12/13; every change is marked
with a `RODINIA:` comment.
