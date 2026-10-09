ACTIVE DIRECTORY

what i learned
- Active Directory (AD) is a Microsoft directory service used to manage users, computers, groups, and other resources in a Windows domain.
- A domain controller suns Active Directory Domain Services (AD DS).
- Users Can be organized into Organizational Unit (OUs)
- Group Policy can be used to manage settings across computers and users.
- Active Directory uses DNS for name resolution and domain services. etc.

Concepts i practiced
- Domain
- Domain Controller (DC)
- Active Directory Domain Services (AD DS)
- Users
- Groups
- Organizational Units (OUs)
- Domain accounts
- DNS and its relationship to Active Directory
- Group Policy
- Computer accounts
- Domain joining


GROUP POLICY
what i learned
- Group Policy (GPO) is used to centrally manage user and computer settings in a Windows domain.
- Folder mapping can be configured through Group Policy.
- User and computer settings can be controlled using Group Policy Objects.
- Security and account lockout policies can be configured to improve system security.
- Printers and software can be deployed through Group Policy.
- Application access can be controlled using AppLocker.
- Group Policies can be backed up and restored.
- Group Policy Objects (GPOs). etc.

concepts i practiced
- Group Policy Objects (GPOs)
- Folder Mapping
- Control Panel Restrictions
- Custom Wallpaper Deployment
- Account Lockout Policies
- Security Policies
- Printer Deployment
- Logon Restriction
- Software Deployment
- AppLocker
- Task Manager Restrictions
- GPO Backup and Restore
- Verifying Applied Group Policies


DOMAIN NAME SYSTEM (DNS)
- DNS (Domain Name System) translates domain names into IP addresses.
- DNS helps computers locate servers and other devices on a network.
- DNS zones store information about domains and their records.
- DNS Forward Lookup Zones resolve names to IP addresses.
- DNS Reverse Lookup Zones resolve IP addresses to names.
- DNS can be configured and managed using Windows Server.
- DNS works with Active Directory to support domain services.

Concepts I Practiced
- Understanding Domain Name System (DNS)
- Installing the DNS Server Role
- Configuring DNS in Windows Server
- Creating Forward Lookup Zones
- Creating Reverse Lookup Zones
- Configuring DNS Settings on Client Computers
- Testing DNS Resolution
- Using DNS Manager
- Understanding DNS Integration with Active Directory. etc.


My Lab Environment
Virtual Machines
- Windows Server 2019-Domain Controller
- Windows Server 2019- Additional server
- Windows 10 pro-Client computer
- Windows 8.1 pro-Client computer
- Other Windows-Restore(backup)

Domain
- MyBusiness.local

Domain Controller 
- Server 1
- Server 2

Clients
- Windows 10
- Windows 8.1


What i practiced
1.Installing Active Directory Domain Services
- I installed the AD DS role on windows server and promoted the server to a Domain Controller.

2.Creating a Domain
- I created the domain: MyBusiness.local

3.Creating Users
- I created domain user accounts and tested logging into Windows using domain credentials.
example:
-MyBusiness.local/username

4.Creating Groups
- I Created security groups to organize users and control access.
example:
- GRP_sales
 
5.Creating Organizational Units
- I creates OUs to organize users and computers within Active Directory.

6.Joining a Windows 10 Computer to a Domain
- I configured the Windows 10 computer to use the domain controller's DNS address and joined it to: MyBusiness.local

7.Testing Domain Connectivity 
- I used commands such as:
-hostname
-ipconfig
-ping
-nslookup
-whoami
to troubleshoot connectivity, DNS and domain login issues.


Lab Screenshot
![Active Directory Lab](Images/active-directory.png)




PROBLEMS I ENCOUNTERED
Problem 1: Windows 10 could not properly communicate with the Domain Controller
what i checked
- IP address
- Subnet mask
- Default gateway
- DNS server
- Network connection
- Domain name
 
Solution:
- I corrected the network/DNS configuration and tested connectivity again.

Problem 2: Group Policy was not immediately reflected on the clients

Solution:
- I used; gpupdate /force and then checked the applied policies.


What I Understand Now
I understand that Active Directory allows an organization to centrally manage:
- Users
- Computers
- Groups
- Security policies
- Access Permissions
- Domain resources
I also understand that the Domain Controller is a central part of an Active Directory domain and that DNS is important for AD communication.


Commands i learned
- ipconfig
- ping
- nslookup
- whoami 
- gpupdate /force
- gpresult /r
- grpresult /h gp-report.html
- gpedit.msc
- ipconfig /displaydns
- ipconfig /flushdns



