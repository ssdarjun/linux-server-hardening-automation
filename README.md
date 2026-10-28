# Linux Server Hardening Automation

Comprehensive Bash and Ansible automation scripts designed to harden Ubuntu/Linux production servers to **CIS (Center for Internet Security) Benchmarks**, eliminating default misconfigurations and securing the OS perimeter.

## Implemented Security Controls
- **Access Control:** Disables root login via SSH, enforces SSH key-only authentication, and changes default SSH configuration parameters.
- **Firewall Management:** Configures `ufw` to drop all incoming traffic by default while explicitly whitelisting required ports.
- **Intrusion Prevention:** Installs and configures `fail2ban` to block brute-force attack vectors.
- **Package Auditing:** Automates unattended security updates and removes unnecessary legacy packages/services.

## Usage Guide
Run the hardening script with administrative privileges on a fresh Ubuntu server instance:
```bash
sudo chmod +x harden.sh
sudo ./harden.sh

(Or execute the equivalent Ansible playbook):
ansible-playbook -i inventory site.yml --ask-become-pass
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
