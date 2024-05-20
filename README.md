<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Create the Domain Controller VM (Windows Server 2022) named “DC-1”.
                                                                                                                        
         a.Take note of the Resource Group and Virtual Network (Vnet) that get created at this time.

- Step 2: Create the Client VM (Windows 10) named “Client-1”. Use the same Resource Group and Vnet that was created in 
                  Step 1a.
- Step 3: Set Domain Controller’s NIC Private IP address to be static.
- Step 4: Ensure that both VMs are in the same Vnet.

<h2>Deployment and Configuration Steps</h2>

![Create DC-1](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/4a6e01c4-38d3-413b-b62e-07d2a91820f5)





The Domain Controller VM has been created. (Resource Group, Virtual Network, and Subnet is automatically created)

![Client-1 VM](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/3bd58885-acbf-4c34-b534-65c1c14c54fe)

The Client-1 VM has been created using the same Resourse Group and Vnet that was created for DC-1 VM in step 1a.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
