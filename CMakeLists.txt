cmake_minimum_required(VERSION "3.16.2")


project("HelloWorld")

add_executable("${PROJECT_NAME}" "main.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION bin)
install(FILES "main.cpp" DESTINATION src)

include(CTest)

add_test("Test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")
