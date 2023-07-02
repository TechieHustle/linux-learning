There can be different type of init system for Linux machines.
To find out the init system, following commands can be used:
1. `stat /sbin/init` or `pstree`


#### Logs:
- Output of the service goes to `syslog`: `/var/log/syslog`
- Or can be checked using command: `journalctl -u <service-name>`
- 

## systemd unit:
It's the basic entity, as a representation of service or system resources that systemd can manage. Some popular Unit types are:
- Service: Long running services, like servers
- Socket:  Socket files for network connections
- Device:  Hardware device on the machine.
- Target:  Unit groups representing system state.
- Timer:   Tasks scheduled at intervals (like cron).
- Mount Point: Mount points on the machine
- Swap file: Files used as swap

NOTE: To list units of a specific type `list-unit-files` can be used. For example, all the units of mount type can be listed using command:  
`systemctl list-unit-files --type mount`

## Location of systemd files:
- `/lib/systemd/system/`: Pre-installed by linux distros.
- `/run/systemd/system/`: Run time related units.
- `/usr/lib/systemd/system/`: Unit files from the packages.
- `/etc/systemd/system/`: Unit files manually created by users. Highest priority of parsing. The order of parsing is `/etc/`, `/run/`, `/lib/`. So any customizations of a unit file should be done in `/etc/`.

- 
