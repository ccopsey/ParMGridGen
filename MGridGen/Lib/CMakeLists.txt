set(SOURCES
  coarsen.c
  kwayfm.c
  match.c
  merge.c
  mgridgen.c
  refine.c
  setup.c
  ../IMlib/blas.c
  ../IMlib/dfkeysort.c
  ../IMlib/dkeysort.c
  ../IMlib/file.c
  ../IMlib/ifkeysort.c
  ../IMlib/ifloatsort.c
  ../IMlib/iintsort.c
  ../IMlib/ikeysort.c
  ../IMlib/memory.c
  ../IMlib/sort.c
  ../IMlib/util.c
)

set(LIBRARIES
  m
)

include_directories(../IMlib)

add_library(mgrid ${SOURCES})
target_link_libraries(mgrid ${LIBRARIES})

install(TARGETS mgrid DESTINATION lib)