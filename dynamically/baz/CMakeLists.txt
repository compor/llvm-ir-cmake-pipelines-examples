# cmake file

set(EXAMPLE_NAME "baz")

add_executable(${EXAMPLE_NAME}
  ${EXAMPLE_NAME}.cpp)

set_target_properties(${EXAMPLE_NAME} PROPERTIES LINKER_LANGUAGE C)


foreach(FRAGMENT ${FRAGMENT_FILES})
  include(${FRAGMENT})
endforeach()

