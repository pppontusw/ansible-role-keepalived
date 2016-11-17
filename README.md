# keepalived

## What does it do?

1. Installs keepalived
2. Configures according to variables

```
# interface to bind to
keepalived_iface: eth0

# must be unique for each host and the master should have the highest number
keepalived_priority: 100

# a secure password for keepalived comms
keepalived_auth_pass: "{{vault_keepalived_auth_pass}}"

# the virtualIP to assign to keepalived
keepalived_virtualip: 172.32.1.24

# instance group name
keepalived_instance: VI_1

#processes to monitor (using pidof) - if your process names vary by distribution define this variable separately instead or in vars/Debian & vars/Redhat
#keepalived_type: 
  #- nginx 
  #- haproxy
```