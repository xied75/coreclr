cmake_minimum_required (VERSION 2.6) 
project (PInvokeIntNative) 
include ("${CLR_INTEROP_TEST_ROOT}/Interop.cmake") 
include_directories(${INC_PLATFORM_DIR}) 
set(SOURCES PInvokeIntNative.cpp) 
add_library (PInvokeIntNative SHARED ${SOURCES}) 
# add the install targets 
install (TARGETS PInvokeIntNative DESTINATION bin) 
