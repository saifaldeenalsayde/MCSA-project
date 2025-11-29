1️⃣ Domain Controller Setup

Install and configure Active Directory Domain Services (AD DS).

Create a new forest with domain name: exam.local.

Server details:

Computer Name: PDC

IP Address: 192.168.1.2

2️⃣ Organizational Units (OUs)

Create the following top-level OUs:

HR

Sales

IT

Each OU contains:

Users

Department Group

Applied GPOs

3️⃣ User Creation

Create 2 users per department:

HR

Mohamed Zohdy

Salma Mohamed

Sales

Maha Ahmed

Alaa Kamal

IT

Moataz Yusuf

Ahmed Nabil

4️⃣ Department Groups

Create a security group for each department and add its users:

HR-Group

Sales-Group

IT-Group

5️⃣ Windows 10 Client Machine

Join a Windows 10 machine to the domain:

Computer Name: HRPC01

IP Address: 192.168.1.40

Add the IT-Group as Local Administrators on the client machine.

🔐 Group Policy Configuration
📁 HR Department GPOs

Applied only to HR users:

✔ Show only Fonts in Control Panel

Restrict Control Panel to show "Fonts" only.

✔ Remove “Properties” from This PC context menu

Disables right-click properties on "This PC".

✔ Disable Command Prompt

Prevents HR users from running cmd.exe.

✔ Disable External Storage

Disable USB storage devices for HR,
but exclude HR manager (Mohamed Zohdy) from this restriction.

🔑 Password & Security Policies (Domain Level)

Password must change every 60 days.

Minimum 6-digit password length.

Must meet complexity requirements.

Remember last 3 passwords.

Lock account for 30 minutes after 5 failed attempts.

🌐 HR Department Homepage Shortcut

Create a desktop shortcut for all HR users pointing to:

http://hrapp.exam.local

🧩 Technologies Used

Windows Server (AD DS, GPO)

Windows 10 Client

DNS

Group Policy Management Console (GPMC)

Active Directory Users and Computers (ADUC)

📘 Purpose of the Project

This project is designed to practice:

AD DS deployment

Organizational structure design

Security hardening using GPO

Managing users, groups, and permissions

Client machine domain joining

Real-world HR/Security policy enforcement
