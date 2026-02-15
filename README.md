<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This lab demonstrates the post-installation configuration of osTicket, focusing on the organizational setup required to manage a professional IT support workflow.<br>
The focus of this section is on defining user roles, establishing departments, and configuring Service Level Agreements (SLAs). These steps are essential for transforming a fresh installation into a structured environment capable of routing and resolving support tickets efficiently.


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop (RDP)
- Internet Information Services (IIS)
- MySQL (Database Management)
- PHP(Server-side Scripting Language)
- HeidiSQL(Database Client)

<h2>Operating Systems Used </h2>
- Windows 10</b> (21H2)

<h2>System Access & Portals</h2>
The following URLs are used to access the osTicket environment:

- <b>Staff Control Panel</b>: http://localhost/osTicket/scp <br>
  This is used by Agents and Admins to manage, assign, and resolve tickets.
- <b>End-User Help Center</b>: http://localhost/osTicket/ <br>
  The public-facing portal where clients submit tickets and check status.

<h2>Post-Installation Configuration</h2>

<h2> 1. Login & Interface Overview</h2>
To begin the configuration, you must first login. <br>

Login Credentials:
- <b>URL:</b> http://localhost/osTicket/scp
- <b>Username:</b> adminuser
- <b>Password:</b> Password1
<img width="1548" height="942" alt="Screenshot (1375)" src="https://github.com/user-attachments/assets/114affc8-1ccf-4ce7-a5af-dae7f22a9ad7" />

<h2> Admin Panel vs. Agent Panel </h2>
Once logged in, notice the tab in the top-right corner. Understanding the difference between the Admin Panel and Agent Panel is essential:<br>


- Admin Panel: This is used to set up Departments, Roles, and System Settings. <br>
- Agent Panel: This is the where tickets and users are managed.

<img width="1555" height="938" alt="Screenshot (1361)" src="https://github.com/user-attachments/assets/288c6430-c9ca-43bb-931e-04a2102bfa77" />
<img width="1559" height="948" alt="Screenshot (1362)" src="https://github.com/user-attachments/assets/46549685-a69f-46ec-a9d8-1c1e5f045368" />

<h2> 2. Configure Roles</h2>
Now that you are in the <b>Admin Panel</b>, we will create a Role to define specific permissions for your staff. Roles are used to manage staff authorizations. They establish a specific set of access rights which are granted to Agents based on their responsibilities. <br>

 1. Go to <b>Agents</b> &#8594; <b>Roles</b> <br>
 2. Click <b> Add New Roles </b> <br>
 3. Enter "Supreme Admin" <br>
 4. Navigate through the tabs (Tickets, Tasks, Acknowledgements) and check the boxes to grant full authority <br>
 5. Click <b>Add Role</b> <br>

 <h2> 3. Configure Departments</h2>
Next we will set up Departments. Departments are used to route tickets to the right people. They ensure that inquiries are directed to the correct team (such as IT or SysAdmins) rather than cluttering a single inbox. <br>
 1. Go to <b>Agents → Departments</b> <br> 
 2. Click <b>Add New Department</b> <br>
 3. Enter <b>SysAdmins</b> <br>
 4. Click <b>Create Department</b> <br>

 <h2> 4. Configure Teams</h2>
 While <b>Departments</b> categorize Agents by their primary job fuction, <b>Teams</b> allow you to group Agents from various departments to collaborate on specific tasks or projects <br>
 1. Go to <b>Agents → Teams</b> <br>
 2. Click <b>Add New Team</b> <br>
 3. Enter <b>Online Banking</b> <br>
 4. Click <b>Create Team</b> <br>  <b></b>

 <h2> 5. User Registration Settings</h2>
 To ensure the help desk is accessible to all users without barriers, we will configure the settings to allow guest ticket creation. This ensures that a user does not need a pre-existing account or login to request assistance. <br>
 1. Go to <b>Admin Panel → Settings → Users</b> <br>
 2. Locate the setting <b>"Registration Required"</b> <br>
 3. Uncheck the box that says <b>Require registration and login to create tickets</b> <br>
 4. Click <b>Save Changes</b> at the bottom of the page <br>

 <h2> 6. Configure Agents (Staff)</h2>
 Now we will add the staff members who will be processing the tickets. <br>
 1. Go to <b>Agents → Add New Agent</b> <br>
 2. <b>Agent 1: </b>Create<b> Jane Doe</b> <br>
  A. <b>Account</b>
  - Email: <b>janefake@gmail.com</b>
  - Username: <b>Jane</b>
  - Password: <b>Password1</b>
  B. <b>Access</b>
  - Department: <b>SysAdmin</b>
  - Role: <b>Supreme Admin</b>
  C. <b>Teams</b>
  - Assigned Teams: <b>Online Banking</b>
  
 3. <b>Agent 2: </b>Create<b> John Doe</b> <br>
  A. <b>Account</b>
  - Email: <b>johnfake@gmail.com</b>
  - Username: <b>John</b>
  - Password: <b>Password1</b>
  B. <b>Access</b>
  - Department: <b>Support</b>
  - Role: <b>View only</b>
    

 <h2> 7. Configure Users (Customers)</h2>
 Next we will add the Users. These are the customers who will be submitting tickets for help. Note that this is done via the <b>Agent Panel</b>  <br>
 1. Switch to <b>Agent Panel</b> on the top right link <br>
 2. Go to <b>Users</b> → <b>Add New User </b> <br>
 3. <b>User 1:</b> Create <b>Karen</b> <br>
 4. <b>User 2:</b> Create <b>Ken</b> <br>

 <h2> 8. Configure SLA (Service Level Agreements</h2>
 Now we will configure SLAs. SLAs define how quickly your team must respond to tickets based on their severity. <br>
 1. Go to <b>Admin Panel</b> → <b>Manage</b> → <b>SLA</b> <br>
 2. Add new SLA: <br>
 
  - <b>Sev-A:</b> Grace Period: 1 hour, Schedule: 24/7. <br>
  - <b>Sev-B:</b> Grace Period: 4 hours, Schedule: 24/7. <br>
  - <b>Sev-C:</b> Grace Period: 8 hours, Schedule: Business Hours. <br>

  <h2> 9. Configure Help Topics</h2>
  Last step will be to configure Help Topics. Help Topics provide a streamlined way for users to categorize their requests. By selecting a topic, the system can automatically route the ticket to the correct department and assign the appropriate priority level. <br>
 1. Go to <b>Admin Panel</b> → <b>Manage</b> → <b>Help Topics</b> <br>
 2. Click <b>Add New Help Topic</b>. <br>
 3. Add the following topics one by one: <br>

  - <b>Business Critical Outage</b>
  - <b>Personal Computer Issues</b>
  - <b>Equipment Request</b>
  - <b>Password Reset</b>
  - <b>Other</b>
 4. click <b>Click Add Topic</b> for reach entry
 



 
 
 
