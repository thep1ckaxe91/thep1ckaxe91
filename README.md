# Dao Phuong Nam
**Systems Engineer | High-Performance Computing | C++ Optimization**

Computer Science student at VNU-UET focused on **Hardware Sympathy**—optimizing memory layouts, minimizing CPU cache misses, and reducing instruction latency. I engineer software that respects the physical constraints of the hardware.

---

### Featured Project: High-Performance Tetris Engine

A study in transforming a legacy simulation into a high-throughput engine using **Data-Oriented Design** and **Linux Systems Programming**.

| Metric | Legacy Implementation | Optimized Engine (Current) | Improvement |
| :--- | :--- | :--- | :--- |
| **Throughput** | ~70 FPS | **~7,000 FPS** (Uncapped) | **100x** |
| **Render Latency** | 16.6ms | **0.06ms** | **99.6% Reduction** |
| **Memory Strategy** | Heap (Linked Lists) | Stack (Ring Buffers) | Stable Frame Times |

**Key Engineering Decisions:**
* **Rendering:** Bypassed SDL2 immediate mode by implementing **Texture Locking** for direct pixel buffer manipulation (CPU $\to$ VRAM).
* **Memory:** Removed non-deterministic heap allocations (`std::list`) in the hot path, replacing them with **Stack-Allocated Ring Buffers** (`std::array`) to eliminate GC-like pauses.
* **Diagnostics:** Profiling via `perf` and Hotspot to identify and eliminate driver overhead.

**Engineering Roadmap (Q1-Q2 2026):**
* [ ] **Modernization:** Refactoring legacy "C with Classes" patterns to idiomatic **C++20** (Concepts, Ranges, Strong Types).
* [ ] **Concurrency:** Decoupling Render and Logic loops into isolated threads using a **lock-free SPSC queue**, utilizing **CPU Affinity (Thread Pinning)** to prevent core migration and cache thrashing.
* [ ] **Networking:** Implementing a **LAN PvP layer** using non-blocking UDP sockets for real-time state synchronization (opponent view).
* [ ] **SIMD:** Exploring AVX2 intrinsics to vectorize collision detection (Stretch Goal).

[View Repository](https://github.com/thep1ckaxe91/Sandtris)

---

### Technical Arsenal

**Languages**
* **C++20:** Concepts, Move Semantics, RAII.
* **C:** Raw memory management, Linux System Calls.
* **Python:** Systems automation and build scripts.

**Systems & Tools**
* **Environment:** Linux (Arch/EndeavourOS), Bash, Vim.
* **Build/Debug:** CMake (FetchContent), GDB, Linux `perf`.
* **Virtualization:** Docker, Linux Namespaces/Seccomp.

**Core Competencies**
* Data-Oriented Design (DOD)
* Low-Latency Audio/Video Pipeline
* Lock-free Concurrency
* Algorithm Optimization (Graph Theory, Flow Networks)

---
