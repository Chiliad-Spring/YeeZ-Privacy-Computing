add_subdirectory(sgx)

add_library(ypc_core SHARED
  timer_loop.cpp
  sha.cpp
  db.cpp
  configuration.cpp
  sealed_file.cpp
  command_executor.cpp
  filesystem.cpp
  privacy_data_reader.cpp
  exceptions.cpp
  status.cpp
  ${PROJECT_SOURCE_DIR}/vendor/fflib/src/net/common/archive.cpp)

target_link_libraries(ypc_core ypc_common_u stbox_common_u mysqlcppconn cryptopp boost_program_options boost_filesystem boost_system glog dl)

