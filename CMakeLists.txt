project(enum-cmake LANGUAGES CXX C)
cmake_minimum_required(VERSION 3.19)
set(CMAKE_CXX_STANDARD 17)

function (enumMain)
    add_library(thirdparty_utils_magic_enum INTERFACE)
    target_include_directories(thirdparty_utils_magic_enum PUBLIC INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/magic_enum/include)
endfunction()

enumMain()
