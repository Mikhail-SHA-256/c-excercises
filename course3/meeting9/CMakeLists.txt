set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=c++14")

find_package(Boost REQUIRED)

include_directories(${Boost_INCLUDE_DIRS})

add_executable(bench
	benchmark.cc
)

target_link_libraries(bench
	benchmark
	pthread
)

add_executable(meeting9
	meeting9.cc
)

