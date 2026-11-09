# B-Tree Splitting and Write Amplification in Storage Engines

- **Author:** Abdullah Ahmed (@AbdullahAhmed2006)
- **Entry:** #2 for 2026-11-09
- **Category:** `databases`

---

### B+ Tree Node Splitting
When an index leaf page exceeds the maximum block size (typically 8KB), an interior node split occurs. While lookups remain optimal at $O(\log N)$, random insertions cause page fragmentation and write amplification.

```sql
-- Create partitioned index to prevent page hot-spots
CREATE TABLE sensor_readings (
    recorded_at TIMESTAMPTZ NOT NULL,
    reading_val DOUBLE PRECISION
) PARTITION BY RANGE (recorded_at);
```

**Remediation:** Bulk loading and sequential monotonically increasing keys minimize page split overhead.

---
*Automated Computer Science & Engineering Architecture Vault.*