
pybind11_add_module(kp src/main.cpp)

include_directories(
        ${PROJECT_SOURCE_DIR}/include/)

target_link_libraries(
        kp PRIVATE
        kompute::kompute)

# Only the Python module needs KOMPUTE_BUILD_PYTHON
target_compile_definitions(kp PRIVATE KOMPUTE_BUILD_PYTHON=1)
