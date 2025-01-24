cmake_minimum_required(VERSION 3.10)
project(deribit_trading)

# Set C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find CURL package
find_package(CURL REQUIRED)

# Create source file list
set(SOURCES
    src/auth.cpp
    src/account.cpp
    src/order.cpp
    src/cancel_order.cpp
    src/get_orderbook.cpp
    src/modify_order.cpp
    src/sell_order.cpp
    main.cpp
)

# Create executable
add_executable(main ${SOURCES})

# Add include directory
target_include_directories(main
    PRIVATE 
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

# Link with CURL
target_link_libraries(main 
    PRIVATE 
        CURL::libcurl
)
