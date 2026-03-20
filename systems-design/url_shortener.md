# [Design a URL Shortener] — System design

**Date:** 2026-03-17  
**Source:** Review

---

## 1. Requirements

### Functional
- Take a long URL and convert it into a shortened url
- Block duplicates
- 

### Non-functional
- Scale (QPS, users, data size):
1 billion users
1% are creators
99% are just clicking links

- Latency:

- Availability / durability:


### Out of scope
- 

---

## 2. High-level design

- **One-line summary:**
- **Diagram (ASCII or link):**

```
[Client] → [API / LB] → [Services] → [Storage / Cache / Queue]
```

- **Main components and responsibilities:**

| Component | Responsibility |
|-----------|----------------|
|           |                 |

---

## 3. Data model & storage

- **Key entities:**
- **Read vs write pattern:** (e.g. read-heavy → cache, write-heavy → …)
- **Storage choices:** (SQL vs NoSQL, why; caching layer if any)

---

## 4. APIs (if applicable)

| Endpoint | Purpose |
|----------|---------|
|          |         |

---

## 5. Deep dives (pick 1–2)

### [Topic A, e.g. consistency, partitioning, caching]
- 
- 

### [Topic B]
- 
- 

---

## 6. Scale / back-of-envelope

- DAU / QPS / storage growth:
- Bottlenecks and mitigations:

---

## 7. Failure modes & ops

- Single points of failure:
- Failover / replication:
- Monitoring and alerts:

---

## 8. Tradeoffs & alternatives

- What we chose and why:
- What we gave up:
- Alternatives considered:

---

## 9. Summary / one-pager

- 
- 