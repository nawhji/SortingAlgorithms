# Sorting Algorithms: Implementation and Benchmarking

Implementation and empirical benchmarking of 12 sorting algorithms from scratch in C++.

## Algorithms

| Algorithm | Time (avg) | Space | Stable |
|---|---|---|---|
| Bubble Sort | O(n²) | O(1) | ✓ |
| Insertion Sort | O(n²) | O(1) | ✓ |
| Selection Sort | O(n²) | O(1) | ✗ |
| Merge Sort | O(n log n) | O(n) | ✓ |
| Heap Sort | O(n log n) | O(1) | ✗ |
| Quick Sort | O(n log n) | O(log n) | ✗ |
| Introsort | O(n log n) | O(log n) | ✗ |
| Timsort | O(n log n) | O(n) | ✓ |
| Library Sort | O(n log n) | O(n) | ✗ |
| Cocktail Shaker Sort | O(n²) | O(1) | ✓ |
| Comb Sort | O(n²) | O(1) | ✗ |
| Tournament Sort | O(n log n) | O(n) | ✗ |

## Benchmarking

Each algorithm was tested across:
- **Input sizes**: 10³, 10⁴, 10⁵, 10⁶
- **Input distributions**: ascending, descending, random, partially sorted
- **Metrics**: execution time (avg over 10 runs), peak memory usage, correctness, stability

## Repository Structure

Each folder contains:
- `<algorithm>.cc` — implementation on a 1-indexed integer array
- `<algorithm>_test.cc` — benchmarking and correctness/stability verification
- `<algorithm>.csv` — recorded results

## Key Findings

- Comb Sort achieved the fastest and most consistent runtime among all O(n log n) algorithms
- Introsort showed stable performance across all input distributions due to its hybrid Quick/Heap fallback
- All 12 algorithms achieved 100% sorting accuracy across all test cases

## Build
```bash
g++ -O2 -o test <algorithm>/<algorithm>.cc
```

## Report

Full analysis available in the [project report](https://nawhji.github.io).
