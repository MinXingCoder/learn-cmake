add_executable(main main.cpp)

add_library(mylib mylib.h mylib.cpp)

if(WIN32)
    set(WINDOWS_EXPORT_ALL_SYMBOLS ON)
endif()
add_library(mylib-shared SHARED mylib.h mylib.cpp)

install(TARGETS main mylib mylib-shared
ARCHIVE DESTINATION lib                  # mylib
RUNTIME DESTINATION bin                  # main, windos dll
LIBRARY DESTINATION lib                  # so, linux
)

install(FILES mylib.h
DESTINATION include
)

install(FILES README.md
DESTINATION doc
)