cmake_minimum_required(VERSION 3.13.4)

project(byedpi)

add_compile_definitions(_WIN32_WINNT=0x0600)

set(SOURCES packets.c main.c conev.c proxy.c desync.c mpool.c extend.c win_service.c)

add_executable(byedpi ${SOURCES})
target_link_libraries(byedpi PRIVATE ws2_32 mswsock)
