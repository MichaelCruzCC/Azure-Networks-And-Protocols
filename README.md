# Azure Virtual Machines Traffic Inspection

In this tutorial, we will be setting up 2 virtual machines and observing several network traffic protocols using Wireshark.
The protocols we will be focusing on include:
- DNS (Domain Name System; UDP Port 53)
- SSH (secure shell; TCP Port 22)
- DHCP (Dynamic Host Configuration Protocol; UDP Ports 67 & 68)
- ICMP (Internet Control Message Protocol; No Port #)
- RDP (Remote Desktop Protocol; TCP Port 3389)
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure Virtual Machines

- Remote Desktop Connection

- Network Protocols (SSH, RDP, DNS, ICMP, DHCP)

- Wireshark is the network traffic analyzer used to observe the different types of traffic being sent between both VMs.

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Linux/Ubuntu Server 20.04 

<h2>Creating the Virtual Machines</h2>

<b>Once logged in, the first step is creating a resource group. Choose the region closest to you, as we will build the Virtual Machines in the same region.</b>

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/17b50e6d-5e33-4b2a-9616-079195770ffe)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/e04d31f1-58e9-4c85-841b-3e1bb9d8decb)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/5aecdc1d-ec6e-4cb1-be32-1dc54cceb971)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/63238a54-1fe4-4fdf-8e25-bc2f2174359d)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/1cc9afb5-ac13-4392-9afd-01fdf86843c5)

