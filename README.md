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
- Windows 11

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 Configure Admin/Users Access
- Step 2 Account Lockout Policy
- Step 3 Group Policy
- Step 4 Reset Passwords

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1637" height="872" alt="Screenshot_14-10-2026_20659_coursecareers com" src="https://github.com/user-attachments/assets/15d5b283-396b-4649-b4b3-b8b73b1c3c41" />

</p>
<p>
The Account Lockout Policy was not automatically installed in Active Directory, so Group Policy had to be used to Configure it. In the Lab, the Configuration Policy was tested to see if it was in Compliance. After five failed Logon attempts, the Agent's was still allowed access and authorization to Logon.  The Lab said do 10 failed attempts to Logon, and that's when a red flag was raised and confirmed that the Lockout Policy must be Configured. The Account Lockout policy was updated on the Client-1 server, so when the Account Lockout Policy threshold has exceeded the amount of failed Logon attempts, that will trigger an Account Lockout.
</p>
<br />
Acct
<p>
<img width="239" height="299" alt="Screenshot_14-10-2026_202840_coursecareers com" src="https://github.com/user-attachments/assets/67fe2e2e-dd4f-4374-8f7f-6a113fe64e2b" />

</p>
<p>
All Configurations has been installed for Agents . Now a failed Logon has to wait 5 minutes before user get a second chance to Login. After five invalid Logon attempts the Account will be locked out for 30 minutes. A script was ran in Power Shell Admin command line to force the Policy to Refresh. If the Policy was not forced, the system would have took 90 minutes to update.

</p>
<br />

<p>
<img width="1660" height="927" alt="Screenshot_14-10-2026_203912_coursecareers com" src="https://github.com/user-attachments/assets/1a0b1573-b076-4268-be56-5372aa2c3ad7" />

</p>
<p>
This Lab is showing how to Reset or Configure an Agent's Password within the Group Policy settings. The Agent's name was located out of a thousand users within the Orginazation. In the settings Tab, an Agent's Account can be Renamed, Deleted, Added to a Group, or have the Account disabled.  
</p>
<br />
