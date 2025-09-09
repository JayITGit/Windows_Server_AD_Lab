# Windows Server Active Directory Lab

## 📌 Overview
This project demonstrates the deployment and configuration of a **Windows Server 2022 Active Directory Domain Services (AD DS) lab** in Microsoft Azure.  
The lab walks through setting up a **Domain Controller (DC)**, creating users and groups, and joining a **client machine** to the domain.

## 🛠 Skills Demonstrated
- Windows Server 2022 administration
- Azure VM deployment and management
- Active Directory installation and domain controller promotion
- User and group account management
- DNS and networking verification
- Client machine domain joining
- Permissions and troubleshooting
- Documentation and workflow management

---

## 🚀 Lab Guide

### **Phase 1: Server and Domain Controller Setup**

#### Step 1: VM Creation
![VM Creation](screenshots/01_vm_creation.jpg)  
This screenshot marks the beginning of the lab setup, where we configure the **DC-01** virtual machine. The VM is provisioned in the **West US 2** region within the **rg-ad-lab** resource group.

#### Step 2: VM Overview
![VM Overview](screenshots/02_vm_overview.jpg)  
The successfully deployed VM’s overview page, confirming **DC-01** is running. The **Private IP (10.0.1.4)** is crucial for networking.

#### Step 3: Accessing the VM
![Server Manager](screenshots/03_server_manager.jpg)  
The **Server Manager** dashboard confirms successful login and administrative access.

#### Step 4: Installation Type
![Install Type](screenshots/04_install_type.jpg)  
The **Add Roles and Features Wizard** begins. Default: **Role-based or feature-based installation**.

#### Step 5: Starting Installation
![AD DS Install](screenshots/05_ad_install.jpg)  
Installing **Active Directory Domain Services** and management tools.

#### Step 6: Feature Installed
![AD DS Installed](screenshots/06_ad_installed.jpg)  
AD DS successfully installed. Next: promote server to Domain Controller.

#### Step 7: Deployment Configuration
![Deployment Config](screenshots/07_deployment_config.jpg)  
Creating a new forest, naming the root domain **JayDC.local**.

#### Step 8: Domain Controller Options
![DC Options](screenshots/08_dc_options.jpg)  
Setting functional levels and **DSRM password**.

#### Step 9: NetBIOS Name
![NetBIOS](screenshots/09_netbios.jpg)  
Wizard generates **NetBIOS name (JAYDC)**.

#### Step 10: Prerequisites Check
![Prereq Check](screenshots/10_prereq.jpg)  
Validation passed — server is ready to be promoted.

#### Step 11: Installation & Promotion
*Not Pictured*  
Clicking **Install** promotes the server to Domain Controller, followed by automatic reboot.

#### Step 12: Diagnostics Check
![dcdiag](screenshots/12_dcdiag.jpg)  
Running **dcdiag** verifies domain controller health.

#### Step 13: Network Verification
![ipconfig](screenshots/13_ipconfig.jpg)  
`ipconfig /all` confirms correct DNS (`127.0.0.1`) and hostname.

#### Step 14: Open ADUC
![ADUC](screenshots/14_aduc.jpg)  
**Active Directory Users and Computers (ADUC)** shows domain **JayDC.local** is active.

#### Step 15: Create User 1
![User 1](screenshots/15_user1.jpg)  
Creating **Jayson Zatarain** (`HelpdeskUser@JayDC.local`) in **IT/HelpDesk OU**.

#### Step 16: Create User 2
![User 2](screenshots/16_user2.jpg)  
Creating second user **Lockout Lab** in default **Users container**.

---

### **Phase 2: Deploying a Client VM and Joining the Domain**

#### Step 17: Deploy Client-01 VM
![Client VM](screenshots/17_client_vm.jpg)  
Deploying **client-01** running **Windows 10 Pro** in **Subnet-Clients**.

#### Step 18: Join the Domain
![Join Domain](screenshots/18_join_domain.jpg)  
Client successfully joined domain: **Welcome to JayDC.local**.

#### Step 19: Verify Admin Permissions
![Admin Check](screenshots/19_admin_check.jpg)  
**HelpdeskUser** confirmed as local **Administrator** on client machine.

#### Step 20: Add Domain User to Client
![Add User](screenshots/20_add_user.jpg)  
Domain user **Lockout.LabUser** added to local accounts on client, granting access.

---

## 📖 Key Takeaways
- Successfully deployed and configured an **Active Directory environment** in Azure.  
- Gained hands-on experience with **user/group management** and **permissions**.  
- Practiced troubleshooting with **diagnostics tools** (`dcdiag`, `ipconfig`).  
- Demonstrated the ability to **document technical workflows** clearly and professionally.  

---

🔹 This project demonstrates a **real-world IT help desk skill set**, from server deployment to user support.
