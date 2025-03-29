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


<table>
    <tr>
        <th>Resources</th>
        <th colspan="3" style="text-align:center;">Specification</th>
        <th>Notes</th>
    </tr>
    <tr>
        <td></td>
        <td>Quantity</td>
        <td>vCore</td>
        <td>Memory (GB)</td>
        <td></td>
    </tr>
    <tr>
        <td>Moodle Web Server</td>
        <td>70 - 100</td>
        <td>16 - 64</td>
        <td>64 - 128</td>
        <td>Ubuntu-22004</td>
    </tr>
    <tr>
        <td>RDS</td>
        <td>14 - 20</td>
        <td>32 - 64</td>
        <td>128 - 256</td>
        <td>PostgreSQL</td>
    </tr>
    <tr>
        <td> ELB </td>
        <td>7 - 10</td>
        <td colspan="2" style="text-align:left;">Enhanced Load Balancer/Dedicated LB which can handle up to 100k Concurrent connection</td>
        <td>One redundant, Auto-failover  elastic load balancer is required</td>
    </tr>
    <tr>
        <td>Caching Service </td>
        <td>7 - 10</td>
        <td>16 - 64</td>
        <td>128 - 256</td>
        <td>Each Cluster will have one dedicated Caching Service</td>
    </tr>
    <tr>
        <td> Elastic IP</td>
        <td>8 - 11</td>
        <td colspan="2" style="text-align:left;">1000 Mbits/s Dedicated BW</td>
        <td></td>
    </tr>
    <tr>
        <td>VPC </td>
        <td>1</td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>Ansible Server</td>
        <td>1</td>
        <td>16 - 32</td>
        <td>64 - 128</td>
        <td></td>
    </tr>
     <tr>
        <td>JumpServer</td>
        <td>1</td>
        <td>16 - 32</td>
        <td>64 - 128</td>
        <td></td>
    </tr>
    <tr>
        <td> WAF Service</td>
        <td>7-10</td>
        <td colspan="2" style="text-align:left;">WI-500</td>
        <td>If a single WAF instance cannot handle the maximum concurrent connections, additional WAF instances can be added, with traffic load balanced between them</td>
    </tr>
    <tr>
        <td>Domain Name  Service and  signed certificate</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>IAM Service</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>



## Production Environment Requirements

The production environment resources are fully utilized during exam (peak) periods, while certain resources can be scaled down or decommissioned during idle times to optimize costs and efficiency.

<table>
    <tr>
        <th>Resources</th>
        <th colspan="3" style="text-align:center;">Specification</th>
        <th>Notes</th>
    </tr>
    <tr>
        <td></td>
        <td>Quantity</td>
        <td>vCore</td>
        <td>Memory (GB)</td>
        <td></td>
    </tr>
    <tr>
        <td>Moodle Web Server</td>
        <td>70 - 100</td>
        <td>16 - 64</td>
        <td>64 - 128</td>
        <td>Ubuntu-22004</td>
    </tr>
    <tr>
        <td>RDS</td>
        <td>14 - 20</td>
        <td>32 - 64</td>
        <td>128 - 256</td>
        <td>PostgreSQL</td>
    </tr>
    <tr>
        <td> ELB </td>
        <td>7 - 10</td>
        <td colspan="2" style="text-align:left;">Enhanced Load Balancer/Dedicated LB which can handle up to 100k Concurrent connection</td>
        <td>One redundant, Auto-failover  elastic load balancer is required</td>
    </tr>
    <tr>
        <td>Caching Service </td>
        <td>7 - 10</td>
        <td>16 - 64</td>
        <td>128 - 256</td>
        <td>Each Cluster will have one dedicated Caching Service</td>
    </tr>
    <tr>
        <td> Elastic IP</td>
        <td>8 - 11</td>
        <td colspan="2" style="text-align:left;">1000 Mbits/s Dedicated BW</td>
        <td></td>
    </tr>
    <tr>
        <td>VPC </td>
        <td>1</td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>Ansible Server</td>
        <td>1</td>
        <td>16 - 32</td>
        <td>64 - 128</td>
        <td></td>
    </tr>
     <tr>
        <td>JumpServer</td>
        <td>1</td>
        <td>16 - 32</td>
        <td>64 - 128</td>
        <td></td>
    </tr>
    <tr>
        <td> WAF Service</td>
        <td>7-10</td>
        <td colspan="2" style="text-align:left;">WI-500</td>
        <td>If a single WAF instance cannot handle the maximum concurrent connections, additional WAF instances can be added, with traffic load balanced between them</td>
    </tr>
    <tr>
        <td>Domain Name  Service and  signed certificate</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>IAM Service</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>

### Production Resource Management :


#### Dynamic Scaling of Moodle Application Servers:

During peak periods, all 7 to 10 application servers per cluster will remain active to handle high user loads.
During idle or non-peak times, application servers will be scaled down to 2 servers per cluster, reducing resource consumption while maintaining service availability.

#### Leveraging Auto-Scaling Services:

If Ethio-Telecom offers an auto-scaling service, it will be integrated with the Elastic Load Balancer (ELB) to dynamically allocate and decommission application servers based on real-time demand.
In the absence of an auto-scaling feature, the scaling process will be managed manually or through orchestration tools like Ansible, ensuring efficient deallocation and decommissioning of resources.

#### Resource Decommissioning:

Excess Moodle application servers will be shut down and deallocated automatically or manually during non-peak times, leveraging Ansible for seamless scaling.

#### Elastic Load Balancer and WAF Flexibility:

The ELB will maintain load balancing with auto-failover capabilities, while WAF instances will scale to handle concurrent connections as needed.

#### Caching and Database Services:

Caching services and database instances will maintain consistent performance, with caching clusters scaled based on the active application server count.

#### Ansible Server and Jump Server Utilization:

The Ansible Server will manage configuration and deployment tasks, while the Jump Server will ensure secure administrative access, both running at minimal capacity during idle times.
Outcome:
This cost optimization strategy will enable the environment to dynamically adapt to workload changes, minimizing costs while maintaining performance and availability. The integration of Ethio-Telecom's auto-scaling service (if available) will further automate resource management, contributing to operational efficiency and reducing the total cost of ownership (TCO).

