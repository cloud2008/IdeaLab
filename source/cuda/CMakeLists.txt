cmake_minimum_required(VERSION 3.22)
project(efficient_cuda LANGUAGES CXX)

enable_language(CUDA)

file(GLOB SOURCE ${CMAKE_SOURCE_DIR}/gemm/matrixMul/*.cu)

include_directories(
	${CMAKE_SOURCE_DIR}
	${CMAKE_SOURCE_DIR}/common
)

add_executable(test_gemm ${SOURCE})