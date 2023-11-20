cmake_minimum_required(VERSION 3.0.0)
project(msi2lmp_c VERSION 3.9.10 LANGUAGES C)

include(CTest)
enable_testing()

aux_source_directory(src/ DIR_SRCS)
add_executable(msi2lmp ${DIR_SRCS})
target_link_libraries(msi2lmp m)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
