# Docker vs. Virtual Machines

[Back to the learning guide](../README.md)

Virtual machines run a guest operating system on virtualized hardware. Containers isolate application processes while sharing the host kernel. Containers are often quicker to start and more lightweight than a full VM, although actual resource use depends on the workload and platform.

| Topic | Container | Virtual machine |
|---|---|---|
| Operating system | Shares host kernel | Runs a guest OS |
| Typical startup | Fast | Slower because the guest OS boots |
| Packaging | Application and dependencies | Guest OS and applications |
| Isolation | Process and namespace based | Virtualized hardware boundary |

Containers and VMs can be used together. For example, Docker Desktop on some platforms runs its Linux environment inside a VM.

Next: [Port Mapping and Environment Variables](06-Ports-and-Environment-Variables.md).
