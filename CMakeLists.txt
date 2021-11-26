cmake_minimum_required(VERSION 2.8) 
PROJECT (GraphCuts)
find_package(OpenCV REQUIRED )
set(NAME_SRC
    main.cpp
    max_flow/block.h
    max_flow/graph.h
    max_flow/graph.cpp
    max_flow/maxflow.cpp
    )

INCLUDE_DIRECTORIES( ${OpenCV_INCLUDE_DIRS})
add_executable( GraphCuts ${NAME_SRC} ${NAME_HEADERS} )
target_link_libraries(GraphCuts ${OpenCV_LIBS} )