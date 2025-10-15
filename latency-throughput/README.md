# ⚙️ Latency and Throughput

## 🚀 Latency

**Latency** refers to the **delay or lag** between sending a request and receiving a response.  
It measures **how long it takes** for data to travel from the **client → server → client** again.

🧮 **Measured in:** milliseconds (ms) or seconds (s)

In short:  
> **Latency = Network Delay + Computational Delay**

---

### 🧠 Example

When a client sends a request to a server:
1. The request travels through the **network** to reach the server.  
2. The server processes it, possibly querying a **database** or another service.  
3. The response travels back through the **network** to the client.

Each step adds some delay (latency).

Let’s assume:
- **t₁** → network delay (client → server)  
- **t₂** → computational delay (server processing time)  
- **t₃** → network delay (server → client)

Then:

> **Total Latency = t₁ + t₂ + t₃**

---

## ⚡ Throughput

**Throughput** represents **how much data or load** a system can handle **over a given period of time**.

🧮 **Measured in:** bits per second (bps), often **Megabits per second (Mbps)**

It tells us how *efficiently* a system processes requests or transmits data.

> **Example:**  
> A database can write **100 records per second** into a table.  
> If more data arrives than it can handle, it may show **timeout or overload errors**.

---

## 🔁 Relationship Between Latency and Throughput

While **latency** and **throughput** are different, they are closely connected:

| Concept | Meaning | Effect |
|----------|----------|--------|
| **Latency** | Time delay in a single request/response | Higher latency → Slower responses |
| **Throughput** | Amount of work done per unit time | Higher latency → Lower throughput |

💡 In simple terms:  
- If **latency is high**, each request takes longer → **throughput decreases**  
- If **latency is low**, more requests can be handled in the same time → **throughput increases**

---

## 🌐 Networking Context

In networking, **throughput** depends on:
- Network bandwidth  
- Packet loss  
- Network congestion  
- Distance between client and server  

And **latency** depends on:
- Physical distance  
- Network routing hops  
- Server load and processing time  

---

### 🏁 Summary

| Term | Definition | Unit | Example |
|------|-------------|------|----------|
| **Latency** | Time delay between request and response | ms or s | Request takes 150ms to complete |
| **Throughput** | Amount of data processed per second | Mbps | API handles 200 requests/sec |

---

### 💬 In Short
> **Latency** → How fast a single request completes.  
> **Throughput** → How many requests the system can handle per second.
