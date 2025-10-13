# 🧱 Monolithic vs Distributed Systems

## 🧩 Monolithic Architecture

A **Monolithic architecture** is a system where all components are combined into a single unit.  
This means the **UI layer**, **business logic**, and **data layer** all live in one codebase and run as one service.

### 🔹 Example
A traditional web application where the frontend, backend, and database access are tightly coupled and deployed together on a single server.

---

### ✅ Pros
- **Easy to deploy:** Everything runs on a single server.  
- **Simple team management:** One team can handle the entire system.  
- **Cost-effective:** Minimal infrastructure and server costs.

### ❌ Cons
- **Hard to maintain:** As the codebase grows, it becomes complex to manage.  
- **Single point of failure:** If one part breaks, the entire system may fail.  
- **Difficult debugging:** Tight coupling makes it harder to isolate and fix issues.

---

## 🌐 Distributed System

A **Distributed System** is a collection of multiple computers (or nodes) connected via a network that work together as one cohesive system.

Each node can perform tasks independently, but collectively, they deliver the full system functionality.

---

### ⚖️ Centralized vs Distributed Systems

| Type | Description |
|------|--------------|
| **Centralized System** | All data and computation reside in a single central location (e.g., one main server). |
| **Distributed System** | Data and computation are spread across multiple servers (nodes) or locations, connected via a network. |

---

### 🏗️ Common Distributed System Architectures

#### 1. **Client-Server Architecture**
- The **server** provides resources or services.  
- The **client** requests those services over a network.  
- Example: A web browser (client) making requests to a web server.

#### 2. **Three-Tier Architecture**
- Divides the system into **Presentation**, **Application**, and **Database** layers.  
- Improves modularity and scalability.

#### 3. **Microservices Architecture**
- Splits the application into **small, independent services**, each handling a specific business function.  
- Services communicate via **APIs** or **message queues**.  
- Enables independent scaling, deployment, and updates.

#### 4. **Event-Driven Architecture**
- Operates through **events** rather than direct requests.  
- Services **emit events** and **respond** to them asynchronously.  
- Useful for real-time systems like notifications, order tracking, or IoT.

---

### 🧠 Key Insight
> A distributed system brings **scalability**, **fault tolerance**, and **availability** — but at the cost of **complexity** and **data consistency challenges**.

---

## 🧾 Summary Comparison

| Feature | Monolithic | Distributed |
|----------|-------------|--------------|
| **Structure** | Single application | Multiple nodes/services |
| **Scalability** | Vertical (scale-up) | Horizontal (scale-out) |
| **Deployment** | Single unit | Multiple servers |
| **Fault Tolerance** | Low | High |
| **Maintenance** | Hard for large systems | Easier with decoupled components |
| **Example** | Traditional web app | Cloud-native, microservices-based apps |

---

> 💡 **Tip:**  
> Start with a **monolith** if you're building an MVP.  
> Move toward a **distributed or microservices architecture** as your system grows in complexity and scale.
