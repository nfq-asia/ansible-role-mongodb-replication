# Ansible Mongodb Replication

## Requirement

Edit mongodb_version in defaults/main.yml or in the mongdb.yml playbook to install a specific version

## Role Variables

```
mongodb_version: "4.0"
mongodb_replica_set_name: "standard-replication"
mongodb_replica_set_enable_majority_read_concern: "true"

admin_password: changeit123
admin_roles: dbAdminAnyDatabase
users:
  devops:
    database: admin
    password: changeit123
    roles: dbAdmin
    state: present

mongodb_conf_template: mongod.conf.j2
mongodb_logrotate_conf_template: mongodb_logrotate.conf.j2
mongodb_logfile: /var/log/mongodb/mongod.log
mongodb_authorization: disabled
```
