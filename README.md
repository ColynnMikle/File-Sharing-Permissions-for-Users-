# File-Sharing-Permissions-for-Users-
This section details file sharing and permissions to be granted to read/write/no access user groups.
<p align="center">
<img src=https://i.imgur.com/fGeIqJT.png
<p>
<p>  
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- VM1 and VM2 from my Active Directory explanation are used in this showcase

<h2>Operating Systems Used </h2>
- Windows Server 2022 Datacenter 
<p></p>
- Windows 10</b> (21H2)

<h2>Configuration Objectives</h2>

- Create access folders to organize users
- Set permissions type in each folder
- Test access from users and admins to folders


<h2>Configuration Steps</h2>

<p>
<img src=https://i.imgur.com/4R3R3CU.png)</p>
<p>
- From the Windows 2022 Server (VM1) access the C: file directory
<p>
- Create folders titled "READ_ACCESS", "WRITE_ACCESS", "NO_ACCESS", and any department specific folders you choose. I made a folder for the "Finance Department" for this showcase.
<p>
<p>
<img src=https://i.imgur.com/vUyQciw.png)</p>
<p>
<p>
- Access the "Properties" tab on each folder by right clicking the file name and using the drop-down menu. Go to "sharing". For the Read folder share to "Domain Users" with the permission Read.
<p>  
- Repeat for Write folder, sharing with "Domain Users". Select Read/Write permissions. The window should appear as the one shown above.
<p>
- Access sharing tab in "Properties" menu for "NO_ACCESS" folder. Share with "Domain Admins" with the permissions of Read/Write.
<p>
<p>
<img src=https://i.imgur.com/hSqB0jI.png
<p>
<p>
<img src=https://i.imgur.com/f1so90F.png
<p>
<p>  
- Test with users on VM2/client computer. An error message should appear if attempting to access folders and add files as shown in the image above if the user only has read only permissions.
<p>
- If the user has "Read/Write" permissions, the folder should allow files to be added, as shown in the image above.
<p>
<p>
<img src=https://i.imgur.com/aZ0mbjC.png  
</p>
<p>
- From VM1/domain controller, access the "Active Directory Users & Computers" window via the start menu. Create an Organizational Unit called "SECURITY_GROUPS". Here, you will place department groups. I added "Finance Department" as an example. 
<p>
- Right click inside the security groups OU to add departments. To add members to a given department, right click and select "Properties". Add user(s) under the "Members" tab to allow the following step. 
<p>
- Return to the C: directory and select the department you want to add permissions to. Share the files to the department name of your choosing as shown below.
<p>
<p>
<img src=https://i.imgur.com/uA4B2Fa.png)

</p>
<p>
- Test department folders with user accounts to ensure proper access is given.
<p>  
- Note: if users are not assigned to that specific department's security group as a member, files will be inaccessible.   
</p>
<br />
