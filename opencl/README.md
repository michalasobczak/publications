# OpenCL. Programowanie CPU i GPU

Ridero, 2022 · ISBN 978-83-8273-803-2 · in Polish. Part of the *Simple High Performance Computing* series.

More than a decade after OpenCL appeared, the book explains the standard and the hardware it runs on, then shows working examples on both historic and current CPUs and GPUs — to test whether theory matches practice. The examples reach up to a **50× speed-up of the GPU over the CPU** on the same algorithm.

- About the book: https://michalasobczak.pl/posts/opencl.html
- Free PDF: https://michalasobczak.pl/wp-content/uploads/2022/09/OpenCL.pdf

## Examples

Java with [JOCL](http://www.jocl.org/); each folder is an IntelliJ IDEA module.

| Module | What it does |
|---|---|
| [src](src) | main module, shared OpenCL setup |
| [bandwidth](bandwidth) | performance of scalar operations |
| [c64_3d](c64_3d) | orthographic and perspective projection |
| [naive_sort](naive_sort) | array indexing with a naive sort |
| [sort2](sort2) | a second sorting approach |
| [reduction](reduction) | parallel reduction |
| [pi_est_monte_carlo](pi_est_monte_carlo) | estimating π by the Monte Carlo method |
| [picture](picture) | image processing |
| [des](des) | DES-related computation (FP32 vs FP64 devices) |
| [aiml](aiml) | AI/ML experiments |
| [reference_c](reference_c) | plain C reference implementations |

## How to run

Build the main module and the example (e.g. `bandwidth`) into `out/production`, download the JOCL JAR, then:

```
java -classpath publications/opencl/out/production/bandwidth\
:jocl-2.0.2.jar\
:publications/opencl/out/production/opencl com.michalasobczak.bandwidth.Main
```

Or run it straight from IntelliJ IDEA or another IDE.
