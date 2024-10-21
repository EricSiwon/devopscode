# proxmox

```text
How to Fix the “No QEMU Guest Agent Configured” Message

    First, enable QEMU Guest Agent on Proxmox during VM creation or configuration. So, go to the VM configuration menu in Proxmox VE.
    Then, go to the Options tab and find the checkbox for “Qemu Agent.”
    Make sure this this checkbox is enabled for this specific VM.
    However, if we are creating a new VM, enable the checkbox during the VM creation process.
    Then, click “Save” to apply the changes.
    Next, we need to install and enable the QEMU Guest Agent within the guest operating system. Here are the steps for common Linux distributions:
        Debian/Ubuntu:

        sudo apt update
        sudo apt install qemu-guest-agent
        CentOS/RHEL:

        sudo yum update
        sudo yum install qemu-guest-agent
    Once installed, enable and start the Guest Agent service:
        Systemd (Most Modern Linux Distros):

        sudo systemctl enable qemu-guest-agent
        sudo systemctl start qemu-guest-agent
        SysVinit (Older Linux Distros):

        sudo chkconfig qemu-guest-agent on
        sudo service qemu-guest-agent start
    In some cases, a VM reboot can resolve any issues that prevent the Guest Agent from starting correctly.

The above steps will help us fix the “No QEMU Guest Agent configured” message in Proxmox VE.
```