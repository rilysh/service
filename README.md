## service
A minimal script to manage services in Void Linux

## Usage
Use `service --help` for this info page.
```
Commands
    link [SERVICE]      - Link a service with current one
    unlink [SERVICE]    - Unlink a service from current one
    relink [SERVICE]    - Relink a service, if previous one is broken
    lnstat [SERVICE]    - Check service symbolic link status
    start [SERVICE]     - Start a service
    restart [SERVICE]   - Restart a service
    stop [SERVICE]      - Stop a service
    list                - List all currently linked services
```

## Info
Since Void uses runit, so it doesn't really have a separate service manager, like in SystemD, we've `systemctl`. All of it has an `sv` (service) command but it can be a little difficult to use for the first time, also it doesn't manage service enabling to disabling. So this script comes in handy!

Basically, it just links to `/var/service` to enable a service and unlinks (remove symbolic link from `/var/service`) to disable a service.

I may rename the repo with something else when I'll add more scripts in this repo!