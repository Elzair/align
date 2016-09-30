cmake_minimum_required(VERSION 3.3)

project(boost_align)

add_library(boost_align INTERFACE)

target_include_directories(boost_align BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_align DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::align ALIAS boost_align)
