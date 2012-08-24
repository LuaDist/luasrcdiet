# Copyright (C) 2007-2012 LuaDist.
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luasrcdiet NONE )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

install_lua_module ( llex llex.lua )
install_lua_module ( lparser lparser.lua )
install_lua_module ( optlex optlex.lua )
install_lua_module ( optparser optparser.lua )
install_lua_module ( plugin.example plugin/example.lua )
install_lua_module ( plugin.sloc plugin/sloc.lua )
install_lua_module ( plugin.html plugin/html.lua )
install_lua_executable ( luasrcdiet LuaSrcDiet.lua )
install_data ( README technotes.txt COPYRIGHT Changelog )
install_example ( sample/ )
install_test ( test/ )
