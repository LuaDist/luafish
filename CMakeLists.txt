# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luafish NONE )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

# LuaFish modules
install ( DIRECTORY lib/ DESTINATION ${INSTALL_LMOD} COMPONENT Runtime )
install_lua_executable ( luafish bin/luafish.lua )
install_lua_executable ( luafishcheck bin/luafishcheck.lua )
install_data ( COPYRIGHT HISTORY README )
install_test ( test/ )
install_example ( examples/ )
