cmake_minimum_required(VERSION 3.15)

project(polybenchc)

include_directories(utilities)
add_definitions(-DPOLYBENCH_TIME)
add_library(polybench OBJECT utilities/polybench.c)

add_executable(datamining_correlation datamining/correlation/correlation.c)
target_link_libraries(datamining_correlation polybench)

add_executable(datamining_covariance datamining/covariance/covariance.c)
target_link_libraries(datamining_covariance polybench)

add_executable(linear-algebra_blas_gemm linear-algebra/blas/gemm/gemm.c)
target_link_libraries(linear-algebra_blas_gemm polybench)

add_executable(linear-algebra_blas_gemver linear-algebra/blas/gemver/gemver.c)
target_link_libraries(linear-algebra_blas_gemver polybench)

add_executable(linear-algebra_blas_gesummv linear-algebra/blas/gesummv/gesummv.c)
target_link_libraries(linear-algebra_blas_gesummv polybench)

add_executable(linear-algebra_blas_symm linear-algebra/blas/symm/symm.c)
target_link_libraries(linear-algebra_blas_symm polybench)

add_executable(linear-algebra_blas_syr2k linear-algebra/blas/syr2k/syr2k.c)
target_link_libraries(linear-algebra_blas_syr2k polybench)

add_executable(linear-algebra_blas_syrk linear-algebra/blas/syrk/syrk.c)
target_link_libraries(linear-algebra_blas_syrk polybench)

add_executable(linear-algebra_blas_trmm linear-algebra/blas/trmm/trmm.c)
target_link_libraries(linear-algebra_blas_trmm polybench)

add_executable(linear-algebra_kernels_2mm linear-algebra/kernels/2mm/2mm.c)
target_link_libraries(linear-algebra_kernels_2mm polybench)

add_executable(linear-algebra_kernels_3mm linear-algebra/kernels/3mm/3mm.c)
target_link_libraries(linear-algebra_kernels_3mm polybench)

add_executable(linear-algebra_kernels_atax linear-algebra/kernels/atax/atax.c)
target_link_libraries(linear-algebra_kernels_atax polybench)

add_executable(linear-algebra_kernels_bicg linear-algebra/kernels/bicg/bicg.c)
target_link_libraries(linear-algebra_kernels_bicg polybench)

add_executable(linear-algebra_kernels_doitgen linear-algebra/kernels/doitgen/doitgen.c)
target_link_libraries(linear-algebra_kernels_doitgen polybench)

add_executable(linear-algebra_kernels_mvt linear-algebra/kernels/mvt/mvt.c)
target_link_libraries(linear-algebra_kernels_mvt polybench)

add_executable(linear-algebra_solvers_cholesky linear-algebra/solvers/cholesky/cholesky.c)
target_link_libraries(linear-algebra_solvers_cholesky polybench)

add_executable(linear-algebra_solvers_durbin linear-algebra/solvers/durbin/durbin.c)
target_link_libraries(linear-algebra_solvers_durbin polybench)

add_executable(linear-algebra_solvers_gramschmidt linear-algebra/solvers/gramschmidt/gramschmidt.c)
target_link_libraries(linear-algebra_solvers_gramschmidt polybench)

add_executable(linear-algebra_solvers_lu linear-algebra/solvers/lu/lu.c)
target_link_libraries(linear-algebra_solvers_lu polybench)

add_executable(linear-algebra_solvers_ludcmp linear-algebra/solvers/ludcmp/ludcmp.c)
target_link_libraries(linear-algebra_solvers_ludcmp polybench)

add_executable(linear-algebra_solvers_trisolv linear-algebra/solvers/trisolv/trisolv.c)
target_link_libraries(linear-algebra_solvers_trisolv polybench)

add_executable(medley_deriche medley/deriche/deriche.c)
target_link_libraries(medley_deriche polybench)

add_executable(medley_floyd-warshall medley/floyd-warshall/floyd-warshall.c)
target_link_libraries(medley_floyd-warshall polybench)

add_executable(medley_nussinov medley/nussinov/nussinov.c)
target_link_libraries(medley_nussinov polybench)

