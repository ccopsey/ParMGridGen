find_package(MPI)

if(MPI_C_FOUND)

set(SOURCES
  io.c
  main.c
  parmgridgen.c
)

set(LIBRARIES
  ${MPI_C_LIBRARIES}
  mpi
  mgrid
  parmgrid
)

include_directories(${MPI_C_INCLUDE_PATH})
include_directories(../../MGridGen/IMlib)
include_directories(../ParLib)

add_executable(parmgridgen ${SOURCES})
target_link_libraries(parmgridgen ${LIBRARIES})

install(TARGETS parmgridgen DESTINATION bin)

endif()
