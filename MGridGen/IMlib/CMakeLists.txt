set(SOURCES
  blas.c
  dfkeysort.c
  dkeysort.c
  file.c
  ifkeysort.c
  ifloatsort.c
  iintsort.c
  ikeysort.c
  memory.c
  sort.c
  util.c
)

add_library(IMlib ${SOURCES})

install(TARGETS IMlib DESTINATION lib)