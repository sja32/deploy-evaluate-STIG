\# deploy\_evaluate\_stig Role



This role copies the Evaluate-STIG package from a network share (Synology NAS)

to the target Windows machine's `C:\\ProgramData\\Evaluate-STIG` directory.



\## Features

\- Creates the destination directory if missing.

\- Securely adds and removes SMB credentials for the share.

\- Uses PowerShell `Copy-Item` for reliable file transfers.

\- Logs every run to `C:\\Windows\\Temp\\evaluate\_stig\_copy\_<timestamp>.log`.



\## Example Playbook

```yaml

\- name: Deploy Evaluate-STIG

&nbsp; hosts: windows

&nbsp; roles:

&nbsp;   - role: deploy\_evaluate\_stig

&nbsp;     vars:

&nbsp;       smb\_user: "allensj"

&nbsp;       smb\_pass: "Luasi965!"



