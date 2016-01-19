add_executable(ceph_test_cls_lua
  test_cls_lua.cc
)
set_target_properties(ceph_test_cls_lua PROPERTIES COMPILE_FLAGS
    ${UNITTEST_CXX_FLAGS})
target_link_libraries(ceph_test_cls_lua
  liblua
  cls_lua_client
  librados
  global
  ${UNITTEST_LIBS}
  ${CMAKE_DL_LIBS}
  ${EXTRALIBS}
  radostest
)
