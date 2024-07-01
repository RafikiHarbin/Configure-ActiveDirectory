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



![IP Setting](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/7febeebf-90b8-42c4-b3c2-36d761e04b7b)

![Static](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/4d8d3e04-9c8c-4d19-9542-f34eb34d1059)
![Static Complete](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/7e3bfcb2-97bb-49c7-8430-3c108935c9b5)

- Step 4: Ensure that both VMs are in the same Vnet.
![Client 1 Vnet](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/97719030-966f-4f40-9258-ab0adf9186dc)

![DC-1 Vnet](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/e8fdb686-7960-4eec-be1b-378840f1b3f3)
___________________________________________________________________________________________________________________________
<h2>Deployment and Configuration Steps</h2>

INSTALL ACTIVE DIRECTORY (AD)


![AD Install](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/dd391f54-128e-42db-841f-8028e0d20f06)

___________________________________________________________________________________________________________________________

CREATE AN ADMIN AND NORMAL USER ACCOUNT IN ACTIVE DIRECTORY (AD)
![Organizational Unit Admin   Employees](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/d9bf4b8f-14de-448e-aa17-85e5d472774f)
__________________________________________________________________________________________________________________________
CREATE USER ACCOUNT & ASSIGN TO DOMAIN ADMIN GROUP

![Assign ed to domain admin group](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/f3e448c4-1cbe-42d8-ba9d-72b64ace4136)

Log out & log back in as "mydomain.com\rafiki_admin"


![mydomain](https://github.com/RafikiHarbin/Configure-ActiveDirectory/assets/170275827/e8516f46-446f-4234-b512-055f3b398073)

___________________________________________________________________________________________________________________________











