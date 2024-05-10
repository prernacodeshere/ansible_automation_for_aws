
# Amazon Web Services Automation using Ansible

The Project is to create a fully functional automated pipeline using Ansible.

\
This project serves as a self learning to have a better understanding of Automation with Ansible. The project implements playbooks to create resources such as EC2 instances and EBS volumes. 

This also handles attachment, formatting and mounting and persisting the attached EBS Volume.

Post provisioning, this also handles deployment of the source code which happens to be a website in the created EC2 Instance. 

Along the way of this project, it uses:
1. Ansible
1. Amazon Web Services

## How to

### Pre-requisite

1. A working installation of ansible.
2. Amazon Web Services Account.
3. Access Keys and Secret Keys

### Deployment

The following playbooks must be executed in the given order:

```bash
[root@localhost ~]# ansible-playbook ec2_create.yml
[root@localhost ~]# ansible-playbook ebs_create.yml
[root@localhost ~]# ansible-playbook ebs_attach.yml
[root@localhost ~]# ansible-playbook storage.yml
[root@localhost ~]# ansible-playbook application_deployment.yml
```
