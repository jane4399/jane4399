## Yilin Xie

B.S. Mathematics–Computer Science, UC San Diego (2026). I work on systems software — the layer where
correctness is hard to *demonstrate*, not just hard to write.

Mostly C and C++. Currently interested in distributed consensus, deterministic testing, and
low-latency data structures.

---

### Selected work

**[raft-kv-store](https://github.com/jane4399/raft-kv-store)** — Raft consensus and a replicated
key-value store, C++20, zero dependencies.
The consensus core is a pure state machine — no threads, no clock, no I/O — so an entire cluster runs
inside a single-threaded seeded simulator at ~190 complete crash-and-partition runs per second, and
any failure replays exactly from a 64-bit seed. Verified over 1.2M committed operations across 6,900
adversarial seeds with zero safety or linearizability violations.

**[cpp-matching-engine](https://github.com/jane4399/cpp-matching-engine)** — Price-time-priority limit
order book, C++20.
Lock-free SPSC ring buffer feeding a deterministic single-threaded matching core. ~10–21M orders/sec,
p99 latency ~200–460 ns, with byte-identical deterministic replays verified by SHA-256.

**[unix-shell-c](https://github.com/jane4399/unix-shell-c)** — UNIX-style shell in C11.
Recursive-descent parser, pipelines, I/O redirection and here-docs, and job control with process
groups, `tcsetpgrp` terminal handover, and correct `SIGINT`/`SIGTSTP`/`SIGCHLD` handling.
AddressSanitizer- and valgrind-clean.

---

Personal experiments and smaller things live on my other account: **[@kirakilL](https://github.com/kirakilL)**

📫 kira.killa123@gmail.com · [LinkedIn](https://linkedin.com/in/yilin-xie-673671334)
