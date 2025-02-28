##Getting started with Ansible-Playbooks
If you want to run ansible playbook i.e camel-rhel-customize.yml manually then make sure that you have installed ansible  on your system where you want to run.
To  install ansible you need to register for subscription-manager prior to that.

##Fallow the below steps for subscription-manager
```bash
# Check the subscription-manager status
subscription-manager refresh
# If it's not subscribed then run the below command
subscription-manager register --username $RH_SUBS_USERNAME --password $RH_SUBS_PASSWORD --auto-attach
```


##Install ansible and required dependencies

```bash
yum install ansible-core -y
ansible-galaxy collection install ansible.posix
```


##Run the playbook
```bash
ansible-playbook -i host.yml camel-rhel-customize.yml
```
