# Business and Technical requirements

## Development Environment Required Resources

To complete the development tasks, the following resources will be required:

The development resources are permanent and are required not only for the initial development and testing phases but also for ongoing maintenance. These resources will support future upgrades, patching, troubleshooting, and continuous improvement efforts, ensuring the environment remains robust, secure, and aligned with evolving business requirements. Additionally, they will facilitate the development of new features, integration testing, and performance optimization over time

|                                    | Quantity      | Specification     |   OS        |  Note             |  Storage              |
| ---------------------------------- | ------------- | ----------------- | ------------| ----------------- |  ---------------------|
| `Moodle application server`        | 3             |:8vCPUS | 32GB     |:Ubuntu-22004|                   |:Shared Storage (120GB)|
| `Catching Service`                 | 1             |:min 16vCore|128GB |             | u7i               |                       |
| `Database Server ( Service)`       | 2             |16vCore |64GB      |MySQL 8.0.28 |1 R/W and 1 R-Only | 200 GB                | 
| `JumpBox/Ansible server`           | 1             |:8vCPUS | 32GB     |             |                   |                       |
| `Elastic IP`                       | 5             |1000 Mbits/s    dedicated band width                 |                       |
| `Elastic Load Balancer`            | 1             |10 Bandwidth size  |             |                   |                       |
|`Domain Name and signed certificate`|               |                   |             |For Each server  FQDN Name                 |
| `WAF`                              | 1             |WI-500             |waf.8u16g    |8 vCPUs | 16 GB    |                       |

Note: Do we have a CLI (KooCLI) software that we can access using the command line interface  and REST API.



## Production-Ready Test Environment Requirements

The following resources are needed for a duration of two months and will be decommissioned once the production-ready environment testing is completed.


## Production Environment Requirements

The production environment resources are fully utilized during exam (peak) periods, while certain resources can be scaled down or decommissioned during idle times to optimize costs and efficiency.
