## ⚙️ Part 2: Scaling – Horizontal vs Vertical

### ✅ What I Learned

- **Scaling** is the ability of a system (like a web app) to handle increasing load.
- There are two primary types of scaling:

#### 1. Vertical Scaling (Scale Up)
- Upgrading to a **larger/more powerful machine**.
- Example: Move from a 2-core to 16-core VM.
- Pros: Simple to implement.
- Cons: Hardware limits, possible downtime.

#### 2. Horizontal Scaling (Scale Out)
- Adding **more machines or VMs** to share the load.
- Example: Instead of 1 VM, use 10 small VMs with a load balancer.
- Pros: More scalable and fault-tolerant.
- Cons: More complex setup (stateless design, distributed systems).

---

### 🌍 Real-World Cloud Example (Azure)

> Suppose I have a website hosted on Azure, and millions of users send requests.

- If one VM can't handle it:
  - I can **vertically scale** by upgrading the VM.
  - Or **horizontally scale** by adding more VMs or capacity units.
- **Azure provides**:
  - Virtual Machines, Load Balancers, Regions, Global Distribution
  - It’s like having a computer in the cloud, on-demand.

---

### 🔄 Load Balancer’s Role in Horizontal Scaling

- Distributes user traffic across multiple instances.
- Improves performance and reliability.
- Supports regional routing (global users = global distribution).

---

### ⚠️ Key Consideration: Loosely Coupled Architecture

- In horizontal scaling, **each instance must be independent**.
- Avoid tight coupling (like local-only state).
- Use **shared storage, cloud databases, or distributed caching** (e.g., Redis, CosmosDB).
