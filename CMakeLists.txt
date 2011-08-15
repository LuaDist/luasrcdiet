# Copyright (C) 2007-2010 LuaDist.
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luasrcdiet NONE )
cmake_minimum_required ( VERSION 2.6 )
include ( dist.cmake )


set ( LUA_FILES llex.lua lparser.lua optlex.lua optparser.lua )
install ( FILES ${LUA_FILES} DESTINATION ${INSTALL_LMOD} )
install ( DIRECTORY plugin DESTINATION ${INSTALL_LMOD} )

install_lua_executable(LuaSrcDiet LuaSrcDiet.lua) 

install_data ( README technotes.txt COPYRIGHT Changelog)
install_example( sample/ )
install_test( test/ )
