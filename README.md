# Azure Virtual Machines Traffic Inspection

In this tutorial, we will be setting up 2 virtual machines and observing several network traffic protocols using Wireshark.
The protocols we will be focusing on include:
- DNS (Domain Name System; UDP Port 53)
- SSH (secure shell; TCP Port 22)
- DHCP (Dynamic Host Configuration Protocol; UDP Ports 67 & 68)
- ICMP (Internet Control Message Protocol; No Port #)
- RDP (Remote Desktop Protocol; TCP Port 3389)


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

<b>Now that we have a Resource Group, this allows us to create the first Virtual Machine. Be sure to select the resource group that was just created as well as the same region that was selected. It should be running Windows 10 and it should be provisioned at least 2 cores and 16GBs of memory. This setting will allow the machine to be as performant as we need it to be. Also, take note of the login information you input because that is how to log in via remote desktop. 

After a successful deployment, be sure to hit "Create another VM" in order to create the second Linux VM. </b>

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/523e0541-1473-411e-b8a8-4f6e656d8cca)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/f482ec5a-d920-4e44-b3d7-18ef795ef55a)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/f0670863-8911-478e-8892-0b6c06d8749b)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/e4e16513-ecde-4e07-8e66-d5b49379475b)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/d6286daa-0b57-4445-9828-df586090dafd)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/36e813f3-4218-4f27-b277-b0cb5ebd96c3)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/d4688cb9-cffb-4bd6-b379-2d8d1e5edc9e)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/2d4f2871-132a-47eb-a4c9-5a0e8b1cebbc)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/41cadc77-1a16-49e3-adc2-fdee9bd279e1)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/66d3a9d0-5e70-4c81-91ae-5fc51843bf1b)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/fced4369-c12a-4d59-a14b-e705ed492558)



