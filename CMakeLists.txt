cmake_minimum_required (VERSION 3.10)
#设置c++编译器
set(CMAKE_CXX_COMPILER "g++")
#项目的名称，可以和文件夹名称不同
project(MYSWAP)
#添加头文件的搜索路径
include_directories(${PROJECT_SOURCE_DIR}/header)
#将源文件列表写在变量SrcFiles中
aux_source_directory(./src SrcFiles)
#设置可执行文件输出路径
set(EXECUTABLE_OUTPUT_PATH  ${PROJECT_SOURCE_DIR}/bin)
#设置可执行文件的名称，make之后bin目录下出现my_cmake_swap.exe
add_executable(my_cmake_swap ${SrcFiles})
