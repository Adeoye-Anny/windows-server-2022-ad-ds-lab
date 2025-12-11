# Windows Server 2022 Active Directory Domain Services Lab

  ![windows-server-active-directory-and-it-support](https://github.com/user-attachments/assets/945faa0a-a813-476a-a3e4-d17b9760e6a5)

### 5. Creating Organizational Units (OUs)

  In this stage I began organizing my domain by creating OUs. This structure makes administration easier and keeps users, groups, and computers separated in a clean         hierarchy.

### 5.1 Opening Active Directory Users and Computers (ADUC)

  1. I clicked Start → Server Manager → Tools → Active Directory Users and Computers.
  2. ADUC opened and displayed my domain lab.local.
    <img width="1920" height="1041" alt="image" src="https://github.com/user-attachments/assets/fb34ec0d-0806-470b-a65a-1efa3e30a481" />
    

### 5.2 Creating New OUs

  1. In the left pane, I right-clicked my domain name lab.local.
  2. I selected New → Organizational Unit.
    <img width="1918" height="1039" alt="image" src="https://github.com/user-attachments/assets/4ed5472f-30ac-4a3c-88cf-568fd9ec6613" />
    I created 3 OUs: USA, Europe, and Asia
  
  3. I created the following OUs under the above OUs:
    * Computer
    * Users
    * Server
    <img width="1920" height="1039" alt="image" src="https://github.com/user-attachments/assets/5dc7a002-0b0c-4b9c-8044-403d5d36f214" />

  5. I unchecked Protect container from accidental deletion where needed.

### 6. Creating Users & Groups

  Now that the OUs were created, I populated the domain with sample users and role-based security groups.

### 6.1 Creating Users

  1. I opened the Users OU.
  2. I right-clicked inside the OU and selected New → User.
  3. I created these sample accounts:
    * Samson Anny
    * Mary Smith
    * IT_Admin
  4. I set strong passwords and enabled User must change password at next logon for regular users.
    <img width="1920" height="1038" alt="image" src="https://github.com/user-attachments/assets/199bae39-394a-4e50-b502-88795121cd66" />


### 6.2 Creating Security Groups

Security groups allow role-based access control.

  1. I opened the Groups OU.
  2. I right-clicked and selected New → Group.
  3. I created:
    * HR_Staff
    * IT_Staff
    * Admins
  4. I ensured:
    *  Group scope: Global
    *  Group type: Security
  5. I added users to each group as needed (ex. Samson Anny → HR_Staff).
    <img width="1920" height="1036" alt="image" src="https://github.com/user-attachments/assets/5771e7e5-73de-45d2-a3c0-7d93d9d2df54" />




