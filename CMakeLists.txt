cmake_minimum_required(VERSION 3.24)
project(BeeAlloc)

set(CMAKE_CXX_STANDARD 17)

add_library(BeeAlloc STATIC src/GeneralPurposeAllocator.cpp src/MallocAndFree.cpp  src/MallocAndFree.h include/GeneralPurposeAllocator.h include/AllocatorBlockHeader.h)

target_include_directories(BeeAlloc
        PUBLIC include
        PUBLIC src
        )
target_link_directories(BeeAlloc
        PRIVATE src
        PRIVATE include
        )