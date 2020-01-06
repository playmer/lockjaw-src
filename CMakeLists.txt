cmake_minimum_required(VERSION 3.14.0 FATAL_ERROR) 
set_property(GLOBAL PROPERTY USE_FOLDERS ON)  
project(lockjaw CXX C)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH};${CMAKE_CURRENT_LIST_DIR}/cmake/)

find_package(Allegro REQUIRED)

add_executable(lockjaw "")

add_subdirectory(src)
target_include_directories(lockjaw PRIVATE ${Allegro_INCLUDE_DIR})
target_link_libraries(lockjaw PRIVATE ${Allegro_LIBRARY}
/usr/lib/x86_64-linux-gnu/liballegro_color.so
/usr/lib/x86_64-linux-gnu/liballegro_image.so
/usr/lib/x86_64-linux-gnu/liballegro_main.so
/usr/lib/x86_64-linux-gnu/liballegro_ttf.so
/usr/lib/x86_64-linux-gnu/liballegro_video.so
/usr/lib/x86_64-linux-gnu/liballegro_audio.so
/usr/lib/x86_64-linux-gnu/liballegro_font.so
/usr/lib/x86_64-linux-gnu/liballegro_primitives.so
/usr/lib/x86_64-linux-gnu/libaldmb.so.1
/lib/x86_64-linux-gnu/libdumb.so.1
)