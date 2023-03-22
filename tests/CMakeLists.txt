
add_executable(test1 test1.cc)
target_link_libraries(test1 PUBLIC siga)

add_executable(test2 test2.cc)
target_link_libraries(test2 PUBLIC siga)

add_executable(test3 test3.cc)
target_link_libraries(test3 PUBLIC siga)

add_executable(test4 test4.cc)
target_link_libraries(test4 PUBLIC siga)

add_executable(test5 test5.cc)
target_link_libraries(test5 PUBLIC siga)

add_executable(test6 test6.cc)
target_link_libraries(test6 PUBLIC siga)

set_tests_properties(test2 PROPERTIES DEPENDS "test1")
set_tests_properties(test3 PROPERTIES DEPENDS "test2")
set_tests_properties(test4 PROPERTIES DEPENDS "test3")
set_tests_properties(test5 PROPERTIES DEPENDS "test4")
set_tests_properties(test6 PROPERTIES DEPENDS "test5")