<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This lab demonstrates the post-installation configuration of osTicket, focusing on the organizational setup required to manage a professional IT support workflow.<br>
The focus of this section is on defining user roles, establishing departments, and configuring Service Level Agreements (SLAs). These steps are essential for transforming a fresh installation into a structured environment capable of routing and resolving support tickets efficiently.

<h2>(Coming Soon) Video Demonstration</h2>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop (RDP)
- Internet Information Services (IIS)
- MySQL (Database Management)
- PHP(Server-side Scripting Language)
- HeidiSQL(Database Client)

<h2>Operating Systems Used </h2>
- Windows 10 (21H2)

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
<br>
<br>
<img width="1548" height="942" alt="Screenshot (1375)" src="https://github.com/user-attachments/assets/114affc8-1ccf-4ce7-a5af-dae7f22a9ad7" />

<h2> Admin Panel vs. Agent Panel </h2>
Once logged in, notice the tab in the top-right corner. Understanding the difference between the Admin Panel and Agent Panel is essential:<br>


- Admin Panel: This is used to set up Departments, Roles, and System Settings. <br>
- Agent Panel: This is where tickets and users are managed.
<br>
<br>
<img width="1555" height="938" alt="Screenshot (1361)" src="https://github.com/user-attachments/assets/288c6430-c9ca-43bb-931e-04a2102bfa77" />
<img width="1559" height="948" alt="Screenshot (1362)" src="https://github.com/user-attachments/assets/46549685-a69f-46ec-a9d8-1c1e5f045368" />

<h2> 2. Configure Roles</h2>
Now that you are in the <b>Admin Panel</b>, we will create a Role to define specific permissions for your staff. Roles are used to manage staff authorizations. They establish a specific set of access rights which are granted to Agents based on their responsibilities. <br>

 1. Go to <b>Agents</b> &#8594; <b>Roles</b> <br>
 2. Click <b> Add New Roles </b> <br>
 3. Enter "Supreme Admin" <br>
 4. Navigate through the tabs (Tickets, Tasks, Acknowledgements) and check the boxes to grant full authority <br>
 5. Click <b>Add Role</b> <br>
<br>
<br>
<img width="1557" height="967" alt="Screenshot (1390)" src="https://github.com/user-attachments/assets/dc587f27-d19d-45e6-aaa6-ac604f2acc89" />
<img width="1557" height="971" alt="Screenshot (1391)" src="https://github.com/user-attachments/assets/0c33002d-63f3-43c7-8d5a-8da6f7a2fc20" />
<img width="1550" height="969" alt="Screenshot (1392)" src="https://github.com/user-attachments/assets/a1492213-989c-4350-89bf-dfba94ab220d" />
<img width="1560" height="969" alt="Screenshot (1393)" src="https://github.com/user-attachments/assets/845d10af-3880-48af-9c1a-9cb850dda040" />
<img width="1553" height="974" alt="Screenshot (1394)" src="https://github.com/user-attachments/assets/7179d99c-f71e-428e-90d7-5631928ab68d" />
<img width="1560" height="968" alt="Screenshot (1395)" src="https://github.com/user-attachments/assets/1fa659ee-00b8-4c10-9dbe-3b65ef0c2414" />
<img width="1552" height="974" alt="Screenshot (1396)" src="https://github.com/user-attachments/assets/38bf0470-8bef-4824-9a0d-9dc040b84417" />
<img width="1558" height="974" alt="Screenshot (1397)" src="https://github.com/user-attachments/assets/58132489-4aec-41fb-aebd-07a0f6aec39b" />
<img width="1547" height="979" alt="Screenshot (1398)" src="https://github.com/user-attachments/assets/24f27fd0-d8e6-4384-aedc-f77e2b3990b1" />


 <h2> 3. Configure Departments</h2>
