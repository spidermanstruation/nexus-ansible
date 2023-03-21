# Nexus

Ansible playbook for deploying Sonatype Nexus OSS 3

## Roles variables

Descritions and default values are given in file [roles/defaults/main.yml](roles/nexus/defaults/main.yml)

## Run ansible playbook

Deploy Nexus on the host
```shell
   export HOSTS=${HOSTS}
   ansible-playbook -i inventories/${HOSTS}/hosts nexus-deploy.yml --diff
```
Deploy HAProxy

```shell
   export ANSIBLE_HASHI_VAULT_ADDR=${VAULT_ADDR}
   export ANSIBLE_HASHI_VAULT_TOKEN=${VAULT_TOKEN}
   ansible-playbook -i inventories/${HOSTS}/hosts haproxy.yml -u ${SSH_LOGIN} --diff

```

## Dependencies

Docker must be installed to use this role
