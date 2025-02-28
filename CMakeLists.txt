# @file CMakeLists.txt
#
# CMake files for BasicShell

cmake_minimum_required(VERSION 3.16)

# Project info
project(BasicShell)

# Main application
add_executable(my_shell myshell.c)

# Run application
add_custom_target(run COMMENT "Run shell\n[WARNING: TERMINAL SHOULD PRINT \"500\" BELOW. RUN \"ulimit -u 500\" IF IT SAYS \"ulimited\"!]"
                      COMMAND bash -c "ulimit -u" && $<TARGET_FILE:my_shell>
                      DEPENDS my_shell)
