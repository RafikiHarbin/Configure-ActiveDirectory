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
SET UP RESOURCES IN AZURE

- Step 1: Create the Domain Controller VM (Windows Server 2022) named “DC-1”.

![Create DC-1](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/354a1afd-cc24-41a6-a131-ecf827d63044)

                                                                                                                        
         1a.Take note of the Resource Group and Virtual Network (Vnet) that get created at this time.

![Resources automatically created](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/936f7760-fd74-4504-9782-f80ccfe1f91b)

- Step 2: Create the Client VM (Windows 10) named “Client-1”. Use the same Resource Group and Vnet that was created in 
                  Step 1a.

![Create Client-1](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/13be4312-316d-4198-8860-0c75b72d54d8)

![Vnet](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/ae0a00ee-b611-42a3-915a-39caa6d0353e)

- Step 3: Set Domain Controller’s NIC Private IP address to be static.

 ![image](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/821e90c0-eae4-4ccb-9f9b-c7ccf3109c04)

![IP Setting](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/7febeebf-90b8-42c4-b3c2-36d761e04b7b)

- Step 4: Ensure that both VMs are in the same Vnet.
____________________________________________________________________________________________________________________________
<h2>Deployment and Configuration Steps</h2>

![Create DC-1](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/4a6e01c4-38d3-413b-b62e-07d2a91820f5)





The Domain Controller VM "DC-1" has been created. (Resource Group, Virtual Network, and Subnet is automatically created)
__________________________________________________________________________________________________________________________




![Client-1 VM](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/3bd58885-acbf-4c34-b534-65c1c14c54fe)

The "Client-1" VM has been created using the same Resourse Group and Vnet that was created for "DC-1" VM in step 1a.
__________________________________________________________________________________________________________________________




![NIC to Static](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/1cecfb24-b07a-42b8-a7f6-6768b34d1cb9)

Domain Controller's Network Interface Card (NIC) has been set from Dynamic to Static.
__________________________________________________________________________________________________________________________




![Both VM's on Same Vnet](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/fe999c5e-a856-4d68-81cc-eb0d73f8800b)

"DC-1" and "Client-1" Virtual Machines (VM's) are on the same Virtual Network (Vnet).
__________________________________________________________________________________________________________________________
