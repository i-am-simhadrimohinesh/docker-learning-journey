# 🐳 1.2 Virtualization

---

# 🏢 Physical Servers

Before virtualization, applications ran directly on physical machines 🖥️.

---

## ⚙️ Problem with Physical Servers

- One OS per machine
- Low hardware utilization
- Difficult scaling
- Expensive infrastructure 💸

---

## 📊 Traditional Setup

```mermaid
flowchart LR
A[Physical Server 1] --> App1[App]
B[Physical Server 2] --> App2[App]
C[Physical Server 3] --> App3[App]
```

👉 One machine = One application (wasteful)

---

# ⚙️ What is Virtualization?

Virtualization is a technique that allows **multiple virtual machines to run on a single physical machine**.

👉 It improves hardware utilization and flexibility.

---

## 🧠 Core Idea

```mermaid
flowchart TD
A[Physical Machine] --> B[Hypervisor]
B --> C[VM 1]
B --> D[VM 2]
B --> E[VM 3]
```

---

# 🧠 Hypervisors

A **Hypervisor ⚙️** is software that creates and manages Virtual Machines (VMs).

It allows multiple operating systems to run on the same hardware.

---

# 💻 Virtual Machines (VMs)

A Virtual Machine is a **software-based computer** that behaves like a real computer.

---

## 📦 Each VM has:

- Own OS 🖥️
- Own kernel 🧠
- Own memory & CPU allocation ⚙️
- Fully isolated environment 🔒

---

## 📊 VM Architecture

```mermaid
flowchart TD
A[Hardware] --> B[Hypervisor]
B --> C[VM 1 - Linux]
B --> D[VM 2 - Windows]
B --> E[VM 3 - Linux]
```

---

# 🔢 Types of Hypervisors

---

## 🟢 Type 1 Hypervisor (Bare Metal)

Runs directly on hardware 🖥️

### Examples:
- VMware ESXi
- Microsoft Hyper-V
- Xen

### 📊 Structure:

```mermaid
flowchart TD
A[Hardware] --> B[Type 1 Hypervisor]
B --> C[VMs]
```

### ✅ Advantages:
- High performance ⚡
- Secure 🔒
- Direct hardware access

---

## 🔵 Type 2 Hypervisor (Hosted)

Runs on top of an operating system 💻

### Examples:
- VirtualBox
- VMware Workstation

### 📊 Structure:

```mermaid
flowchart TD
A[Hardware] --> B[Host OS]
B --> C[Type 2 Hypervisor]
C --> D[VMs]
```

### ❌ Limitations:
- Slower than Type 1
- Extra OS overhead

---

# ✅ Advantages of Virtualization

- 🧠 Better resource utilization
- 💰 Cost savings
- 🔒 Strong isolation
- ⚙️ Multiple OS on same machine
- 📦 Easy backup and recovery

---

# ❌ Limitations of Virtualization

- 🪨 Heavy (each VM has full OS)
- ⏳ Slow boot time
- 💾 High memory usage
- ⚡ Lower performance compared to containers

---

# 🧠 Key Insight

👉 Virtualization = Multiple OS on same hardware  
👉 But each OS is heavy and resource-consuming

---

# 📚 Summary

Virtualization solves physical server limitations by introducing hypervisors and virtual machines.

However, VMs are still heavy, which later leads to the need for **containers (Docker)**.

---

# 🎯 Final Flow

```mermaid
flowchart TD
A[Physical Server Problem] --> B[Virtualization]
B --> C[Hypervisor]
C --> D[Virtual Machines]
D --> E[Better Utilization]
E --> F[But Still Heavy]
F --> G[Need for Containers 🚀]
```

---