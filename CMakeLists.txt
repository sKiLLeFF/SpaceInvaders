cmake_minimum_required(VERSION 3.6)
project(SpaceInvaders)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -lmingw32")
set(CMAKE_EXE_LINKER_FLAGS "-static-libgcc -static-libstdc++")

include_directories(${PROJECT_SOURCE_DIR}/include)
link_directories(${PROJECT_SOURCE_DIR}/lib)


set(SOURCE_FILES main.cpp Entity.cpp Entity.h Game.cpp Game.h Player.h AbstractFactory.h SDLFactory.cpp SDLFactory.h SDLPlayer.cpp SDLPlayer.h Enum.h Rocket.h SDLRocket.cpp SDLRocket.h Enemy.h SDLEnemy.cpp SDLEnemy.h Player.cpp SDLRender.h SDLRender.cpp)
add_executable(SpaceInvaders ${SOURCE_FILES})

target_link_libraries(SpaceInvaders SDL2main SDL2 SDL2_ttf SDL2_mixer)