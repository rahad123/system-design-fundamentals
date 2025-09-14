# 📚 What is System Design?

System Design is the process of defining the **architecture, components, modules, interfaces, and data** of a system to satisfy specified requirements.  

It’s similar to creating a **blueprint for a building** before the construction begins.

---

## 🎯 Goals of System Design

A well-designed system should be:

- **Scalable** → Can handle growth in users, data, or traffic.  
- **Reliable** → Works correctly and consistently, even under failures.  
- **Available** → Operational and accessible most of the time (e.g., "99.9% uptime").  
- **Efficient** → Performs with low latency and high throughput.  
- **Maintainable** → Easy to update, modify, and extend over time.  

👉 Achieving these goals requires making **thoughtful trade-offs**  
(e.g., consistency vs. availability, latency vs. cost).

---

## 🏗️ Levels of System Design

### 1. High-Level Design (HLD)
A **macro-level** view of the system architecture.  

**Focus:**  
- Overall system structure and main components (services, databases, caches).  
- How components interact with each other.  
- Technology choices and key trade-offs.  

**Answers:**  
- **What** the system looks like.  
- **Why** certain choices are made.  

**Purpose:**  
To create a blueprint understandable by **architects, managers, and stakeholders**, ensuring it meets both business and technical requirements.

---

### 2. Low-Level Design (LLD)
A **micro-level** view of each module or component.  

**Focus:**  
- Detailed logic, data structures, and APIs.  
- Class diagrams, database schemas, and interface specifications.  

**Answers:**  
- **How** each part will be built and function.  

**Purpose:**  
To provide developers with a **step-by-step guide** for implementation.

---

## 📝 Workflow

1. **Start with HLD** → Define the system at a high level.  
2. **Move to LLD** → Break down each component with implementation details.  
3. **Implementation** → Use the LLD as a blueprint to write code.  

---

## 💡 Summary
System Design bridges the gap between **requirements** and **implementation**, ensuring that software systems are:  
- Well-structured  
- Scalable  
- Reliable  
- Efficient  
- Easy to maintain over time
