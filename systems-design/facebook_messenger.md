# [Facebook Messenger] — System design

**Date:** 2026-03-19  
**Source:** (e.g. Interview, side project, blog post)

---

## 1. Requirements
- should support real time ultra low latency when users are online
- when user is offline, notify them they have a message
- messages should never be lost
- should support 1 to 1 conversations, and group chats up to 50 people

### Functional
- 
- 

### Non-functional
- Scale (QPS, users, data size):
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