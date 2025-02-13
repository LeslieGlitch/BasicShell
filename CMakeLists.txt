# @file CMakeLists.txt
#
# CMake files for BasicShell

cmake_minimum_required(VERSION 3.16)

# Project info
project(BasicShell)

# Main application
add_executable(my_shell myshell.c)

# Run application
add_custom_target(run COMMENT "Run shell"
                      COMMAND ulimit -p
                      COMMAND $<TARGET_FILE:my_shell>
                      DEPENDS my_shell)
