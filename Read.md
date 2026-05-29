Linux User Management Lab Assignment
Overview
This project demonstrates practical Linux system administration using Kali Linux. The lab focused on user and group management, file ownership, Linux permissions, and secure access control implementation within a simulated enterprise environment.
The assignment was divided into two departments:
•	Marketing Department (Private User Files)
•	IT Department (Collaborative Shared Files)

Objectives
•	Create and manage Linux users and groups
•	Configure secure file ownership
•	Apply Linux permission models
•	Demonstrate user isolation and group collaboration
•	Verify permissions and access control using command-line tools

Environment Used
•	Kali Linux
•	Linux Terminal
•	GitHub

Part 1 — Marketing Department
Scenario
The Marketing department required private workspaces where employees could securely access only their own files.
Tasks Completed
•	Created the marketing group
•	Added five users:
	alice_m
	bob_m
	carol_m
	david_m
	emma_m
•	Added all users to the marketing group
•	Created individual report files
•	Assigned ownership to corresponding users
•	Applied 700 permissions for file privacy
Permission Model
bash id="6d3jkg" rwx------
Numeric value:
bash id="4n8rmx" 700
Meaning:
•	Owner → Full access
•	Group → No access
•	Others → No access
This configuration enforces strict user isolation and protects sensitive departmental files.

Part 2 — IT Department
Scenario
The IT department required a collaborative workspace where authorized team members could access and modify a shared project file.
Tasks Completed
•	Created the itdept group
•	Added five users:
	frank_it
	grace_it
	henry_it
	iris_it
	jack_it
•	Added all users to the itdept group
•	Created a shared file: /home/shared/itdept/project_specs.txt
•	Assigned group ownership to itdept
•	Configured collaborative access permissions
Permission Model
bash id="j8i7om" rwxrwx---
Numeric value:
bash id="bwl7z4" 770
Meaning:
•	Owner → Full access
•	Group → Full access
•	Others → No access
This configuration supports secure collaboration while preventing unauthorized access.

Verification Commands
Verify Created Users
bash id="j35xpf" cat /etc/passwd | grep '_m\|_it'
Verify Groups
```bash id=“3nhy7f” getent group marketing
getent group itdept

## Verify Files and Permissions
```bash id="egmujh"
ls -l /home/shared/marketing

ls -l /home/shared/itdept

Screenshots Included
The repository contains screenshots showing:
•	User account creation
•	Group membership verification
•	File creation
•	Ownership configuration
•	Linux permission verification

Key Skills Demonstrated
•	Linux user administration
•	Group management
•	File permission configuration
•	Access control implementation
•	Linux command-line operations
•	Enterprise security principles

Lessons Learned
Through this lab, I gained hands-on experience with Linux system administration and practical access control management. The assignment strengthened my understanding of the principle of least privilege, user isolation using 700 permissions, and secure collaboration using 770 permissions within enterprise environments.

Author
Gidraph Waburi
Notepad++ v8.9.6.1 vulnerability fixes:

 