# Deploy Evaluate-STIG

This playbook deploys the latest Evaluate-STIG package from a network share to Windows endpoints.

## Usage
- Runs from AWX or Ansible using a Windows Execution Environment.
- Copies Evaluate-STIG from `\\192.168.40.42\raw-images\Evaluate-STIG_1.2507.5`
  to `C:\ProgramData\Evaluate-STIG` on the target host.

## Required Vars
| Variable | Example | Description |
|-----------|----------|-------------|
| `smb_user` | `Billy-Butcher\svc-ansible` | SMB credential for share access |
| `smb_pass` | `YOURSECUREPASSWORD!` | SMB password for share access |

## AWX Settings
- **Execution Environment:** `Windows EE`
- **Inventory:** `Windows Test Inventory`
- **Credential:** `WinRM - svc-ansible`
- **Playbook:** `deploy-evaluate-stig.yml`
