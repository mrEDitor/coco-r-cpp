cmake_minimum_required(VERSION 3.0)
project(coco-r-cpp VERSION 1.0.1)

set(COCO_BIN "cococpp")
file(GLOB SOURCES "*.cpp")
file(GLOB FRAMES "*.frame")

add_executable("${COCO_BIN}" ${SOURCES})
foreach(F ${FRAMES})
	configure_file("${F}" "." COPYONLY)
endforeach()
install(TARGETS "${COCO_BIN}" DESTINATION "bin")
install(FILES ${FRAMES} DESTINATION "share/coco-cpp")
