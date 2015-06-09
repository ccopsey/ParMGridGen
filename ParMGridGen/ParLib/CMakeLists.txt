find_package(MPI)

if(MPI_C_FOUND)

set(SOURCES
  comm.c
  util.c
  memory.c
  debug.c
  setup.c
  parmgridgen.c
  grsetup.c
  move.c
  ikeysort.c
  ../IMParMetis-2.0/ParMETISLib/fused.c
  ../IMParMetis-2.0/ParMETISLib/comm.c
  ../IMParMetis-2.0/ParMETISLib/util.c
  ../IMParMetis-2.0/ParMETISLib/memory.c
  ../IMParMetis-2.0/ParMETISLib/debug.c
  ../IMParMetis-2.0/ParMETISLib/setup.c
  ../IMParMetis-2.0/ParMETISLib/diffuse.c
  ../IMParMetis-2.0/ParMETISLib/grsetup.c
  ../IMParMetis-2.0/ParMETISLib/timer.c
  ../IMParMetis-2.0/ParMETISLib/coarsen.c
  ../IMParMetis-2.0/ParMETISLib/edge_refine.c
  ../IMParMetis-2.0/ParMETISLib/drivers.c
  ../IMParMetis-2.0/ParMETISLib/remap.c
  ../IMParMetis-2.0/ParMETISLib/iidxsort.c
  ../IMParMetis-2.0/ParMETISLib/ikeysort.c
  ../IMParMetis-2.0/ParMETISLib/var.c
)

set(LIBRARIES
  ${MPI_C_LIBRARIES}
  mgrid
)

add_definitions(${MPI_C_COMPILE_FLAGS})

include_directories(${MPI_C_INCLUDE_PATH})
include_directories(../../MGridGen/IMlib)

add_library(parmgrid ${SOURCES})
target_link_libraries(parmgrid ${LIBRARIES})

install(TARGETS parmgrid DESTINATION lib)

endif()
