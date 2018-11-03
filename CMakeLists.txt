cmake_minimum_required(VERSION 3.0)
project(coco-r-cpp VERSION 1.0)

set(COCO_BIN "cococpp")
file(GLOB SOURCES "*.cpp")
file(GLOB FRAMES "*.frame")

add_executable("${COCO_BIN}" ${SOURCES})
install(TARGETS "${COCO_BIN}" DESTINATION "bin")
install(FILES ${FRAMES} DESTINATION "share/coco-cpp")
