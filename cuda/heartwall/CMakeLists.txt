file(GLOB SOURCES *.c *.cu AVI/*.c)

add_executable(cuda_heartwall ${SOURCES})

target_include_directories(cuda_heartwall PRIVATE AVI/)
