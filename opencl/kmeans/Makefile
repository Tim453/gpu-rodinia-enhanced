include ../../common/make.config

#Can be changed by `make TYPE=CPU`
TYPE = GPU

#Library
ifeq ($(TYPE),GPU)
	OPENCL_INC = $(NV_OPENCL_INC)
	OPENCL_LIB = $(NV_OPENCL_LIB)
else
	OPENCL_INC = $(INTEL_OPENCL_INC)
	OPENCL_LIB = $(INTEL_OPENCL_LIB)
endif

# C compiler
CC = g++
CC_FLAGS = -g -O2 

kmeans: cluster.o getopt.o read_input.o kmeans_clustering.o rmse.o
	$(CC) $(KERNEL_DIM) $(CC_FLAGS) \
		kmeans.cpp ../util/timing.c cluster.o getopt.o read_input.o kmeans_clustering.o rmse.o -o kmeans.out \
        -I$(OPENCL_INC) -L$(OPENCL_LIB) -lOpenCL \
        -I../util -DTIMING

%.o: %.cpp
	$(CC) $(CC_FLAGS) $< -c

cluster.o: cluster.cpp 
	$(CC) $(CC_FLAGS) cluster.cpp -c

getopt.o: getopt.cpp 
	$(CC) $(CC_FLAGS) getopt.cpp -c

read_input.o: read_input.cpp
	$(CC) $(CC_FLAGS) read_input.cpp -c

rmse.o: rmse.cpp
	$(CC) $(CC_FLAGS) rmse.cpp -c

clean:
	rm -f *.o *~ kmeans.out *.linkinfo
