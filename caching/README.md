## 🧠 What is Caching?

**Caching** is a concept where data is stored temporarily in a **fast-access storage layer (cache)**, allowing future requests for that data to be served more quickly.  
The primary purpose of caching is to **improve performance** and **reduce data retrieval time**.

🗂️ Typically, caches store data **in memory**, using technologies like **Redis**, **Memcached**, or **in-process caches**.

---

## ⚙️ How Does Cache Work?

When a client requests data:
1. The system first **checks the cache** to see if the data already exists (a **cache hit**).
2. If the data is found in the cache → it’s **served directly** from memory (faster).
3. If not found (**cache miss**) → the system **fetches data from the main storage** (like a database), and then **stores a copy** in the cache for next time.

This process helps reduce **network calls**, **database load**, and **overall latency**.


---

## 💾 Why Not Store Everything in Cache?

Although caching is fast, it’s not suitable for storing all data because:

- 🧠 **Volatile Storage:** Cache data is stored in **memory (RAM)**, which is **temporary** and can be lost on restart.  
- 💸 **Cost:** Memory hardware (RAM) is **more expensive** than persistent storage (like disks used in databases).  
- 📏 **Limited Size:** Caches have limited capacity and cannot hold large datasets.

Therefore, caching is best used for **frequently accessed** or **high-demand data**.

---

## 🧱 Common Cache Data Structures

Caches use various data structures depending on the implementation:

- **Key-Value Pair:** The most common structure (e.g., `user:123 → user data`)  
- **Stack / Queue:** Used in certain caching policies like **LRU (Least Recently Used)** or **FIFO (First In, First Out)**

---

## 🌍 Applications of Caching

Caching is used across multiple layers in system design:

1. **Web Page Caching**  
   Store rendered pages or fragments to speed up future page loads.

2. **Database Caching**  
   Cache results of frequent queries to reduce database load.

3. **CDN (Content Delivery Network)**  
   CDNs use caching to keep copies of static assets (images, videos, etc.) in **edge locations** across the globe.  
   This allows users to download data from the **nearest server**, improving performance.

4. **API Response Caching**  
   Cache responses of frequently requested APIs to avoid repeated computation or database queries.

---

## ⚠️ Drawbacks of Caching

While caching improves performance, it introduces some challenges:

- **Cache Inconsistency (Stale Data):** Cached data might become outdated if the main database changes.  
- **Distributed Cache Misses:**  
  In distributed systems with multiple servers behind a **load balancer**, each server might have its own local cache.  
  Since these caches don’t share data, one server may have cached information while another experiences a cache miss — causing inconsistent performance.
  
  Example:

- **Memory Management:** Caches must use efficient eviction policies (like **LRU**, **LFU**) to prevent memory overflow.

---

## 🏁 Summary

| Concept | Description |
|----------|-------------|
| **Cache** | A temporary in-memory storage for frequently accessed data |
| **Goal** | Reduce latency and improve response times |
| **Example Tools** | Redis, Memcached |
| **Cache Miss** | When data is not found in cache and must be fetched from main storage |
| **Cache Hit** | When requested data is found in the cache |
| **Drawback** | Volatile, expensive, limited, potential for stale data |

