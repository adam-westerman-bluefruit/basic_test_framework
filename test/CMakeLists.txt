cmake_minimum_required(VERSION 3.20)

set(This MyTests)

set(TestSources Tests.cpp)

add_executable(${This} ${TestSources} ${Sources} ${Headers})

target_link_libraries(${This} PUBLIC gtest_main)

add_test(
  NAME ${This}
  COMMAND ${This}
)