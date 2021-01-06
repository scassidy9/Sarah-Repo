## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

! [https://github.com/scassidy9/Sarah-Repo/blob/main/Images/Project_1_Diagram.png]

These files have been tested and used to generate a live ELK deployment on Azure.
They can be used to recreate the entire deployment pictured above. Alternatively, select portions of the *yml* or *config* file may be used to install only certain pieces of it, 
such as Filebeat.

  - _TODO:  - TODO Find ansible_playbook
- Test  
- ansible hosts
- ansible configuration
- ansible ELK installation and VM configuration
- ansible filebeat playbook
- ansible filebeat config file

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly monitored, in addition to restricting access to the network.
The off-loading function of the load balancer defends an organizaion against distributed denial-of-service attack. It does this by shifting traffic from the corporate server to a 
public cloud provider. 
Another level of security is a jump box. A jump box is a system on a network used to access and manage devices in a separate - generally remote - locations. They create separation between 
a users working area and the privileged assets within the network. A separation such as this keeps potentially compromised working areas free from direct contact of most valuable
information. 

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the *data* and *system* logs.
* *Filebeat* monitors the log files or locations that you specify, collects log events and send them to either Elasticsearch or Logstash for cataloging.
* *Metricbeat* takes the metrics and statistics that it collects and sends them to the output you that specify, such as Elasticsearch or Logstash.

The configuration details of each machine may be found below.

| Name              | Function       | IP Address     | Operating System |
|-------------------|----------------|----------------|------------------|
| Jump Box          | Gateway        | 40.78.21.200   | Linux            |
| Web1              | Web Server     | 10.0.0.7       | Linux            |
| Web2              | Web Server     | 10.0.0.8       | Linux            |
| Elk               | ELK Server     | 10.3.0.4       | Linux            |
| Load Balancer     | Load Balancer  | 104.45.228.210 | Linux            |
| Personal Computer | Access Control | External IP    | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet.

Only the *ELK Server* machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
* Personal Computer IP through TCP 5601

Machines within the network can only be accessed by the *Personal Computer and Jump Box*.
* Jump Box 40.78.21.200
* Personal Computer IP by port TCP 5601

A summary of the access policies in place can be found in the table below.

| Name          | Publicly Accessible | Allowed IP Address                |
|---------------|---------------------|-----------------------------------|
| Jump Box      | No                  | Personal Computer IP              |
| Web1          | No                  | 10.0.0.7                          |
| Web2          | No                  | 10.0.0.8                          |
| ELK Server    | No                  | Personal Computer using port 5601 |
| Load Balancer | No                  | Personal Computer on HTTP 80      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because *You do not have to separately set up$


The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.
! [https://github.com/scassidy9/Sarah-Repo/blob/main/Images/Docker_sweet_benz.png]


### Target Machines & Beats
This ELK server is configured to monitor the following machines:
* Web1 10.0.0.7
* Web2 10.0.0.8

We have installed the following Beats on these machines:
* ELK Stack, Web1 and Web2
* The Elk Stack installed is FileBeat

These Beats allow us to collect the following information from each machine:
 * FileBeat collects log events

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:

SSH into the control node and follow the steps below:
- Copy the Ansible ELK Installation file .
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:
* Which file is the playbook? Where do you copy it?
  * Ansible. 
* Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install FileBeat
  * 
* Which URL do you navigate to in order to check that the ELK server is running?
  *  http://13.68.239.154:5601/
