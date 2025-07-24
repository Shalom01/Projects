# Projects
A list of projects I am actively working on, or working towards:


# (1) Lock-Free Data Structures Library
 * **Fomitchev & Ruppert List** 
 * **Asbell & Ruppert Adaptive List** 
 * **Naderibeni & Ruppert Queue** 
 * **FEAST lock-Free BST** 

# (2) Low‑Latency FIX Engine — Project Summary (C++)

* **Language / Goal**

  * C++ FIX 4.2/4.4 stack targeting **sub‑100 µs p99 RTT** on localhost.

* **Core Components**

  * **FIX Gateway**: custom FIX codec + full session management (Logon, Heartbeat, Resend, Logout).
  * **SPSC lock‑free rings**: in‑process handoff of decoded orders/ERs between threads.
  * **Exchange Simulator (single thread per shard)**: risk checks, in‑memory limit order book, matching, ER generation.
  * **WAL**: mmap’d **append‑only log** with async/group‑commit flushing and periodic snapshots.

* **Benchmark Client**

  * Generates FIX traffic (NOS/Cancel/Replace), measures **p50/p99/p99.9** RTT, validates resend/recovery logic.

* **Deliverables**

  * Binaries: `fix_gateway`, `exchange_sim`, `fix_bench_client`.
  * Latency reports, WAL replay & snapshot tools.
 

