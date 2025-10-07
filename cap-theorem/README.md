## ⚖️ CAP Theorem

**CAP** stands for **Consistency**, **Availability**, and **Partition Tolerance** — the three core properties of distributed systems.  

In any distributed system, you can **only guarantee two out of the three** at any given time.  

| Property | Meaning | Example |
|-----------|----------|----------|
| **Consistency (C)** | Every read receives the most recent write — all nodes see the same data at the same time. | When you update one server, all other servers are updated immediately. |
| **Availability (A)** | The system is always up and responsive — every request receives a response (success or failure). | The server remains live and ready to handle requests at all times. |
| **Partition Tolerance (P)** | The system continues to function even if communication between nodes fails (network partition). | Even if one server or network link fails, the overall system keeps running. |

---

### 🔹 The Trade-Off

You can’t have **all three** simultaneously — you must choose any **two**:

- **CA (Consistency + Availability)** → Not possible in real distributed systems because network failures (P) are unavoidable.  
- **CP (Consistency + Partition Tolerance)** → Prioritizes data accuracy over availability.  
- **AP (Availability + Partition Tolerance)** → Prioritizes uptime and responsiveness over perfect data consistency.  

Since **Partition Tolerance (P)** is essential in distributed environments, real-world systems must choose between **CP** and **AP**.

---

### 💡 When to Use What?

| Scenario | Choose | Reason |
|-----------|---------|--------|
| **Banking or Financial Systems** | **CP** | Accuracy and consistency of data (e.g., balance after a transaction) are critical. Temporary unavailability is acceptable. |
| **E-commerce, Social Media, or Content Platforms** | **AP** | High availability is more important. Slight data delay (eventual consistency) is acceptable to keep the system responsive. |

---

**Summary:**  
> - **Consistency:** Every node shows the same data.  
> - **Availability:** The system is always responsive.  
> - **Partition Tolerance:** The system survives network failures.  
>  
> In distributed systems, **Partition Tolerance (P)** is mandatory, so you must choose between **Consistency (C)** and **Availability (A)** based on your use case.
