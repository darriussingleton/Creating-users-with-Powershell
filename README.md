# Creating-users-with-Powershell

<h1>Active Directory: Creating Users With a Powershell Script 🪟</h1>
In this portion of the Active Directory lab I use a custom Powershell Script to add 10,000 new users into our previously created Domain. I go through the process of Running Powershell ISE as an Administrator, saving a script as a Powershell file, running the script and observing User creation. From here I confirm that the users were successfully added and then I test the operation by choosing one of the users at random to log into our Client Machine remotely.
(Link Back to Main Project Contents Page is at the Bottom of this Repo)

<h2>Environments and Technologies Used</h2>
Lenovo Ideapad 5 Pro 16gb AMD Ryzen 7
Microsoft Azure Resource Group
Microsoft Azure Windows 10 Pro version 22H2 - x64 Gen2 Virtual Machine
Microsoft Azure Windows Server 22 Datacenter: Azure Edition - x64 Gen2 Virtual Machine

<h2>Operating Systems Used</h2>
Local Windows 11 Home Version 21H2
Windows 10 Pro Version 22H2 Virtual Machine
Windows Server 22 Datacenter: Azure Edition - x64 Gen2 Virtual Machine

<h2>List of Prerequisites</h2>
Microsoft Azure Subscription

<br>

<h2>Remote Desktop Setup and User Creation</h2>

<h3>1. Setup Remote Desktop for Non-Administrative Users on Client-1</h3>

<ol>
  <li>
    <p>Log into Client-1 using the domain administrator account: <code>mydomain.com\jane_admin</code>.</p>
  </li>
  <li>
    <p>Open System Properties (you can search for "system properties" in the Windows search bar).</p>
  </li>
  <li>
    <p>Click on the "Remote Desktop" tab.</p>
  </li>
  <li>
    <p>Select the option to allow remote connections to this computer.</p>
  </li>
  <li>
    <p>Click "Select Users..." and add the "Domain Users" group to the list of allowed users.</p>
  </li>
  <li>
    <p>You can now log into Client-1 as a normal, non-administrative domain user.</p>
    <p><strong>Note:</strong> In a real-world environment, this configuration would typically be managed via Group Policy for centralized control.</p>
  </li>
</ol>

<h3>2. Create Additional Users and Test Remote Login</h3>

<ol>
  <li>
    <p>Log into DC-1 as <code>mydomain.com\jane_admin</code>.</p>
  </li>
  <li>
    <p>Open PowerShell ISE as an administrator.</p>
  </li>
  <li>
    <p>Create a new file and paste the provided PowerShell script (for user creation) into it.</p>
    <p><strong>Note:</strong> Ensure you have the script content available. The script should create multiple users within the _EMPLOYEES OU.</p>
  </li>
  <li>
    <p>Run the script.</p>
  </li>
  <li>
    <p>Open Active Directory Users and Computers (ADUC) and verify that the new user accounts are created within the <code>_EMPLOYEES</code> OU.</p>
  </li>
  <li>
    <p>Attempt to log into Client-1 using one of the newly created user accounts. Refer to the script for the password.</p>
  </li>
</ol>
