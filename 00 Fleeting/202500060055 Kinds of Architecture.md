# Kinds of Architecture

1. Shared-Memory Architecture
   - Multiple CPUs, RAM chips, disk are connected under a single operating system
   - A fast interconnect allow any CPU to access any part of the memory or disk
   - Scalability limit: Cost increase faster than linearly as more components are added
2. Shared-Disk Architecture
   - Each machine has its own CPU and RAM, but all machines share access to a common disk array
   - Machines are connected via a fast network
   - Scalability limit: Contention for disk access and the overhead of coordinating looks across machines limit scalability
3. Shared-Nothing Architecture
    - Each machine or virtual machine running its own instance of database software, referred to as a *node*
    - Each node uses its own CPUs, RAM and disk independently
    - Coordination: Any required coordination happens at the software level over a conventional network
    - Highly scalable and is commonly used in distributed databases and big data systems