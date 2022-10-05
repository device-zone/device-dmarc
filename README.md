# device-opendmarc
Provides an OpenDMARC appliance.

This appliance does the following:

- All parameters passed to the device commands are syntax checked and canonicalised, with bash completion.
- Automatically configures OpenDMARC's configuration files before startup.
- Binds securely to the unix domain socket /run/opendmarc/opendmarc.sock.
- Enables enforcement of email DMARC policies.
- Autostarts on server restart.
- Zero Trust configuration.

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


