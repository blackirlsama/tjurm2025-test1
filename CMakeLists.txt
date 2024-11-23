cmake_minimum_required(VERSION 3.0)
project(tjurm2025-test4)

# 设置C++标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# 查找OpenCV包
find_package(OpenCV REQUIRED)

# 添加可执行文件
add_executable(tjurm2025-test4  src/main.cpp src/ArmorPlate.cpp)

# 包含OpenCV头文件目录
target_include_directories(tjurm2025-test4 PRIVATE ${OpenCV_INCLUDE_DIRS})

# 链接OpenCV库
target_link_libraries(tjurm2025-test4 ${OpenCV_LIBS})

include_directories(${CMAKE_SOURCE_DIR}/include)
