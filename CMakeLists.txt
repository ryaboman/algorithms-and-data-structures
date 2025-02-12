cmake_minimum_required(VERSION 3.14)

project(algorithms-and-data-structures LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Core)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Core)

add_executable(algorithms-and-data-structures
  main.cpp
)
target_link_libraries(algorithms-and-data-structures Qt${QT_VERSION_MAJOR}::Core)

include(GNUInstallDirs)
install(TARGETS algorithms-and-data-structures
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
