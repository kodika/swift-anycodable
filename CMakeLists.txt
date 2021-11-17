add_library(AnyCodable
	Sources/AnyCodable.swift
)

target_link_libraries(AnyCodable
	dispatch
	Foundation
)

set_target_properties(AnyCodable PROPERTIES
  INSTALL_RPATH "$ORIGIN"
  Swift_MODULE_DIRECTORY ${CMAKE_BINARY_DIR}/swift
  INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_BINARY_DIR}/swift
)

_install_target(AnyCodable)
