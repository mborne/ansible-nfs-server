# ansible-nfs-server

Ansible role deploying NFS server exposing a single export **for test purpose**.

## Motivation

This repository mainly aims at illustrating the use of [nfs-subdir-external-provisioner](https://github.com/kubernetes-sigs/nfs-subdir-external-provisioner?tab=readme-ov-file#kubernetes-nfs-subdir-external-provisioner).

## Role Variables

See [defaults/main.yml](defaults/main.yml) :

| Name           | Description                     | Default          |
| -------------- | ------------------------------- | ---------------- |
| `nfs_data_dir` | Directory exposed by NFS server | `/var/nfs-data`  |
| `nfs_host`     | Allowed client IP range         | `192.168.0.0/16` |

## Example Playbook

```yaml
---
- hosts: nfs_servers
  vars:
    nfs_data_dir: '/var/nfs-data'
    nfs_host: '192.168.0.0/16'
  roles:
    - role: ansible-nfs-server
```

## License

[MIT](LICENSE)

## See also

* [galaxy.ansible.com - search - nfs-server](https://galaxy.ansible.com/ui/search/?keywords=nfs-server)
