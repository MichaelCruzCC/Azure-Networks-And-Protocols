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

<b>When creating the second VM be sure to select the same Resource Group as the Windows VM, the same region, and the same size allocation. For authentication type choose password and use the same login as you did for the Windows VM. The default SSH port is fine as is. Once deployed, it will then be time to observe network protocols between the two VMs.

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/6eb01db6-7d2f-4daa-a8ea-c45414fedbdd)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/2629c3f6-91c7-40bc-8fb1-dcaf951aed58)
![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/cf491485-2b33-4eea-befb-9b87dd28e438)

<h2>Observing Network Protocols Using Wireshark</h2>

<b>With the VM's created, we can now go back to portal.azure.com and see them listed in our resources.</b>

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/87d188dd-c492-416d-8b87-87e6707a281d)

<b>Select VM-01 and copy the public IP address in order to use Remote Desktop Connection to log in to the VM. Once logged in with the previously chosen credentials, open up Microsoft Edge, download, and install Wireshark. </b>

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/ca71b4a1-f2fc-46be-844d-d9d1121f8a71)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/37a72187-b319-403b-85fe-cd3cb74c5b65)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/c82f8038-a8cb-4da2-987d-2e889699ffca)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/a37debc3-0530-47a4-afe9-bceddf07fe8e)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/69d56e86-2914-486c-8204-fc3f02bd0e1f)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/a11fa5df-9d4c-4e79-8c06-842cd8dcf65c)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/b4f16222-2dff-437e-9463-d5636825d301)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/f27a9f1c-9124-49ca-b39a-c9ddd268a0f2)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/725d64ad-fa7c-4137-adb3-38363a316b77)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/79e12cbe-edc1-49d0-85c1-c86886669b4a)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/86a59277-f078-4c79-a41c-ea6e0076071d)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/ad8de4b7-10a9-4480-8432-585e772ed903)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/46e4b8ce-6574-4833-b6b6-2aef681512b0)

<b>With Wireshark now installed, it is possible to filter for different types of traffic. The first of which will be ICMP traffic, based on a simple ping command to our Linux VM. </b>

- Within wireshark start capturing packets then filter for icmp.
- On your actual machine, go back to portal.azure.com and copy VM-02's IP address.
- Go back to the remote session, open Command Prompt and run "ping -t *Linux IP address*"
- You'll note that the requests time out. This is because VM-02's firewall is blocking it.
- Back on your actual machine, go to VM-02's networking tab and add an Inbound rule for icmp, with the priority being before any of the existing rules.
- Within the remote session, once applied, the pings should start to succeed, rather than time out.
- Once successful pings have been observed, feel free to stop pinging using Ctrl + C.

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/1ded7253-6a09-4b52-a97f-ba9522625507)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/4defb8c6-27fe-44b1-9425-ce253c00e6a3)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/7a48bdfa-e2aa-4cc5-b3e0-fe77aa255924)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/4b3ddd9d-3077-471c-90ab-2430ff859a71)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/4b57e828-ec42-4504-841f-6f866b742c3c)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/04bafbd2-64f3-4f7b-8403-826b376fd231)

<b> The second type of traffic to observe will be SSH, once we connect and log in to the Ubuntu VM from within the Windows VM. </b>

- First, check the Azure portal for the private IP address of VM-02, be sure to copy it.
- Within the Windows VM, set your Wireshark filter to "ssh" or "tcp.port == 22" and run Windows Powershell to SSH into VM-02. 
- The Powershell command is "ssh *username*@*private IP address*
- Say Yes to continue connecting, then enter the password for VM-02. It won't show your characters being typed out.
- Run Linux commands such as "id", "uname -a", "pwd", "ls -lasth", "touch hi.txt"
- Run "exit" command to close the ssh connection and Ctrl + C to end the command. You can observe all the Wireshark traffic.

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/927c9410-c801-4208-a7d8-e9fcb9f6ef19)

<b> Next is observing DHCP traffic by reissuing an IP address to our Windows VM using the command "ipconfig/renew". Remember to set the filter to dhcp.

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/063b9e77-f647-4544-b006-5d272d3e9398)

<b> Now it is time to monitor DNS traffic by using the "nslookup" command. This command essentially asks the DNS server what the IP address of the inputted website is. Wireshark will show you the live traffic over the internet once you filter using "dns" or "udp.port == 53" </b>

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/c6c33a98-50a4-43ae-9f4e-351d05e3b1cb)

<b> Finally, the last thing to observe is RDP traffic. This will spam network traffic because of our live remote desktop connection between our Physical machine and the Virtual Machine. The filter for this is "rdp" or "tcp.port == 3389".</b>

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/017d9778-2cdf-4491-9fb7-e4767fff6067)


<h2>Cleaning Up Our Resources</h2>

<b> Now that the inspection between the two VMs is done, it is a good idea not to waste precious credits on resources that we will no longer be utilizing. </b>
- Go to portal.azure.com
- Delete the two resource groups
- Wait for the resources to be de-provisioned. Refresh every so often to make sure there are no more resource groups.

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/32e3cbd2-02e0-4ab5-91c9-793178bd9744)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/5c131711-37e5-40ee-8127-56bf9f7060f0)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/7bd557d3-f98a-473b-97c1-06536ee42aad)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/758ef893-99d9-4f31-a955-abbbfcda6fea)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/9a2b760d-c775-4e50-8aff-568d54a16fdb)

![image](https://github.com/MichaelCruzCC/Azure-Networks-And-Protocols/assets/138819301/2dbd6e43-ed99-4686-b913-e912c783c780)

<h1>Inspection Tutorial Complete</h1>



