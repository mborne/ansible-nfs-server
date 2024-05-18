# ansible-nfs-server

Ansible role deploying NFS server exposing a single export **for test purpose**. Note that it mainly aims at illustrating the use of [nfs-subdir-external-provisioner](https://github.com/kubernetes-sigs/nfs-subdir-external-provisioner?tab=readme-ov-file#kubernetes-nfs-subdir-external-provisioner).

## Role Variables

## Example Playbook

```yaml
---
- hosts: nfs_servers
  vars:
    nfs_host: '*'
  roles:
    - role: ansible-nfs-server
  tasks:
```

## License

[MIT](LICENSE)

## See also

* [galaxy.ansible.com - search - nfs-server](https://galaxy.ansible.com/ui/search/?keywords=nfs-server)
