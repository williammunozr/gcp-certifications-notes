# Sole Tenancy

- There may be times when you do not want virtual machines from other projects running on the same server as your project's virtual machines.
- With `Sole Tenancy`, only VMs from your project with `node affinity` labels matching the labels you specify here will run on the same server together.
- We also have the option of over-committing the CPUs on a server that is configured as sole tenant.