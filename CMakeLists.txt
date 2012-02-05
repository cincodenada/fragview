project (fragview)
cmake_minimum_required (VERSION 2.6)

find_package (PkgConfig)

pkg_check_modules (GTKMM gtkmm-3.0)

link_directories (
	${GTKMM_LIBRARY_DIRS}
)

include_directories (
	${GTKMM_INCLUDE_DIRS}
)

add_executable (fragview
	graph-cxx.cc
	clusters-cxx.cc
)

target_link_libraries (fragview
	${GTKMM_LIBRARIES}
)
