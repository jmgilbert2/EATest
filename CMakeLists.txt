#-------------------------------------------------------------------------------------------
# Copyright (C) Electronic Arts Inc.  All rights reserved.
#-------------------------------------------------------------------------------------------
cmake_minimum_required(VERSION 3.5)
project(EATest CXX)

#-------------------------------------------------------------------------------------------
# Library definition
#-------------------------------------------------------------------------------------------
file(GLOB EATEST_SOURCES "source/*.cpp")
add_library(EATest ${EATEST_SOURCES})

#-------------------------------------------------------------------------------------------
# Defines
#-------------------------------------------------------------------------------------------
add_definitions(-D_CHAR16T)
add_definitions(-D_CRT_SECURE_NO_WARNINGS)

#-------------------------------------------------------------------------------------------
# Include directories
#-------------------------------------------------------------------------------------------
target_include_directories(EATest PUBLIC include)

#-------------------------------------------------------------------------------------------
# Dependencies
#-------------------------------------------------------------------------------------------
target_link_libraries(EATest EABase)
target_link_libraries(EATest EAStdC)
target_link_libraries(EATest EASTL)
target_link_libraries(EATest EAMain)
target_link_libraries(EATest EAThread)

