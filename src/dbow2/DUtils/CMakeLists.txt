camodocal_library(camodocal_dutils STATIC
  BinaryFile.cpp
  ConfigFile.cpp
  DebugFunctions.cpp
  FileFunctions.cpp
  LineFile.cpp
  LUT.cpp
  Profiler.cpp
  Random.cpp
  StringFunctions.cpp
  TimeManager.cpp
  Timestamp.cpp
)

if (MSVC)
    target_link_libraries(camodocal_dutils PUBLIC Ws2_32.lib)
endif()

camodocal_install(camodocal_dutils)