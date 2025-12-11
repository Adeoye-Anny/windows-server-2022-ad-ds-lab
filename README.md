# Windows Server 2022 Active Directory Domain Services Lab

  ![windows-server-active-directory-and-it-support](https://github.com/user-attachments/assets/945faa0a-a813-476a-a3e4-d17b9760e6a5)

### 5. Creating Organizational Units (OUs)

  In this stage I began organizing my domain by creating OUs. This structure makes administration easier and keeps users, groups, and computers separated in a clean         hierarchy.

#### 5.1 Opening Active Directory Users and Computers (ADUC)

  1. I clicked Start → Server Manager → Tools → Active Directory Users and Computers.
  2. ADUC opened and displayed my domain lab.local.
    <img width="1920" height="1041" alt="image" src="https://github.com/user-attachments/assets/fb34ec0d-0806-470b-a65a-1efa3e30a481" />
    

#### 5.2 Creating New OUs

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

#### 6.1 Creating Users

  1. I opened the Users OU.
  2. I right-clicked inside the OU and selected New → User.
  3. I created these sample accounts:
    * Samson Anny
    * Mary Smith
    * IT_Admin
  4. I set strong passwords and enabled User must change password at next logon for regular users.
    <img width="1920" height="1038" alt="image" src="https://github.com/user-attachments/assets/199bae39-394a-4e50-b502-88795121cd66" />


#### 6.2 Creating Security Groups

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


### 7. Configuring Group Policy (GPO)
I created and linked Group Policy Objects to control domain behavior. This shows I understand centralized management of users and computers.

#### 7.1 Opening Group Policy Management
  1. On the domain controller, I opened:
     Server Manager → Tools → Group Policy Management
  2. The GPMC console displayed all OUs and the default domain policy.
     <img width="1920" height="1039" alt="image" src="https://github.com/user-attachments/assets/2672ef7c-1cd2-438f-8e70-7d5ecf7e433d" />


#### 7.2 Creating a New GPO
Example GPO: Paasword Policy
  1. In GPMC, I right-clicked the Users OU.
  2. I selected Create a GPO in this domain, and Link it here.
  3. I named it:
     Password Policy
  4. I right-clicked the new GPO and selected Edit.
     <img width="1920" height="1035" alt="image" src="https://github.com/user-attachments/assets/cdcbd7f3-d364-4935-a06e-108dcb2360c4" />


#### 7.3 Configuring the GPO Settings
Inside the GPO editor:
  1. I navigated to:
     Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Password Policy
  2. I adjusted the Maximum Password length to (12 character), the minimum and maximum password age (30 days - 90 days). 
  3. Password Policy GPO successfully created and editted.
    <img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/9fddf39e-0c25-4109-9648-10dfffb38da6" />

  4. After completing the first policy, I proceeded to create more additional Group Policy Objects  and configured them to demonstrate centralized management of user            settings and resources within the domain.
      * Drive Mapping
        <img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/5a1b311c-6ead-4876-a991-6f44046b00d9" />

      * Desktop Wallpaper
        <img width="1919" height="1036" alt="image" src="https://github.com/user-attachments/assets/2bf77b2c-340a-4001-ab1a-071c65095957" />

      * Restrict Access to Control Panel
        <img width="1920" height="1037" alt="image" src="https://github.com/user-attachments/assets/ec941782-00a8-4da2-afd4-901e2e314942" />
      
      * USB Storage
        <img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/37653bc1-1dde-4e8f-87fc-f80d04ab846d" />
      
      * Account Lockout Policy
        To strengthen domain security, I configured the Account Lockout Policy in the Default Domain Policy.
        I set the following values:
          * Account lockout threshold: 3 failed attempts
          * Account lockout duration: 30 minutes
          * Reset lockout counter after: 30 minutes
        This ensures user accounts are protected from repeated unauthorized login attempts.

        <img width="1920" height="1036" alt="image" src="https://github.com/user-attachments/assets/6e12c7e9-1a9f-40ef-819a-f274c1bc6c4f" />





