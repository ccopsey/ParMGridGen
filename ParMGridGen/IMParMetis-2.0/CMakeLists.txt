find_package(MPI)

if(MPI_C_FOUND)

set(SOURCES
  ParMETISLib/fused.c
  ParMETISLib/comm.c
  ParMETISLib/util.c
  ParMETISLib/memory.c
  ParMETISLib/debug.c
  ParMETISLib/setup.c
  ParMETISLib/diffuse.c
  ParMETISLib/grsetup.c
  ParMETISLib/timer.c
  ParMETISLib/coarsen.c
  ParMETISLib/edge_refine.c
  ParMETISLib/drivers.c
  ParMETISLib/remap.c
  ParMETISLib/iidxsort.c
  ParMETISLib/ikeysort.c
  ParMETISLib/var.c
)

set(LIBRARIES
  ${MPI_C_LIBRARIES}
)

add_definitions(${MPI_C_COMPILE_FLAGS})

include_directories(${MPI_C_INCLUDE_PATH})

add_library(IMparmetis ${SOURCES})
target_link_libraries(IMparmetis ${LIBRARIES})

install(TARGETS IMparmetis DESTINATION lib)

endif()