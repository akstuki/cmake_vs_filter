cmake_minimum_required(VERSION 2.8.9)
project(TEST)

set(SOURCES
main/main.h
main/main.cpp
)
set(MATHSRC
math/kalman.h
math/kalman.cpp
)
set(MATSRC
math/matrix/quat.h
math/matrix/quat.cpp
)
set(UAVSRC
uav/control.h
uav/control.cpp
)
source_group(main FILES ${SOURCES})
source_group(math FILES ${MATHSRC})
source_group(math\\matrix FILES ${MATSRC})
source_group(uav FILES ${UAVSRC})

add_executable(MAIN ${SOURCES} ${MATHSRC} ${MATSRC} ${UAVSRC})


