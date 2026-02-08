<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This lab demonstrates the post-installation configuration of osTicket,focusing on the organizational setup required to manage a professional IT support workflow.<br>
The focus of this section is on defining user roles, establishing departments, and configuring Service Level Agreements (SLAs). These steps are essential for transforming a fresh installation into a structured environment capable of routing and resolving support tickets efficiently.


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (RDP)
- Internet Information Services (IIS)
- MySQL (Database Management)
- PHP(Server-side Scripting Language)
- HeidiSQL(Database Client)

<h2>Operating Systems Used </h2>
- Windows 10</b> (21H2)

<h2>System Access & Portals</h2>
The following URLs are used to access the osTicket environment:

- <b>Staff Control Panel<b/>: http://localhost/osTicket/scp
  This is used by Agents and Admins to manage, assign, and resolve tickets.
- <b>End-User Help Center<b/>: http://localhost/osTicket/
  The public-facing portal where clients submit tickets and check status

<h2>Post-Installation Configuration</h2>

<h2> 1. Login & Interface Overview</h2>
To begin the configuration, you must first login. <br>

Login Credentials:
- <b>URL:<b/> http://localhost/osTicket/scp
- <b>Username:<b/> adminuser
- <b>Password:<b/> Password1
<img width="1548" height="942" alt="Screenshot (1375)" src="https://github.com/user-attachments/assets/114affc8-1ccf-4ce7-a5af-dae7f22a9ad7" />

<b> Admin Panel vs. Agent Panel <b/>
Once logged in, notice the tab in the top-right corner. Understanding the difference between the Admin Panel and Agent Panel is essential:

-Admin Panel: This is used to set up Departments, Roles, and System Settings. <br>
-Agent Panel: This is the where tickets and users are managed.

<img width="1555" height="938" alt="Screenshot (1361)" src="https://github.com/user-attachments/assets/288c6430-c9ca-43bb-931e-04a2102bfa77" />
<img width="1559" height="948" alt="Screenshot (1362)" src="https://github.com/user-attachments/assets/46549685-a69f-46ec-a9d8-1c1e5f045368" />

<h2> 2. Configure Roles</h2>
Now that you are in the <b>Admin Panel</b>, we will create a Role to define specific permissions for your staff. Roles are used to manage staff authorizations. They establish a specific set of access rights which are granted to Agents based on their responsibilities.
 1. Go to <b>Agents</b> &#8594; <b>Roles</b> <br>
 2. Click <b>Add New Roles</b>
 3. Enter "Supreme Admin"
 4. Navigate through the tabs (Tickets, Tasks, Acknowledgements) and check the boxes to grant full authority. 
 5. Click <b>Add Role</b>

 <h2> 3. Configure Departments</h2>
Next we will set up Departments. Departments are used to route tickets to the right people. They ensure that inquiries are directed to the correct team (such as IT or SysAdmins) rather than cluttering a single inbox. 
 1. Go to Agents → Departments</b>
 2. Click <b>Add New Department</b>
 3. Enter <b>SysAdmins</b>
 4. Click <b>Create Department</b>

 <h2> 4. Configure Teams</h2>
 

