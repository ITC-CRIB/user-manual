Unsupported packages
====================

| Package          | Description                                                                        | Reason                                | Alternative   |
|------------------|------------------------------------------------------------------------------------|---------------------------------------|---------------|
| accimage         | High performance image loading and augmenting routines mimicking PIL               | Requires Intel PPI (Intel X86)        | Pillow        | 
| gpustat          | Utility to monitor NVIDIA GPU status and usage                                     | Requires NVML (not supported)         |               |
| gputil           | Module for getting the GPU status from NVIDA GPUs using nvidia-smi                 | Requires nvidia-smi (not supported)   |               |
| nvidia-ml-py     | Bindings for the NVIDIA Management Library                                         | Requires NVML (not supported)         |               |
| pillow-simd      | SIMD drop-in replacement for Pillow                                                | Requires AVX4 (Intel X86)             | Pillow        |
| pynvml           | Python Bindings for the NVIDIA Management Library                                  | Required NVML (not supported)         |               |
| py3nvml          | Bindings for the NVIDIA Management Library                                         | Requires NVML (not supported)         |               |
| tensorrt         | Bindings for TensorRT                                                              | Binary only, available for Python 3.6 |               |
