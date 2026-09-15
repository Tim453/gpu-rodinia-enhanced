# mst input graph

`rmat12.sym.gr` is the default input for `cuda_mst`: an RMAT graph of 4096 nodes
and 59,320 (directed) edges in the Galois binary graph format, version 1.

It is not part of the Rodinia dataset. It comes from the LonestarGPU 2.0 input
collection, which `cuda/mst/main.cu` was written against:

  https://iss.oden.utexas.edu/projects/galois/downloads/lonestargpu2-inputs.tar.bz2
  member `inputs/rmat12.sym.gr`, md5 5efc11a5a29ad310b0daab6398ce468a

The full archive is 1.3 GB, so only this one 496 KB graph is kept here.

Reference result (minimum spanning forest): weight 2560798, 3942 edges,
154 components.
