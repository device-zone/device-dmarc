# device-opendmarc
Provides an OpenDMARC appliance.

This appliance does the following:

- Automatically configures OpenDMARC's configuration files before startup.
- Binds securely to the unix domain socket /run/opendmarc/opendmarc.sock.
- Enables enforcement of email DMARC policies.
- Autostarts on server restart.

## before

- Deploy the device-opendmarc package.

```
[root@server ~]# dnf install device-opendmarc
```

## enable

To switch the appliance on, run this.

```
[root@server ~]# device services mail smtp dmarc enable 
```

## disable

To switch the appliance off, run this.

```
[root@server ~]# device services mail smtp dmarc disable  
```


