find_package(Eigen3 REQUIRED CONFIG)

if(OpenCV_FOUND)
camodocal_library(camodocal_sparse_graph STATIC
  Odometry.cc
  Pose.cc
  SparseGraph.cc
  SparseGraphUtils.cc
  Transform.cc
)

camodocal_link_libraries(camodocal_sparse_graph
  ${CAMODOCAL_PLATFORM_UNIX_LIBRARIES}
  ${Boost_FILESYSTEM_LIBRARY}
  ${Boost_SYSTEM_LIBRARY}
  ${OpenCV_LIBS}
  ::Eigen3
)

camodocal_install(camodocal_sparse_graph)
endif(OpenCV_FOUND)
