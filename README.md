# sshjumpbox_configure_host

## Description:

Configures a RHEL host as an SSH jump box.

## Behaviour:

**Feature:** Ensures Docker Compose is installed
As a System Admin
I want to ensure that a RHEL host is configured as an SSH jump box
So that remote connections can be passed through to other IP addresses securely and easily

**Scenario**: Configures a RHEL 7 host to act as an SSH jump host
- **Given** a base RHEL 7 host is available
- **Given** the host is ready to accept SSH connections from Ansible
- **When** the configuration of the host is initiated
- **Then** OpenSSH service is configured
- **Then** Security certificates are created

## Configuration:

### Default variables

The following is a list of default variables used by this role.

### Variables
| Variable  | Description  |
|---|---|
| **listening_ssh_port** | The port that SSH listens to for incoming connections (defaults to 22) |
| **listening_ip** | The IP address for SSH to listen on (defaults to 0.0.0.0) |
| **private_ssh_key** | The private key to use instead of default generated one (optional) |
| **public_ssh_key** | The public key to use instead of the default generated one (optional) |
