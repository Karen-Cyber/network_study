SET(TEST_SOURCES 
    # hello_server
    # hello_client
    low_read
    )

FOREACH (test_src ${TEST_SOURCES})
    ADD_EXECUTABLE(${test_src} ${test_src}.c)
    TARGET_LINK_LIBRARIES(${test_src} ${NET_LIBRARY})
ENDFOREACH (test_src)