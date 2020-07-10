# Benchmark result

* Pull request commit: [`3d7b6a98d5ec35cf925a800898a487c74a4f7251`](https://github.com/JuliaFolds/Transducers.jl/commit/3d7b6a98d5ec35cf925a800898a487c74a4f7251)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/319> (Treat transducers as iterator transforms at surface syntax)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Jul 2020 - 09:32
    - Baseline: 3 Jul 2020 - 09:36
* Package commits:
    - Target: df715e
    - Baseline: 8bcb4a
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`
    - Baseline: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                       | time ratio                   | memory ratio |
|------------------------------------------|------------------------------|--------------|
| `["filter_map_map!", "man"]`             |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.81 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.14 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   |                1.40 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.13 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`  | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.25 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "xf"]`               | 0.80 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`             |                1.12 (5%) :x: |   1.00 (1%)  |
| `["overhead", "foldl"]`                  | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["findall"]`
- `["gemm", "fusedmul", "blas"]`
- `["gemm", "fusedmul", "xf"]`
- `["gemm", "mul", "linalg"]`
- `["gemm", "mul", "man", "false"]`
- `["gemm", "mul", "man", "ivdep"]`
- `["gemm", "mul", "man", "true"]`
- `["gemm", "mul", "xf", "false"]`
- `["gemm", "mul", "xf", "ivdep"]`
- `["gemm", "mul", "xf", "true"]`
- `["groupby", "sum"]`
- `["missing_argmax"]`
- `["missing_dot"]`
- `["overhead"]`
- `["partition_by"]`

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      44996 s          0 s       1252 s      13863 s          0 s
       #2  2593 MHz      11830 s          0 s       1490 s      46266 s          0 s
       
  Memory: 6.791385650634766 GB (3114.265625 MB free)
  Uptime: 617.0 sec
  Load Avg:  1.11083984375  1.0478515625  0.6787109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      66516 s          0 s       1335 s      15002 s          0 s
       #2  2593 MHz      13124 s          0 s       1563 s      67569 s          0 s
       
  Memory: 6.791385650634766 GB (3075.4609375 MB free)
  Uptime: 844.0 sec
  Load Avg:  1.09716796875  1.0537109375  0.77197265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Jul 2020 - 9:32
* Package commit: df715e
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                       | time            | GC time | memory          | allocations |
|------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`               |  61.000 μs (5%) |         |  65.63 KiB (1%) |          74 |
| `["append!!", "xf"]`                     |  61.700 μs (5%) |         |  67.19 KiB (1%) |         124 |
| `["cat", "base"]`                        |   1.850 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.870 μs (5%) |         |   80 bytes (1%) |           3 |
| `["collect", "filter-missing"]`          | 104.800 μs (5%) |         | 345.36 KiB (1%) |       10018 |
| `["collect", "identity-float"]`          |  73.001 μs (5%) |         | 569.20 KiB (1%) |       10018 |
| `["collect", "identity-union"]`          | 312.101 μs (5%) |         | 705.19 KiB (1%) |       16671 |
| `["dot", "blas"]`                        |   1.210 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.200 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.144 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.156 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`             |  61.300 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 748.603 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 230.000 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 230.001 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 815.304 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 755.404 μs (5%) |         |   3.03 MiB (1%) |       99197 |
| `["findall", "xf-iter"]`                 |   3.176 ms (5%) |         |   9.63 MiB (1%) |      299922 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.262 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.162 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.811 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.340 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.284 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 656.402 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.574 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.628 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 891.604 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 243.145 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.570 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 457.868 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.577 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 382.266 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.570 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.929 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 490.769 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.576 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 379.902 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.591 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.663 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 452.792 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.574 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.829 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 380.788 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 247.001 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 185.001 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 188.400 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["missing_argmax", "man"]`              |   2.678 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   3.200 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.567 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.710 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.490 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.943 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.740 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 214.301 μs (5%) |         |  72.08 KiB (1%) |        3739 |
| `["missing_dot", "xf_nota"]`             | 212.101 μs (5%) |         |  71.89 KiB (1%) |        3733 |
| `["overhead", "foldl"]`                  |   4.700 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 179.716 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   2.078 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.037 ms (5%) |         |   6.10 MiB (1%) |      200007 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["findall"]`
- `["gemm", "fusedmul", "blas"]`
- `["gemm", "fusedmul", "xf"]`
- `["gemm", "mul", "linalg"]`
- `["gemm", "mul", "man", "false"]`
- `["gemm", "mul", "man", "ivdep"]`
- `["gemm", "mul", "man", "true"]`
- `["gemm", "mul", "xf", "false"]`
- `["gemm", "mul", "xf", "ivdep"]`
- `["gemm", "mul", "xf", "true"]`
- `["groupby", "sum"]`
- `["missing_argmax"]`
- `["missing_dot"]`
- `["overhead"]`
- `["partition_by"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      44996 s          0 s       1252 s      13863 s          0 s
       #2  2593 MHz      11830 s          0 s       1490 s      46266 s          0 s
       
  Memory: 6.791385650634766 GB (3114.265625 MB free)
  Uptime: 617.0 sec
  Load Avg:  1.11083984375  1.0478515625  0.6787109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Jul 2020 - 9:36
* Package commit: 8bcb4a
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                       | time            | GC time | memory          | allocations |
|------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`               |  60.900 μs (5%) |         |  65.63 KiB (1%) |          74 |
| `["append!!", "xf"]`                     |  61.900 μs (5%) |         |  67.19 KiB (1%) |         124 |
| `["cat", "base"]`                        |   1.770 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.820 μs (5%) |         |   80 bytes (1%) |           3 |
| `["collect", "filter-missing"]`          | 104.200 μs (5%) |         | 345.36 KiB (1%) |       10018 |
| `["collect", "identity-float"]`          |  72.100 μs (5%) |         | 569.20 KiB (1%) |       10018 |
| `["collect", "identity-union"]`          | 312.102 μs (5%) |         | 705.05 KiB (1%) |       16660 |
| `["dot", "blas"]`                        |   1.210 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.180 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.144 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.133 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`             |  58.300 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 749.903 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 230.001 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 231.200 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 795.003 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 764.803 μs (5%) |         |   3.04 MiB (1%) |       99437 |
| `["findall", "xf-iter"]`                 |   3.189 ms (5%) |         |   9.63 MiB (1%) |      299925 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.201 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.175 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.903 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.318 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.285 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 652.002 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.571 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.622 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 890.804 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.617 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.602 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.608 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.618 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.300 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.607 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.632 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 249.401 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 187.000 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 210.201 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["missing_argmax", "man"]`              |   2.678 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.550 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   3.200 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.700 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.490 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.843 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.560 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 207.501 μs (5%) |         |  71.89 KiB (1%) |        3733 |
| `["missing_dot", "xf_nota"]`             | 211.701 μs (5%) |         |  72.11 KiB (1%) |        3743 |
| `["overhead", "foldl"]`                  |   5.100 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 178.430 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   2.024 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.009 ms (5%) |         |   6.10 MiB (1%) |      200007 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["findall"]`
- `["gemm", "fusedmul", "blas"]`
- `["gemm", "fusedmul", "xf"]`
- `["gemm", "mul", "linalg"]`
- `["gemm", "mul", "man", "false"]`
- `["gemm", "mul", "man", "ivdep"]`
- `["gemm", "mul", "man", "true"]`
- `["gemm", "mul", "xf", "false"]`
- `["gemm", "mul", "xf", "ivdep"]`
- `["gemm", "mul", "xf", "true"]`
- `["groupby", "sum"]`
- `["missing_argmax"]`
- `["missing_dot"]`
- `["overhead"]`
- `["partition_by"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      66516 s          0 s       1335 s      15002 s          0 s
       #2  2593 MHz      13124 s          0 s       1563 s      67569 s          0 s
       
  Memory: 6.791385650634766 GB (3075.4609375 MB free)
  Uptime: 844.0 sec
  Load Avg:  1.09716796875  1.0537109375  0.77197265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:            7
    CPU MHz:             2593.905
    BogoMIPS:            5187.81
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |
