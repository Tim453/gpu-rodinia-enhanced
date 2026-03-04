file(GLOB SOURCES main.cu  kernel/*.cu util/*/*.c util/*/*.cu)

add_executable(cuda_b+tree ${SOURCES})
