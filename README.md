An ansible playbook to install Cloud Monitoring plugins on the localhost.   This guide will not go into how to install ansible or git for your system.

Default command:

```ansible-playbook -i hosts <playbook>```

## Available playbooks 
- holland_mysqldump.yml
- mysql_slave.yml
- port_check.yml

## Examples
| Name | Examples
| ---------- | -------- |
| holland_mysqldump | `holland_mysqldump.yml`
| mysql_slave | `mysql_slave.yml`
| port_check | `port_check.yml -e port=8080` <br> `port_check.yml -e '{"host":"rackspace.com","port":"80"}'`

## Modifiers
You can edit the `group_vars/all` file if you want to change any of the defaults.  
- Notification Plan will default to npManaged, but you can change it to npTechnicalContactsEmail or any notification plan that is created for the account.

## References:
- [Rackspace Cloud Monitorin API - Agent Configuration File](http://docs.rackspace.com/cm/api/v1.0/cm-devguide/content/install-configure.html#agent-config-file)
- [Github for Cloud Monitoring Agent Plugins](https://github.com/racker/rackspace-monitoring-agent-plugins-contrib)
