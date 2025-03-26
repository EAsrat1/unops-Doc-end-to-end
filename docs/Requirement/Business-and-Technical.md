# Business and Technical requirements

## Development Environment Required Resources

To complete the development tasks, the following resources will be required:

The development resources are permanent and are required not only for the initial development and testing phases but also for ongoing maintenance. These resources will support future upgrades, patching, troubleshooting, and continuous improvement efforts, ensuring the environment remains robust, secure, and aligned with evolving business requirements. Additionally, they will facilitate the development of new features, integration testing, and performance optimization over time

|                               | Quantity      | Specification    |   OS        |  Note            |  Storage              |
| ----------------------------- | ------------- | ---------------- | ------------| ---------------- |  ---------------------|
| `Moodle application server`   | :3            |:8vCPUS | 32GB    |:Ubuntu-22004|                  |:Shared Storage (120GB)|
| `Database Server ( Service)`  | :2            |:min 16vCore|128GB|             |:u7i              |                       |
| `JumpBox/Ansible server`      | :2            |:16 vCPUs | 64GB  |:MySQL 8.0.28|:1 R/W and1 R-Only|:200GB                 |

## Production-Ready Test Environment Requirements

The following resources are needed for a duration of two months and will be decommissioned once the production-ready environment testing is completed.


## Production Environment Requirements

The production environment resources are fully utilized during exam (peak) periods, while certain resources can be scaled down or decommissioned during idle times to optimize costs and efficiency.