Next we will set up Departments. Departments are used to route tickets to the right people. They ensure that inquiries are directed to the correct team (such as IT or SysAdmins) rather than cluttering a single inbox. <br>
 1. Go to <b>Agents → Departments</b> <br> 
 2. Click <b>Add New Department</b> <br>
 3. Enter Parent: <b>Top Level Department</b> and Name: <b>SysAdmins</b> <br>
 4. Click <b>Create Department</b> <br>
<br>
<br>
<img width="1558" height="976" alt="Screenshot (1399)" src="https://github.com/user-attachments/assets/3eaa0934-5249-44c0-98b3-c3e2bd01f357" />
<img width="1549" height="972" alt="Screenshot (1400)" src="https://github.com/user-attachments/assets/6f566bb8-e937-4043-8b22-85619eff54f8" />
<img width="1555" height="1138" alt="Screenshot (1401)" src="https://github.com/user-attachments/assets/96c61f6f-30d2-40a8-8932-65bed8a272d4" />
<img width="1547" height="1136" alt="Screenshot (1402)" src="https://github.com/user-attachments/assets/8ce3316b-0525-4a61-bda0-7fb135c4b3aa" />

 <h2> 4. Configure Teams</h2>
 While <b>Departments</b> categorize Agents by their primary job function, <b>Teams</b> allow you to group Agents from various departments to collaborate on specific tasks or projects. <br>
 1. Go to <b>Agents → Teams</b> <br>
 2. Click <b>Add New Team</b> <br>
 3. Enter <b>Online Banking</b> <br>
 4. Click <b>Create Team</b> <br>  
<br>
<br>
<img width="1557" height="1140" alt="Screenshot (1403)" src="https://github.com/user-attachments/assets/222c6b1a-e320-4f59-adcc-0b88550200f6" />
<img width="1552" height="1136" alt="Screenshot (1404)" src="https://github.com/user-attachments/assets/6597fa89-6d77-4792-a871-0c9daa67de7b" />
<img width="1558" height="1126" alt="Screenshot (1405)" src="https://github.com/user-attachments/assets/66739919-46fd-40d2-9452-650a7b2e8a15" />

 <h2> 5. User Registration Settings</h2>
 To ensure the help desk is accessible to all users without barriers, we will configure the settings to allow guest ticket creation. This ensures that a user does not need a pre-existing account or login to request assistance. <br>
 1. Go to <b>Admin Panel → Settings → Users</b> <br>
 2. Locate the setting <b>"Registration Required"</b> <br>
 3. Uncheck the box that says <b>Require registration and login to create tickets</b> <br>
 4. Click <b>Save Changes</b> at the bottom of the page <br>
<br>
<br>
<img width="1550" height="1136" alt="Screenshot (1407)" src="https://github.com/user-attachments/assets/6b2f60db-0555-48a8-a1d0-2100fccb290c" />
<img width="1555" height="1136" alt="Screenshot (1409)" src="https://github.com/user-attachments/assets/0b192fd8-4069-40fd-b114-e3354d3059c7" />

 <h2> 6. Configure Agents (Staff)</h2>
 Now we will add the staff members who will be processing the tickets. <br>
 
1. Go to **Agents → Add New Agent**
2. **Create Agent 1**
    * **Account:**
        * Name: **Jane Doe**
        * Email: **janefake@gmail.com**
        * Username: **Jane**
        * Password: **Password1**
    * **Access:**
        * Department: **SysAdmin**
        * Role: **Supreme Admin**
    * **Teams:**
        * Assigned Teams: **Online Banking**
<br>
<br>
<img width="1557" height="1135" alt="Screenshot (1410)" src="https://github.com/user-attachments/assets/cf592144-998d-4714-899c-db265e931384" />
<img width="1551" height="1134" alt="Screenshot (1411)" src="https://github.com/user-attachments/assets/82302fd2-4f9c-4afc-8c98-e1cfbc331806" />
<img width="1563" height="1152" alt="Screenshot (1413)" src="https://github.com/user-attachments/assets/da1ed4bb-ab9d-46d0-8033-eefe434f241f" />
<img width="1556" height="1136" alt="Screenshot (1414)" src="https://github.com/user-attachments/assets/bf138385-511d-494b-90c1-f7a74c62ca96" />
<img width="1557" height="1139" alt="Screenshot (1415)" src="https://github.com/user-attachments/assets/0ac86d16-f53f-4464-98ac-eeab7f8073e9" />
<img width="1543" height="1129" alt="Screenshot (1416)" src="https://github.com/user-attachments/assets/2161bbc9-04a6-4624-a30a-68ef0df7cbd4" />

