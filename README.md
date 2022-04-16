## CMPT 431 Project Group 11

## Algorithm

Perform a Breath First Search started at source vertex, all vertices in the same
depth are within the same distance to the source. If the current depth no vertices has their distence updated, algorithm terminated.

`static_partition.cpp` has the code for pre-assign the workset used by threads, all vertices are pushed to `neighbor` by BFS
`partition[i]` is the index in `neighbor` of the first neighbor of the i-th vertex `vertex-ptr[i]`
`width-ptr` is the index in `neighbor` of the first vertex of depth i. (Based on the idea of CSR/CSC matrix format).

## Compile

```bash
make SSSP_parallel_ver0
```
Or

```bash
make SSSP_parallel_ver1
```

## Run

```bash
./SSSP_parallel_ver1 --source 0 --inputFile absolute_path_of_input_graph --nThreads 4
```
## Result

Input graph: web-Google (900000+ vertices)
Thread #      :  1    2     4
Time(local PC): <4s  30s+  220s+
