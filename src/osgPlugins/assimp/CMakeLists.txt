SET(TARGET_SRC ReaderWriterAssimp.cpp)

find_package(assimp REQUIRED
  PATHS
  "$ENV{HOME}/Rvbust/Install/Assimp/lib/cmake/assimp-5.0/"
  NO_DEFAULT_PATH)

SETUP_PLUGIN(assimp)
target_link_libraries(osgdb_assimp PRIVATE assimp::assimp)

