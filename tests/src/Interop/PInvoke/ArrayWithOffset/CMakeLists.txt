cmake_minimum_required (VERSION 2.6) 
project (ArrayWithOffsetNative) 
include ("${CLR_INTEROP_TEST_ROOT}/Interop.cmake") 
include_directories(${INC_PLATFORM_DIR}) 
set(SOURCES 
    ArrayWithOffsetNative.cpp 
) 
if(WIN32)
    list(APPEND LINK_LIBRARIES_ADDITIONAL
        OleAut32.lib
    )
endif(WIN32)
# add the executable 
add_library (ArrayWithOffsetNative SHARED ${SOURCES}) 
target_link_libraries(ArrayWithOffsetNative ${LINK_LIBRARIES_ADDITIONAL}) 
# add the install targets 
install (TARGETS ArrayWithOffsetNative DESTINATION bin) 
