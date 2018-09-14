find_package(Eigen3 REQUIRED CONFIG)
camodocal_library(camodocal_pose_estimation STATIC
  P3P.cc
)

target_link_libraries(camodocal_pose_estimation PUBLIC ::Eigen3)

camodocal_install(camodocal_pose_estimation)