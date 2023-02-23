# Compute Engine Machine Family

## Machine Group Types

- Standard types.
- High-memory machines.
- High-CPU machines.
- Shared core type.
- Memory-optimized machines.
- Custom machine type.

## Different Machine Families for Different Workloads

- General Purpose (E2, N2, N2D, N1):
    - Best price-performance ratio.
    - Web application servers, small-medium databases, dev environments.
- Memory Optimized (M2, M2):
    - Ultra high memory workloads
    - Large In-Memory databases and In-Memory analytics.
- Compute Optimized (C2):
    - Compute intensive workloads.
    - Gamming applications.

## Custom Machine Type

- Set the number of `Cores`.
- Set the number of `Memory`.
- The price of a custom configuration is based on the number of `vCPUs` and `Memory` allocated.

## Use Cases for Compute Engine Virtual Machines

- Good option when you need maximum control over VM instances.
- Choose the specific image to run on the instance.
- Install software packages or custom libraries.
- Have fine-grained control over which users have permissions on the instance.
- Have control over SSL certificates and firewall rules for the instance.