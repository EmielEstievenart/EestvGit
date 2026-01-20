add_library(eestvgit STATIC src/eestv/git/version.cpp)

add_library(EestvGit::EestvGit ALIAS eestvgit)

target_compile_features(eestvgit PUBLIC cxx_std_17)

target_include_directories(
  eestvgit PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/includes>
                  $<INSTALL_INTERFACE:include>)
