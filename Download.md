# Download OPNsense On Mac:
Open the official download page:
Download OPNsense: https://opnsense.org/download/
## Select:
  - Architecture: amd64
  - Image type: dvd
  - Mirror: Germany
Download the ISO file (.iso.bz2).

## Extract the OPNsense ISO
After downloading:
1. Open Finder.
2. Go to Downloads.
3. Find the file ending in .iso.bz2.
4. Double-click it to extract it.
   
## Open VirtualBox:
<img width="1366" height="781" alt="Bildschirmfoto 2026-11-19 um 18 09 20" src="https://github.com/user-attachments/assets/afdeafd1-5b27-4427-8ed7-fb2163bc459f" />
## Step 3 – Configure OPNsense:
Recommended virtual machine settings‼️
| Setting      | Value       |
|--------------|-------------|
| RAM          | 4 GB        |
| CPU          | 2 cores     |
| Hard disk    | 20 GB       |
| Network      | 2 adapters  |
| Installation | ISO         |

## Create your virtual machine
Open VirtualBox.
1. Click New.
2. Enter the name: OPNsense-Lab.
3. Type: BSD.
4. Version: FreeBSD (64-bit).
5. RAM: 4096 MB (4 GB).
6. Processors: 2 CPUs.
7. Create a virtual hard disk:
   - Type: VDI
   - Storage: Dynamically allocated
   - Size: 20 GB
## Configure the network
This is an important step. We will isolate your practice firewall from your real home network.

Select your VM and click Settings → Network.

<img width="842" height="533" alt="image" src="https://github.com/user-attachments/assets/2c574fd0-384d-4f9e-8ac8-dc3b9734c47e" />

Adapter 1 – LAN
- Enable Network Adapter.
- Attached to: Host-only Adapter.
- Name: Select the available VirtualBox host-only network.
Adapter 2 – WAN
- Enable Network Adapter.
- Attached to: NAT.

  Ps: Do not use Bridged Adapter for this exercise.

## Install OPNsense
Start the virtual machine.
Wait for OPNsense to boot.
When the login prompt appears, enter: 
- Username: installer
- Password: opnsense

Follow the installation wizard.

  1-Choose the default keyboard layout.
  2-Choose UFS for the filesystem (simple for this lab).
  3-Select the virtual hard disk (ada0).
  4-Confirm installation.
  5-Set a new root password.



Complete installation and reboot.




