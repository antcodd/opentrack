if(WIN32)
    otr_module(tracker-rs-impl STATIC NO-QT SOURCES "${SDK_REALSENSE}/opensource/src/libpxc/libpxc.cpp")
    target_compile_definitions(opentrack-tracker-rs-impl PRIVATE -DUNICODE -D_UNICODE)
    target_include_directories(opentrack-tracker-rs-impl PRIVATE SYSTEM "${SDK_REALSENSE}/include")
    target_link_libraries(opentrack-tracker-rs-impl advapi32)
endif()
