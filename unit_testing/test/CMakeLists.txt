include_directories ("${PROJECT_SOURCE_DIR}/src")
add_executable(test_state test_state.c)
add_dependencies(test_state test_state)
add_test(test_state test_state)
add_test(test_state_valgrind valgrind
         --error-exitcode=1 --read-var-info=yes
         --leak-check=full --show-leak-kinds=all
         ./test_state)
target_link_libraries(test_state state cmocka)

