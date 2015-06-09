cmake_minimum_required(VERSION 2.8)

project(ParMGridGen)

add_subdirectory(MGridGen/IMlib)
add_subdirectory(MGridGen/Lib)
add_subdirectory(MGridGen/Programs)

add_subdirectory(ParMGridGen/IMParMetis-2.0)
add_subdirectory(ParMGridGen/ParLib)
add_subdirectory(ParMGridGen/Programs)
