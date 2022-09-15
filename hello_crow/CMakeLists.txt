cmake_minimum_required(VERSION 3.7)

project(hello_crow)

set(CMAKE_CXX_STANDARD 11)
set(THREADS_PREFER_PTHREAD_FLAG ON)
set(CMAKE_PREFIX_PATH "/usr/local/mongo-cxx-driver/lib/cmake/libmongocxx-3.6.7" "/usr/local/mongo-cxx-driver/lib/cmake/libbsoncxx-3.6.7")

find_package(Boost COMPONENTS system filesystem REQUIRED)
find_package(Threads)
find_package(libmongocxx REQUIRED)

include_directories(${Boost_INCLUDE_DIRS})

add_executable(hello_crow main.cpp)

find_package(LIBMONGOCXX ${LIBMONGOCXX_REQUIRED_VERSION} REQUIRED CONFIGS libmongocxx-config.cmake)

target_include_directories(hello_crow PRIVATE ${Boost_LIBRARIES} ${LIBMONGOCXX_INCLUDE_DIRS})

target_link_libraries(hello_crow ${Boost_LIBRARIES} Threads::Threads ${LIBMONGOCXX_LIBRARIES})

include_directories(/usr/local/mongo-cxx-driver/include/mongocxx)