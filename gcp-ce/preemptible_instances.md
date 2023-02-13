# Preemptible Instances

Preemptible VM instances are a kind of compute resource that function like normal instances but have some limitations. The use case of preemptible instances is when the application is fault-tolerant and can withstand possible instance preemptions. Preemptible VM instances are available at much lower price --a `60-91% discount`-- compared to the price of standard VMs.

## Limitations

- Compute Engine might stop preemptible instances at any time due to system events.
- Compute Engine always stops preemptible instances after they run for 24 hours.
- Preemptible instances are finite Compute Engine resources.
- Preemptible instances can't live migrate to a regular VM instance.
- Preemptible instances are not covered by any Service Level Agreement and are excluded from the Compute Engine SLA.
- The Google Cloud Free Tier credits for Compute Engine do not apply to preemptible instances.

