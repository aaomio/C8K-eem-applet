# C8K EEM Applets

A collection of Cisco Catalyst 8000V (C8KV) **Embedded Event Manager (EEM)** applets demonstrating event-driven automation with Cisco IOS XE.

## EEM Applets

### Interface Re-Enable

Automatically detects an interface going down and attempts to recover it.

* [Configuration](./config/int_re_enable.cfg)
* [Output](./Screengrabs/int_re_enable.png)

### Hourly Backup

Periodically backs up the running configuration to flash.

* [Configuration](./config/hourly_backup.cfg)
* [Output](./Screengrabs/hourly_backup.png)

### Daily Backup

Creates a scheduled backup of the running configuration.

* [Configuration](./config/daily_backup.cfg)
* [Output](./Screengrabs/daily_backup.png)

### Configuration Change by User

Detects configuration changes and extracts the user associated with the change.

* [Configuration](./config/by_user.cfg)
* [Output](./Screengrabs/by_user.png)

### No Erase

Demonstrates EEM automation associated with an erase operation.

* [Configuration](./config/no_erase.cfg)
* [Output](./Screengrabs/no_erase.png)

## Embedded Event Manager

**Embedded Event Manager (EEM)** provides event-driven automation within Cisco IOS XE.

EEM monitors events and executes configured actions when a matching event occurs.

Actions can execute CLI commands, generate syslog messages, process variables, and perform automated configuration or monitoring tasks.

## Verifying EEM

### Display Registered Policies

```cisco
show event manager policy registered
```

Displays the EEM policies currently registered on the device.

### Display Detailed Policy Information

```cisco
show event manager policy registered detailed <policy-name>
```

Displays detailed information about a registered EEM policy.

### Display EEM Configuration

```cisco
show running-config | section event manager
```

Displays the EEM configuration from the running configuration.

### Display EEM Event History

```cisco
show event manager history events
```

Displays the history of EEM events and can be useful when troubleshooting an applet that is not triggering or completing correctly.


## Catalyst 8000V and GNS3

The EEM applets in this repository can be tested using a **Cisco Catalyst 8000V (C8KV)** virtual router in GNS3.

- [GNS3 Setup](./GNS3.md)



