# clusterpi-ansble
Ansible config for ClusterPi

## Running playbook(s)

### baseline-setup

```bash
ansible-playbook -u {ssh USER} baseline-setup.yml
-or-
ansible-playbook -i hosts.yml -u {ssh USER} baseline-setup.yml
```

### deb-update

```bash
ansible-playbook -u {ssh USER} deb-update.yml
-or-
ansible-playbook -i hosts.yml -u {ssh USER} deb-update.yml
```

### cluster

```bash
ansible-playbook -u {ssh USER} cluster.yml
-or-
ansible-playbook -i hosts.yml -u {ssh USER} cluster.yml
```
