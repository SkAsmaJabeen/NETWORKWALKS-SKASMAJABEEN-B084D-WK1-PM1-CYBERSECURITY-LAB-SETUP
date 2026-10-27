# NETWORKWALKS-SKASMAJABEEN-B084D-WK1-PM1-CYBERSECURITY-LAB-SETUP
# Cybersecurity Lab Environment Setup - WK1-PM1

## NetworkWalks Cybersecurity Internship

**Project:** Week 1 – Project Module 1 (WK1-PM1)
**Author:** Asma Jabeen Shaik
**Tools:** Oracle VirtualBox, Kali Linux, 7-Zip
**Category:** Cybersecurity Lab Setup

## 1. Project Overview

This project involves setting up a virtual cybersecurity testing environment using Oracle VirtualBox and Kali Linux. The purpose is to prepare an isolated virtual lab for authorized cybersecurity learning, networking practice, and future ethical hacking exercises.

## 2. Objectives

- Install and configure VirtualBox.
- Import Kali Linux as a virtual machine.
- Configure a custom NAT Network using the `10.0.0.0/24` subnet.
- Assign Kali Linux the static IP address `10.0.0.2/24`.
- Enable clipboard sharing and drag-and-drop.
- Configure a shared folder named `downloads` from the host machine.
- Verify internet connectivity from Kali Linux.
- Take a snapshot of the configured virtual machine.

## 3. Tools and Technologies

| Tool                     | Purpose                             |
| ------------------------ | ----------------------------------- |
| Oracle VirtualBox        | Virtualization platform             |
| Kali Linux               | Cybersecurity testing environment   |
| 7-Zip                    | Archive extraction, where required  |
| NetworkManager (`nmcli`) | Network configuration in Kali Linux |

## 4. Network Configuration

| Parameter       | Required configuration                           |
| --------------- | ------------------------------------------------ |
| Network type    | NAT Network                                      |
| Network name    | `NatNetwork`                                     |
| IPv4 subnet     | `10.0.0.0/24`                                    |
| Kali Linux IP   | `10.0.0.2/24`                                    |
| Gateway         | `10.0.0.1` (verify against actual configuration) |
| DNS             | Configured DNS resolver(s)                       |
| Internet access | To be verified                                   |

## 5. Implementation Steps

1. Installed the required virtualization software and extracted the Kali Linux virtual machine files, if necessary.
2. Imported the Kali Linux virtual machine into VirtualBox.
3. Created a custom NAT Network with the required IPv4 subnet.
4. Connected the Kali Linux virtual machine to the NAT Network.
5. Configured Kali Linux with the required static IPv4 address.
6. Enabled shared clipboard and drag-and-drop in the VM settings.
7. Configured the host's downloads folder as a shared folder.
8. Tested the IP configuration and internet connectivity.
9. Created a snapshot of the configured virtual machine.

## 6. Verification Commands

Run the following commands inside Kali Linux and compare their output with the assignment requirements.

Check the IP address:

```bash
ip -br address
```

Check the routing table:

```bash
ip route
```

Test connectivity to the configured gateway:

```bash
ping -c 4 10.0.0.1
```

Test external IP connectivity:

```bash
ping -c 4 8.8.8.8
```

Test DNS resolution:

```bash
ping -c 4 google.com
```

**Verification results:** Record the actual results after running these tests.

- Kali IP address: [Verified / Pending]
- NAT Network subnet: [Verified / Pending]
- Gateway connectivity: [Pass / Fail / Not tested]
- Internet connectivity: [Pass / Fail / Not tested]
- DNS resolution: [Pass / Fail / Not tested]
- Clipboard and drag-and-drop: [Verified / Pending]
- Shared folder: [Verified / Pending]
- VM snapshot: [Created / Pending]

## 7. Screenshots and Evidence

The `screenshots/` directory contains evidence of the lab configuration.

| Screenshot                     | Evidence                          |
| ------------------------------ | --------------------------------- |
| `01-virtualbox-kali.png`       | Kali Linux VM in VirtualBox       |
| `02-nat-network.png`           | NAT Network subnet configuration  |
| `03-kali-ip.png`               | Kali Linux IP address             |
| `04-internet-connectivity.png` | Network connectivity test results |
| `05-clipboard-drag-drop.png`   | VM integration settings           |
| `06-shared-folder.png`         | Shared folder configuration       |
| `07-vm-snapshot.png`           | Completed VM snapshot             |

Replace any missing evidence and filenames as necessary.

## 8. Troubleshooting: Kali Linux Internet Connectivity

**Issue:** Kali Linux was not accessing the internet properly after configuring the virtual machine's network settings.

**Possible Cause:** The NAT Network configuration, IP address settings, default gateway, or DNS configuration may have been incorrect.

**Solution:**

1. Verified that the VirtualBox NAT Network was enabled and configured with the subnet `10.0.0.0/24`.
2. Checked that Kali Linux was connected to the correct NAT Network.
3. Verified the IP address and routing table using `ip -br address` and `ip route`.
4. Tested connectivity to the gateway and an external IP address.
5. Checked DNS resolution using `ping -c 4 google.com`.
6. Corrected the relevant network settings and restarted the network connection where necessary.

**Verification:** Repeated the connectivity tests after applying the correction to determine whether internet access and DNS resolution were working.

**Learning:** This troubleshooting process helped me understand the relationship between virtual network configuration, IPv4 addressing, default gateways, and DNS resolution in a virtualized cybersecurity lab.

## 9. Learning Outcomes

Through this project, I practised:

- Creating and configuring virtual machines.
- Understanding NAT Network configuration and IPv4 addressing.
- Configuring a static IP address in Kali Linux.
- Testing basic connectivity and DNS resolution.
- Configuring VM integration features and shared folders.
- Creating snapshots to preserve a working lab state.

## 10. Responsible Use

This environment is intended for educational purposes and authorized cybersecurity testing only. All future practical exercises will be performed within systems I own or have explicit permission to test.

## 11. References

- [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads)
- [Kali Linux Downloads](https://www.kali.org/get-kali/)
- [NetworkWalks Sample Repository](https://github.com/waqaskarimccie/Cybersecurity-Lab-Setup1)

---

**Project:** NetworkWalks Cybersecurity Internship - WK1-PM1
**Author:** Shaik Asma Jabeen
