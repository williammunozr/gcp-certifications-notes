# Networking Services

## Virtual Private Cloud (VPC)

- `Virtualized network` within Google Cloud.
- `Core networking` service.
- `Global resource`.
- Each VPC contains a `default network`.
- Additional networks can be created in your project, but `networks cannot be shared` between projects. 

## Firewall Rules

- Govern traffic coming into instances on a network.
- The Default network has a default set of firewall rules.
- Custom rules can be created.

## Routes

- Advanced networking functions for your instances.
- Specifies how packets leaving an instance should be directed.

## Load Balancing

Distributing Workloads across multiple instances 

- HTTP(S) Load Balancing

Distribute traffic across regions to ensure that requests are routed to the closest region or, in the event of a failure or over-capacity, to a healthy instance in the next closest region.
Distribute traffic based on the content type.

- Network Load Balancing

Distribute traffic among server instances in the same region based on incoming IP protocol data, such as an address, port, and protocol.

## Google Cloud DNS

- Publish and maintain DNS records by using the same infrastructure that Google uses.
- Work with managed zones and DNS records through the CLI, API, or SDK 

## Cloud VPN

- Connect your existing network to your VPC through an IPsec connection. 

## Direct Interconnect

- Connect an existing network to your VPC using a highly available, low-latency, enterprise-grade connection. 

## Direct Peering

- Exchange internet traffic between your business network and Google at one of Google's broad-reaching edge network locations.

## Carrier Peering

- Connect your infrastructure to Google's network edge through highly available, lower-latency connections by using service providers.
