add_executable(alignment alignment.cpp)
target_link_libraries(alignment Threads::Threads)
if (MSVC)
    target_compile_options(alignment PRIVATE /W4 /WX)
else()
    target_compile_options(alignment PRIVATE -Wall -Wextra -pedantic -Werror)
endif()
