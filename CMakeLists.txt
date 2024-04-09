cmake_minimum_required(VERSION 3.15)

project(polybenchc)

include_directories(utilities)
add_definitions(-DPOLYBENCH_TIME)
add_library(polybench OBJECT utilities/polybench.c)

add_executable(correlation datamining/correlation/correlation.c)
target_link_libraries(correlation polybench)

add_executable(covariance datamining/covariance/covariance.c)
target_link_libraries(covariance polybench)

add_executable(gemm linear-algebra/blas/gemm/gemm.c)
target_link_libraries(gemm polybench)

add_executable(gemver linear-algebra/blas/gemver/gemver.c)
target_link_libraries(gemver polybench)

add_executable(gesummv linear-algebra/blas/gesummv/gesummv.c)
target_link_libraries(gesummv polybench)

add_executable(symm linear-algebra/blas/symm/symm.c)
target_link_libraries(symm polybench)

add_executable(syr2k linear-algebra/blas/syr2k/syr2k.c)
target_link_libraries(syr2k polybench)

add_executable(syrk linear-algebra/blas/syrk/syrk.c)
target_link_libraries(syrk polybench)

add_executable(trmm linear-algebra/blas/trmm/trmm.c)
target_link_libraries(trmm polybench)

add_executable(2mm linear-algebra/kernels/2mm/2mm.c)
target_link_libraries(2mm polybench)

add_executable(3mm linear-algebra/kernels/3mm/3mm.c)
target_link_libraries(3mm polybench)

add_executable(atax linear-algebra/kernels/atax/atax.c)
target_link_libraries(atax polybench)

add_executable(bicg linear-algebra/kernels/bicg/bicg.c)
target_link_libraries(bicg polybench)

add_executable(doitgen linear-algebra/kernels/doitgen/doitgen.c)
target_link_libraries(doitgen polybench)

add_executable(mvt linear-algebra/kernels/mvt/mvt.c)
target_link_libraries(mvt polybench)

add_executable(cholesky linear-algebra/solvers/cholesky/cholesky.c)
target_link_libraries(cholesky polybench)

add_executable(durbin linear-algebra/solvers/durbin/durbin.c)
target_link_libraries(durbin polybench)

add_executable(gramschmidt linear-algebra/solvers/gramschmidt/gramschmidt.c)
target_link_libraries(gramschmidt polybench)

add_executable(lu linear-algebra/solvers/lu/lu.c)
target_link_libraries(lu polybench)

add_executable(ludcmp linear-algebra/solvers/ludcmp/ludcmp.c)
target_link_libraries(ludcmp polybench)

add_executable(trisolv linear-algebra/solvers/trisolv/trisolv.c)
target_link_libraries(trisolv polybench)

add_executable(deriche medley/deriche/deriche.c)
target_link_libraries(deriche polybench)

add_executable(floyd-warshall medley/floyd-warshall/floyd-warshall.c)
target_link_libraries(floyd-warshall polybench)

add_executable(nussinov medley/nussinov/nussinov.c)
target_link_libraries(nussinov polybench)

add_executable(adi stencils/adi/adi.c)
target_link_libraries(adi polybench)

add_executable(fdtd-2d stencils/fdtd-2d/fdtd-2d.c)
target_link_libraries(fdtd-2d polybench)

add_executable(heat-3d stencils/heat-3d/heat-3d.c)
target_link_libraries(heat-3d polybench)

add_executable(jacobi-1d stencils/jacobi-1d/jacobi-1d.c)
target_link_libraries(jacobi-1d polybench)

add_executable(jacobi-2d stencils/jacobi-2d/jacobi-2d.c)
target_link_libraries(jacobi-2d polybench)

add_executable(seidel-2d stencils/seidel-2d/seidel-2d.c)
target_link_libraries(seidel-2d polybench)
