cmake_minimum_required(VERSION 3.5)
project(01_moveObj VERSION 1.0 LANGUAGES CXX)
add_executable(moveObj
	main.cpp
	SecondFunk/SecondaryFunction.h SecondFunk/SecondaryFunction.cpp)



# if (Visual Studio)
# настраиваю в качестве запускаемого проекта
# настройка на стандарт с++17
if(MSVC)
set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT moveObj)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /std:c++17")
else()
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")
endif()




### add_subdirectory(../Catch2 Catch2-build)
#find_package(Catch2 3 REQUIRED)
## 		These tests need their own main
#add_executable(test test.cpp Table.hpp)
#target_link_libraries(test PRIVATE Catch2::Catch2)