3. **Create Agent 2**
    * **Account:**
          * Name: **John Doe**
        * Email: **johnfake@gmail.com**
        * Username: **John**
        * Password: **Password1**
    * **Access:**
        * Department: **Support**
        * Role: **View only**
<br>
<br>
<img width="1555" height="1142" alt="Screenshot (1418)" src="https://github.com/user-attachments/assets/49c2eaf0-10ed-4eba-aba1-349387e66923" />
<img width="1558" height="1146" alt="Screenshot (1419)" src="https://github.com/user-attachments/assets/649b8037-4c64-48c7-816a-d228fe494e96" />
<img width="1415" height="1169" alt="Screenshot (1014)" src="https://github.com/user-attachments/assets/46b82fa8-835b-4e7d-b8e2-21ce1dafe790" />


 <h2> 7. Configure Users (Customers)</h2>
 Next we will add the Users. These are the customers who will be submitting tickets for help. Note that this is done via the <b>Agent Panel</b>.  <br>
 
1. Switch to **Agent Panel** (top right link)
2. Go to **Users → Add New User**
3. **Create User 1**
    * **Account:**
        * Name: **Karen**
        * Email: **Karen@gmail.com**
4. **Create User 2**
    * **Account:**
        * Name: **Ken**
        * Email: **Ken@gmail.com**
     
<br>
<br>
<img width="1551" height="1146" alt="Screenshot (1426)" src="https://github.com/user-attachments/assets/0cb9e69f-0e31-4664-b5af-7af55c23ee2a" />   
<img width="1553" height="1148" alt="Screenshot (1427)" src="https://github.com/user-attachments/assets/18d73f57-6418-42d8-aa93-82682de4d752" />   
<img width="1552" height="1123" alt="Screenshot (1428)" src="https://github.com/user-attachments/assets/64fbc9b0-d0fe-4dd3-98a0-0924eb68714c" />
<img width="1552" height="1130" alt="Screenshot (1429)" src="https://github.com/user-attachments/assets/3443ef10-efce-4339-ac2f-acc95da95c64" />
<img width="1554" height="1139" alt="Screenshot (1430)" src="https://github.com/user-attachments/assets/78eec187-f212-44ec-8ee1-f2a0750c5be1" />
<img width="1544" height="1128" alt="Screenshot (1431)" src="https://github.com/user-attachments/assets/567e5268-76a7-4bd2-afb6-dbf19f309280" />
<img width="1548" height="1135" alt="Screenshot (1432)" src="https://github.com/user-attachments/assets/07447929-8f60-4a2d-b502-3aa81c5de3b5" />
<img width="1549" height="1128" alt="Screenshot (1433)" src="https://github.com/user-attachments/assets/a06f1ac5-4e1b-4f7c-8330-e3c3045f7e66" />

 <h2> 8. Configure SLA (Service Level Agreements)</h2>
 Now we will configure SLAs. SLAs define how quickly your team must respond to tickets based on their severity. <br>
 1. Go to <b>Admin Panel</b> → <b>Manage</b> → <b>SLA</b> <br>
 2. Add new SLA: <br>
 
  - <b>Sev-A:</b> Grace Period: 1 hour, Schedule: 24/7. <br>
  - <b>Sev-B:</b> Grace Period: 4 hours, Schedule: 24/7. <br>
  - <b>Sev-C:</b> Grace Period: 8 hours, Schedule: Business Hours. <br>
