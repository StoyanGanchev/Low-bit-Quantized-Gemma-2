# Low-bit-Quantized-Gemma-2

## Description
In this project, we explore the capabilities and limitations of Gemma-2 when subjected to low-bit quantization. We conduct an empirical evaluation of various post-training quantization methods on Gemma-2, examining their impact on model performance across different bit-widths and benchmarks. Our study aims to provide a comprehensive understanding of Gemma-2’s behavior under quantization, identify the challenges associated with performance degradation, and propose potential solutions to mitigate these issues.

## Benchmark results:
Gemma-2-9B
| Benchmark               | Wiki  | C4    | PIQA  | ARC-E | ARC-C  | HellaSwag | Wino  | Avg.  |
|-------------------------|-------|-------|-------|-------|--------|-----------|-------|-------|
| Metric                  | 0-shot| 0-shot| 0-shot| 0-shot| 25-shot| 0-shot    | 0-shot| -     |
| Gemma-2-9B unquantized  | 6.88  | 10.12 | 81.39 | 87.25 | 64.33  | 61.27     | 74.11 | 73.67 |
| Gemma-2-9B (INT4) g128  | 7.27  | 11.34 | 80.47 | 85.86 | 63.23  | 59.55     | 74.27 | 72.67 |
| Gemma-2-9B (NF4) g128   | 7.05  | 11.04 | 81.45 | 86.78 | 64.62  | 60.87     | 74.51 | 73.65 |
| Gemma-2-9B (AWQ4) g128  | 7.07  | 11.05 | 80.68 | 86.57 | 62.96  | 60.52     | 73.71 | 72.89 |

Gemma-2-2B
| Benchmark               | Wiki  | C4    | PIQA  | ARC-E | ARC-C  | HellaSwag | Wino  | Avg.  |
|-------------------------|-------|-------|-------|-------|--------|-----------|-------|-------|
| Metric                  | 0-shot| 0-shot| 0-shot| 0-shot| 25-shot| 0-shot    | 0-shot| -     |
| Gemma-2-2B unquantized  | 8.76  | 12.54 | 78.40 | 80.18 | 50.85  | 54.98     | 68.90 | 66.66 |
| Gemma-2-2B (INT4) g128  | 9.81  | 13.80 | 77.48 | 78.24 | 43.43  | 51.62     | 67.80 | 63.72 |
| Gemma-2-2B (NF4) g128   | 9.15  | 13.05 | 78.02 | 78.96 | 49.15  | 53.53     | 69.14 | 65.76 |
| Gemma-2-2B (AWQ4) g128  | 11.05 | 12.99 | 78.18 | 78.95 | 45.05  | 53.55     | 68.19 | 64.78 |


