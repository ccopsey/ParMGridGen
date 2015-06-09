set(SOURCES
  io.c
  mgridgen.c
)

set(LIBRARIES
  mgrid
)

include_directories(../IMlib)
include_directories(../Lib)

add_executable(mgridgen ${SOURCES})
target_link_libraries(mgridgen ${LIBRARIES})

install(TARGETS mgridgen DESTINATION bin)
