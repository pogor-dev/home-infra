# Cockpit Role

This Ansible role installs and configures the Cockpit web console on AlmaLinux.
Replicates [these steps](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/8/html/managing_systems_using_the_rhel_8_web_console/getting-started-with-the-rhel-8-web-console_system-management-using-the-rhel-8-web-console).

## Requirements

None.

## Role Variables

None.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - cockpit
```

## License

MIT

## Author Information

Victor Pogor
