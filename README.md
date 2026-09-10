# Hi, I'm Lukas

I'm a CS undergrad at Northeastern. 

My current focus is AI inference optimization through model quantization kernels, KV-Cache quantization, and inference infrastructure.

## Current Project

### ARM NEON kernels for `IQ4_NL_Q8_0` — ggml / llama.cpp
Optimizing 4-bit quantized inference on **non-dotprod ARMv8.0-A** (testing on Cortex-A53 architecture), where ggml's dispatch silently falls back to an unaccelerated generic path.

- Identified a missing batched repacked GEMM kernel for non-dotprod ARMv8.0
- Kernel work in `ggml-cpu/arch/arm/repack.cpp`, portable to llama.cpp's ggml dependency

Finalizing tests before opening PR

## Previous Projects

### [unsloth-turboquant](https://github.com/lukasdim/unsloth-turboquant)
Fork of [Unsloth](https://github.com/unslothai/unsloth) adding TurboQuant KV-cache quantization to Unsloth Studio's inference frontend, passing arguments to beellama.cpp.

- Env-gated runtime injection at the inference hook
- From-source installer for the `beellama.cpp` fork with multi-backend dispatch

### [SEND](https://github.com/lukasdim/SEND) - 1st of 1,463 - Hackonomics 2026
Node-based platform for building and backtesting trading strategies from composable graphs. [Devpost](https://devpost.com/software/send-3k8o9w)

- Nodes cover data fetches, calculations, and buy/sell conditions; backtests over 6 months of data with daily P/L and replay
- Three-tier architecture: React frontend → Java/Spring REST API → **OCaml execution engine** over stdin/stdout
- Self-hosted end to end: Docker, nginx, Cloudflare Tunnel, PostgreSQL/TimescaleDB

## Research - PGSS at Carnegie Mellon

Selected as 1 of 72 from 403 applicants (18%) for the **Pennsylvania Governor's School for the Sciences** at CMU. My team's project and paper on occluded-face detection was published in the PGSS journal.

- **Paper:** [Hide and Seek — PGSS Journal Vol. 39](https://www.cmu.edu/mcs/pgss/journal-archive/vol39-classof2024.pdf#page=155)
- **CMU Article:** [Hide and Seek at Governor's School](https://www.cmu.edu/news/stories/archives/2024/July/hide-and-seek-governors-school)

**My Role:** Investigated IR depth and IR thermal sensor supplementation for **OpenFace** to improve detection of obscured faces. 