<br>
<br>
<img width="1547" height="1129" alt="Screenshot (1434)" src="https://github.com/user-attachments/assets/7a3a52f2-b55e-4faa-bdb7-d75529e12d04" />
<img width="1552" height="1136" alt="Screenshot (1435)" src="https://github.com/user-attachments/assets/67c3fc15-5a79-40f0-bf8e-20de0041ba6b" />
<img width="1554" height="1134" alt="Screenshot (1436)" src="https://github.com/user-attachments/assets/1b003531-60de-465e-ac5c-073734256a3e" />
<img width="1553" height="1144" alt="Screenshot (1437)" src="https://github.com/user-attachments/assets/ab0c8ff9-7936-4aa6-a4b0-209725eeab5b" />
<img width="1553" height="1141" alt="Screenshot (1438)" src="https://github.com/user-attachments/assets/f85343b3-6fbf-4ea0-824f-0bbe3dd0d2c2" />
<img width="1556" height="1125" alt="Screenshot (1440)" src="https://github.com/user-attachments/assets/05dd3e5f-8ee5-4b4c-99bb-58badd6381af" />
<img width="1561" height="1131" alt="Screenshot (1441)" src="https://github.com/user-attachments/assets/d52436d3-5110-4042-a242-430bcc1e475b" />
<img width="1553" height="1133" alt="Screenshot (1442)" src="https://github.com/user-attachments/assets/68ade58e-8bad-4aad-b04d-bea5edabe144" />
<img width="1550" height="1132" alt="Screenshot (1443)" src="https://github.com/user-attachments/assets/d8a74640-4d1a-4d2b-a957-f9b231753377" />

  <h2> 9. Configure Help Topics</h2>
  Last step will be to configure Help Topics. Help Topics provide a streamlined way for users to categorize their requests. By selecting a topic, the system can automatically route the ticket to the correct department and assign the appropriate priority level. <br>
 1. Go to <b>Admin Panel</b> → <b>Manage</b> → <b>Help Topics</b> <br>
 2. Click <b>Add New Help Topic</b>. <br>
 3. Add the following topics one by one: <br>

  - Topic: <b>Business Critical Outage Parent</b> Parent Topic: <b>Report a Problem</b>
  - Topic: <b>Personal Computer Issues</b> Parent Topic: <b>Report a Problem</b>
  - Topic: <b>Equipment Request</b> Parent Topic: <b>General Inquiry</b>
  - Topic: <b>Password Reset</b> Parent Topic: <b>Report a Problem</b>
  - Topic: <b>Other</b> Parent Topic: <b>General Inquiry</b>
 4. Click <b> Add Topic</b> for each entry.
<br>
<br>
<img width="1550" height="1138" alt="Screenshot (1445)" src="https://github.com/user-attachments/assets/f3689ae2-4922-40f2-bef8-4a2c3e14419a" />
<img width="1554" height="1130" alt="Screenshot (1446)" src="https://github.com/user-attachments/assets/f214e73e-cf6c-4525-a54c-9943564022df" />
<img width="1562" height="1142" alt="Screenshot (1447)" src="https://github.com/user-attachments/assets/4bc8d26d-8c47-4586-93ee-80e26ebd36a8" />
<img width="1560" height="1140" alt="Screenshot (1448)" src="https://github.com/user-attachments/assets/7b083305-a2f1-48f2-bdc1-fdd63c0be0f1" />
<img width="1555" height="1126" alt="Screenshot (1449)" src="https://github.com/user-attachments/assets/a95dafc4-f340-4248-aa20-1afcc2fc7633" />
<img width="1560" height="1125" alt="Screenshot (1450)" src="https://github.com/user-attachments/assets/9391f51a-0b46-457d-9f6c-79281b06d112" />

<h2>Conclusion</h2>
 With the core infrastructure, including roles, departments, and routing rules, now established, the system is fully prepared to handle and categorize incoming tickets efficiently. <br>

 - [Click here for next step: osTicket: Ticket Lifecycle Examples](https://github.com/JahdaiF/ticket-lifecycle)
