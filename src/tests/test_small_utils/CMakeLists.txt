set(exe_name test_small_utils)

set(depends_on_lib small_utils)

target_collect_sources(${exe_name})

add_executable(${exe_name} ${${exe_name}_files})

set_all_warnings(${exe_name} PUBLIC)

target_link_libraries(${exe_name} PRIVATE ${depends_on_lib})
target_link_libraries(${exe_name} PRIVATE GTest_Integrated)
