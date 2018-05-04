# cmake file

set(EXAMPLE_NAME "foo")

add_executable(${EXAMPLE_NAME}
  ${EXAMPLE_NAME}.c)

set_target_properties(${EXAMPLE_NAME} PROPERTIES LINKER_LANGUAGE C)

if(COMMAND loopc14n_pipeline)
  loopc14n_pipeline(NAME ${EXAMPLE_NAME} DEPENDS ${EXAMPLE_NAME})
endif()

# installation

