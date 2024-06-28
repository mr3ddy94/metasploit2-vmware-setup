# metasploit2-vmware-setup

# Setting Up a Metasploitable 2 Virtual Machine on VMware Workstation

This guide provides step-by-step instructions to create and configure a Metasploitable 2 VM on VMware Workstation, which is essential for testing and training on various security tools and techniques.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Download Metasploitable 2](#download-metasploitable-2)
3. [Create a New Virtual Machine](#create-a-new-virtual-machine)
4. [Configure the VM Settings](#configure-the-vm-settings)
5. [Starting the Metasploitable 2 VM](#starting-the-metasploitable-2-vm)
6. [Post-Installation Steps](#post-installation-steps)
7. [Troubleshooting](#troubleshooting)

## Prerequisites

- VMware Workstation installed on your system.
- Minimum 10 GB of free disk space.
- Minimum 1 GB of RAM.
- An active internet connection.

## Download Metasploitable 2

1. Go to the [Metasploitable 2 download page](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/).

2. Download the `Metasploitable2-Linux.zip` file.

3. Extract the downloaded `.zip` file to a desired location on your system.


## Create a New Virtual Machine

1. Open VMware Workstation and click on `Create a New Virtual Machine`.

2. Choose `Typical (recommended)` and click `Next`.

3. Select `I will install the operating system later` and click `Next`.

4. Choose `Linux` as the guest operating system and select `Other Linux 2.6.x kernel` as the version. Click `Next`.

5. Name your virtual machine (e.g., `Metasploitable 2`) and choose a location for storing the VM files. Click `Next`.

6. Set the disk size. It's recommended to allocate at least 10 GB. Choose `Store virtual disk as a single file` and click `Next`.

7. Review the hardware settings and click `Customize Hardware...`.


## Configure the VM Settings

1. In the `Hardware` tab, select `New CD/DVD (IDE)` and set the connection to `Use ISO image file`. Browse and select the extracted `Metasploitable2-Linux.iso` file. This will act as our hard drive for the VM.

2. Optionally, adjust the amount of RAM and CPU cores allocated to the VM in the `Memory` and `Processors` sections respectively. It's recommended to assign at least 1 GB of RAM and 1 CPU core.

3. Click `Close` and then `Finish` to complete the setup.

## Starting the Metasploitable 2 VM

1. Start the virtual machine by clicking on `Power on this virtual machine`.

2. The Metasploitable 2 VM will boot up and you will see a login screen. The default credentials are:
   - Username: `msfadmin`
   - Password: `msfadmin`


## Post-Installation Steps

1. **Network Configuration**: Ensure that the VM is configured to use the `Bridged` or `NAT` network mode to communicate with your host and other networked systems.

2. **Security Note**: Metasploitable 2 is intentionally vulnerable. Use it in a controlled and isolated environment to avoid unintended exposure to your network or sensitive data.

3. **Snap a Screenshot**: You can take a screenshot of the running VM for documentation or future reference using the `Take Snapshot` feature in VMware Workstation.


## Troubleshooting

- **VM doesn't start**: Check that the `.vmdk` file is correctly associated and that the VM settings are configured properly.
- **No network connection**: Verify the network adapter settings in the VM configuration and ensure it's set to `Bridged` or `NAT`.
- **Performance issues**: Adjust the VM’s allocated resources (CPU, RAM) to improve performance if necessary.
