cmake_minimum_required(VERSION 3.8)
project(httpclient)
#set(CMAKE_CXX_FLAGS "-m32") 
set(CMAKE_CXX_STANDARD 11)
#set(INCLUDES
#        http.h
#        http_parser.h
#        krypton.h)
		
set(SOURCE_FILES
        http.c
        http.h
        http_parser.c
        http_parser.h
        krypton.c
        krypton.h
        main.c)
		
#ADD_LIBRARY(httpclient_dll SHARED ${INCLUDES} ${SOURCE_FILES})
#TARGET_LINK_LIBRARIES(httpclient_dll ${LINK_LIBS})
#INSTALL(TARGETS httpclient_dll DESTINATION  ${CMAKE_CURRENT_SOURCE_DIR}/lib)
#set_target_properties(httpclient_dll PROPERTIES COMPILE_FLAGS "-m32" LINK_FLAGS "-m32") 

add_executable(httpclient ${SOURCE_FILES})
set_target_properties(httpclient PROPERTIES COMPILE_FLAGS "-m32" LINK_FLAGS "-m32") 