# cmake file

set(EXAMPLE_NAME "foo")

add_executable(${EXAMPLE_NAME}
  ${EXAMPLE_NAME}.c)

set_target_properties(${EXAMPLE_NAME} PROPERTIES LINKER_LANGUAGE C)

if(COMMAND loopc14n_pipeline)
  loopc14n_pipeline(DEPENDS ${EXAMPLE_NAME} MAIN_TARGET PLINE_FOO_TRG1)

  message(STATUS "loopc14n pipeline main target: ${PLINE_FOO_TRG1}")
endif()

# installation

