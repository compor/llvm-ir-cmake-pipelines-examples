# cmake file

set(FRAGMENT_FILE "main_fragment")

llvmir_pipelines_setup(
  DEPENDS EXAMPLE_NAME
  OUTPUT_FILE ${FRAGMENT_FILE})

set(FRAGMENT_FILES "${FRAGMENT_FILE}")

add_subdirectory(baz)
add_subdirectory(qux)

