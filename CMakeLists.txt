cmake_minimum_required (VERSION 2.8)
project(NeuralNetworkSandbox)

set(CMAKE_CXX_FLAGS -std=c++11)

include_directories("${PROJECT_SOURCE_DIR}/src")
include_directories("${PROJECT_SOURCE_DIR}/src/Net")
include_directories("${PROJECT_SOURCE_DIR}/src/Neuron")
include_directories("${PROJECT_SOURCE_DIR}/src/TrainingDataHandler")

file(GLOB SOURCES "src/*.cpp"
                  "src/Net/*.cpp"
                  "src/Neuron/*.cpp"
                  "src/TrainingDataHandler/*.cpp")

add_executable(NeuralNetworkSandbox ${SOURCES})

file(COPY "${PROJECT_SOURCE_DIR}/data" DESTINATION ${CMAKE_CURRENT_BINARY_DIR} )
