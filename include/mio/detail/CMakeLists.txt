#
# iff mio is the highest level project, include the implementation
# detail files in the source listing for CMake-generated IDE projects
#
if(NOT subproject)
  target_sources(mio INTERFACE
    $<BUILD_INTERFACE:
      ${CMAKE_CURRENT_LIST_DIR}/basic_mmap.hpp
      ${CMAKE_CURRENT_LIST_DIR}/basic_mmap.ipp
      ${CMAKE_CURRENT_LIST_DIR}/string_util.hpp>)
endif()
