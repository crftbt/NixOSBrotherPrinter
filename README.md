# NixOSBrotherPrinter

Steps I used to print with a Brother HL-2240 printer on NixOS 23.11.
1. Install virt-manager
2. Install PopOS in a virtual machine
3. Plug in Brother Printer USB
4. Add USB device to Virtual Machine
5. Setup printer in PopOS
6. Print
7. In a terminal on PopOS ```sudo find / | grep -i hl |grep -i 2240 |grep -i "ppd$"```
8. Copy the ppd file to NixOS ```scp /etc/hl2440.ppd nixos@nixos:~/```
9. In Desktop Environment Printer Settings, Add Printer
10. Right click ... and select Printer Details for HL-2240
11. Use the ppd file in our home directory.
