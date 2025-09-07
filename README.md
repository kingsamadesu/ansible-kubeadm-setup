## Requirements
* Operating System
> Supported operating systems: Ubuntu 18.04 and later.

* Network

> Ensure that the necessary network ports are open between the nodes, following the official Kubernetes [network Requirements](https://kubernetes.io/docs/reference/networking/ports-and-protocols/).

## To RUn the playbook 
```bash
ansible-playbook -i hosts playbooks/main-ec2-aws.yaml
```


**Keep in mind** there is no loadbalancer to split load between master nodes.
the playbook will take the first master node in the inventory file **hosts** as the main master node to use to join other remaining nodes.
```yaml
[master-group]
54.210.131.36 
54.88.48.53
54.172.121.45
[worker-group]
54.152.130.167
```

