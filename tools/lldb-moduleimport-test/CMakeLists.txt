add_swift_executable(lldb-moduleimport-test
  lldb-moduleimport-test.cpp
  LINK_LIBRARIES
    swiftASTSectionImporter swiftFrontend swiftClangImporter
  LLVM_COMPONENT_DEPENDS
    DebugInfoCodeView
)

swift_install_in_component(testsuite-tools
    TARGETS lldb-moduleimport-test
    RUNTIME DESTINATION "bin")

