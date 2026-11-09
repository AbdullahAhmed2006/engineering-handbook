# Virtual Memory Paging and Translation Lookaside Buffer

**Date Published:** 2026-11-09 (Automated Knowledge Engine)
**Category:** `internals`

---

Virtual memory decouples process address spaces from physical DRAM. The CPU Memory Management Unit (MMU) uses multi-level Page Tables to map virtual page numbers (VPN) to physical frame numbers (PFN).

### TLB Role:
Traversing page tables requires multiple memory accesses. The Translation Lookaside Buffer (TLB) acts as a high-speed hardware cache for page table mappings, reducing average address translation latency to under a nanosecond.

---
*Verified Engineering Note for CS Knowledge Base.*