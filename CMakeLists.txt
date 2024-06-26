cmake_minimum_required(VERSION 3.27)
project(Stockfish)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_EXE_LINKER_FLAGS "-static")

include_directories(src)
include_directories(src/incbin)
include_directories(src/nnue)
include_directories(src/nnue/features)
include_directories(src/nnue/layers)
include_directories(src/syzygy)

add_executable(Stockfish
        src/incbin/incbin.h
        src/nnue/features/half_ka_v2_hm.cpp
        src/nnue/features/half_ka_v2_hm.h
        src/nnue/layers/affine_transform.h
        src/nnue/layers/affine_transform_sparse_input.h
        src/nnue/layers/clipped_relu.h
        src/nnue/layers/simd.h
        src/nnue/layers/sqr_clipped_relu.h
        src/nnue/network.cpp
        src/nnue/network.h
        src/nnue/nnue_accumulator.h
        src/nnue/nnue_architecture.h
        src/nnue/nnue_common.h
        src/nnue/nnue_feature_transformer.h
        src/nnue/nnue_misc.cpp
        src/nnue/nnue_misc.h
        src/syzygy/tbprobe.cpp
        src/syzygy/tbprobe.h
        src/benchmark.cpp
        src/benchmark.h
        src/bitboard.cpp
        src/bitboard.h
        src/evaluate.cpp
        src/evaluate.h
        src/main.cpp
        src/misc.cpp
        src/misc.h
        src/movegen.cpp
        src/movegen.h
        src/movepick.cpp
        src/movepick.h
        src/perft.h
        src/position.cpp
        src/position.h
        src/search.cpp
        src/search.h
        src/thread.cpp
        src/thread.h
        src/thread_win32_osx.h
        src/timeman.cpp
        src/timeman.h
        src/tt.cpp
        src/tt.h
        src/tune.cpp
        src/tune.h
        src/types.h
        src/uci.cpp
        src/uci.h
        src/ucioption.cpp
        src/ucioption.h)
