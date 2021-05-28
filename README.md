# Project-1

The files that are provided in this repo were used to configure the network that is shown in the image below.

#<img src = "Images/">

All of the files were tested and utilized in order to create a live ELK deployment on Azure and by doing so, they can recreate the network above. Filebeat was installed and used as a portion of the playbook file.

#insert filebeat-playbook.yml

The following will be described:
- Topology Description
- Access Policies
- ELK Configuration
  - Beats Used
  - Monitored Machines
- Using Ansible


# Topology Description
The goal of this network was to expose the a load-balanced Damn Vulnerable Web Application (DVWA) and have the exposed DVWA instances be monitored as well. 

Using a load-balancer ensures that the application would be available for an "attack" but also ensures that outside ip addresses can't gain access. The load-balancer is able to do this because they protect the servers by distributing traffic amongst the servers that are available. In combination, the load-balancer and jump box together enables a layer of protection for the virtual machines (VMs) from public exposure.

Adding an ELK server into the combination enables a monitoring system for the VMs to visualize any changes that might occur to the log files and system performance, making it a better method of discovering an "attack" by analyzing any changes in these logs. This is where Filebeat comes into play as the monitoring system.

Below is a list of the machines in the network that were configured and used as well as the applications used.
| Name                 | Function         | IP Adddress | Operating System |        
|----------------------|------------------|-------------|------------------|      
| jump-box-provisioner | Gateway          | 10.0.0.5    | Linux            |
| web-1                | Container VM     | 10.0.0.6    | Linux            |
| web-2                | Container VM     | 10.0.0.7    | Linux            |
| elk-server           | Kibana Container | 10.1.0.4    | Linux            |


| Name       |
|------------|
| Docker     |
| Filebeat   |
| Metricbeat |
| Ansible    |

