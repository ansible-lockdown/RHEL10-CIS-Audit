
# RHEL 10 Goss config

## Overview

based on CIS 1.0.1 - 22-Sep-2025

Ability to audit a system using a lightweight binary to check the current state.

### Memory Usage
 Running the audit sees an Increased RAM usage, improvements seen when dropping swappiness e.g. 5. Already improved by latest kernel update 6.12.0-55.12.1 as of 19-05-25

This is:

- very small 11MB
- lightweight
- self contained

It works using a set of configuration files and directories to audit CIS of RHEL family 10 servers. These files/directories correlate to the CIS Level and STIG_ID

Tested on

- RHEL10
- almalinux10
- rocky10

## Requirements

You must have [goss](https://github.com/goss-org/goss/) available to your host you would like to test.

You must have sudo/root access to the system as some commands require privilege information.

Assuming you have already cloned this repository you can run goss from where you wish.

Please refer to the audit documentation for usage.

- [readthedocs](https://ansible-lockdown.readthedocs.io/en/latest/)

This also works alongside the [Ansible Lockdown RHEL10-CIS role](https://github.com/ansible-lockdown/RHEL10-CIS)

Which will:

- install
- audit
- remediate
- audit

## Join us

On our [Discord Server](https://www.lockdownenterprise.com/discord) to ask questions, discuss features, or just chat with other Ansible-Lockdown users

Set of configuration files and directories to run the first stages of CIS of RHEL 10 servers

This is configured in a directory structure level.

Goss is run based on the goss.yml file in the top level directory. This specifies the configuration.

## Further Information

- [goss documentation](https://github.com/aelsabbahy/goss/blob/master/docs/manual.md#patterns)
- [CIS standards](https://www.cisecurity.org)
