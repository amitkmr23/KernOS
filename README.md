# Operating System Kernel

A custom operating system kernel implementing core OS concepts including **CPU scheduling, system calls, exception handling, virtual memory, process management, inter-process communication, synchronization, and file systems**.

## 🚀 Overview

This project focuses on implementing fundamental operating-system abstractions from the kernel level, with emphasis on **process scheduling, memory management, system calls, IPC, synchronization, and storage I/O**.

The kernel provides low-level mechanisms for managing CPU execution, virtual memory, processes, synchronization primitives, and persistent storage.

## ✨ Key Features

### ⚙️ CPU Scheduling & Process Management

* Implemented **Round-Robin CPU scheduling** for fair process execution.
* Added custom **system calls** for kernel–user space interaction.
* Implemented **exception handling** for processor-level faults and interrupts.
* Built process management mechanisms for controlling process execution and state.

### 🧠 Memory Management

* Implemented **4-level page tables** for virtual-to-physical address translation.
* Developed **page-table walking** for resolving virtual memory mappings.
* Implemented `mmap`-style memory mapping functionality.
* Added **Copy-on-Write (COW) fork** to efficiently duplicate process address spaces.
* Managed page permissions and memory mappings at the kernel level.

### 🔄 IPC & Synchronization

* Implemented **semaphores** for process/thread synchronization.
* Developed **wait queues** for blocking and waking processes.
* Added **circular trace buffers** for efficient kernel event tracing and coordination.
* Provided synchronization mechanisms for concurrent kernel operations.

### 💾 File System & Storage

* Developed a layered **file-system architecture**.
* Implemented **file descriptors** for process-level file management.
* Added **block allocation** for storage management.
* Implemented storage-related **I/O system calls**.
* Integrated file operations with the underlying storage layer.

## 🏗️ Architecture

```text
                User Programs
                     │
                     ▼
             ┌───────────────┐
             │ System Calls  │
             └───────┬───────┘
                     │
        ┌────────────┼────────────┐
        ▼            ▼            ▼
   Process Mgmt   Memory Mgmt   File System
        │            │            │
        ▼            ▼            ▼
   Round-Robin   Page Tables   File Descriptors
   Scheduling    Page Walking  Block Allocation
   Exceptions    MMAP / COW    Storage I/O
        │            │            │
        └────────────┼────────────┘
                     ▼
             ┌───────────────┐
             │ Kernel Core   │
             └───────┬───────┘
                     │
                     ▼
                Hardware
```

## 🛠️ Technical Concepts

* Operating System Kernels
* Process Management
* CPU Scheduling
* Round-Robin Scheduling
* System Calls
* Exception Handling
* Virtual Memory
* 4-Level Page Tables
* Page-Table Walking
* `mmap`
* Copy-on-Write
* `fork`
* Inter-Process Communication
* Semaphores
* Wait Queues
* Circular Buffers
* File Systems
* File Descriptors
* Block Allocation
* Storage I/O

## 📁 Major Kernel Components

```text
kernel/
├── process/
│   ├── scheduler
│   ├── process management
│   └── exception handling
│
├── memory/
│   ├── page tables
│   ├── page-table walker
│   ├── mmap
│   └── copy-on-write
│
├── ipc/
│   ├── semaphores
│   ├── wait queues
│   └── trace buffers
│
├── filesystem/
│   ├── file descriptors
│   ├── block allocation
│   └── storage I/O
│
└── syscalls/
    └── kernel-user interfaces
```

> **Note:** The directory structure above is a conceptual organization. Update it to match the actual repository structure.

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

* Kernel-level programming and low-level systems development
* CPU scheduling and process lifecycle management
* Virtual memory and address translation
* Page-table manipulation and memory protection
* Process creation using `fork` and Copy-on-Write
* Synchronization and concurrent execution
* Inter-process communication mechanisms
* File-system internals and storage management
* Designing interfaces between user space and kernel space

## 🔧 Build & Run

Clone the repository:

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_NAME>
```

Build the kernel using the project's build system:

```bash
make
```

Run using the configured emulator:

```bash
make run
```

> Update the commands above according to the actual build/run instructions of the project.

## 📌 Project Highlights

| Subsystem           | Implementation                 |
| ------------------- | ------------------------------ |
| CPU Scheduling      | Round-Robin                    |
| System Interface    | Custom System Calls            |
| Exceptions          | Kernel Exception Handling      |
| Virtual Memory      | 4-Level Page Tables            |
| Address Translation | Page-Table Walking             |
| Memory Mapping      | MMAP                           |
| Process Creation    | Fork + Copy-on-Write           |
| Synchronization     | Semaphores + Wait Queues       |
| IPC                 | Kernel Coordination Mechanisms |
| Tracing             | Circular Trace Buffers         |
| File System         | Layered File System            |
| Storage             | Block Allocation + Storage I/O |

## 📚 Concepts Demonstrated

This project demonstrates practical understanding of **Operating Systems, Computer Architecture, Memory Management, Concurrency, IPC, File Systems, and low-level systems programming**.
