🛡️ User Access Management System

📌 Overview:
==============
A web-based system for managing user access to software applications within an organization. It allows employees to sign up and request access, managers to approve or reject requests, and admins to manage software entries.

🚀 Features:
==============
User Registration (Sign-Up)

User Authentication (Login)

Software Creation (Admin)

Access Request Submission (Employee)

Access Approval/Rejection (Manager)

🧰 Tech Stack:
=================
Backend: Java Servlets, JSP

Database: PostgreSQL

Server: Apache Tomcat

Build Tool: Maven

👥 User Roles:
==================
Role	Capabilities
Employee	Sign up, log in, request access
Manager	Approve/reject access requests
Admin	Full access: create software, approve requests, manage settings

🧩 System Modules:
======================
🔐 Sign-Up (SignUpServlet)
Registers new users as Employee

Stores data in users table

🔑 Login (LoginServlet)
Validates user credentials

Redirects by role:

Employee → requestAccess.jsp

Manager → pendingRequests.jsp

Admin → createSoftware.jsp

💼 Software Management (SoftwareServlet):
============================================
Admins can add new software

Fields: Name, Description, Access Levels

📩 Access Requests (RequestServlet)
Employees request software access

Fields: Software, Access Type, Reason

✅ Approvals (ApprovalServlet)
Managers view and approve/reject requests

🗃️ Database Schema:
=========================
users
id, username, password, role

software
id, name, description, access_levels

requests
id, user_id, software_id, access_type, reason, status

📦 Deliverables:
======================
Java Servlet Code: SignUpServlet, LoginServlet, SoftwareServlet, RequestServlet, ApprovalServlet

JSP Pages: signup.jsp, login.jsp, createSoftware.jsp, requestAccess.jsp, pendingRequests.jsp

PostgreSQL SQL Scripts

README Setup Instructions
