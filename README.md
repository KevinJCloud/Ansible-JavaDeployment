Java Application Deployment using Ansible

Overview
This project automates the end-to-end deployment of a Java application using Ansible.  
It eliminates manual setup by provisioning the server, building the application, and managing the service.

---

Features

- Install required packages (Java, Git)
- Download and configure Apache Maven
- Clone application code from Git repository
- Build application using Maven (`mvn clean install`)
- Locate and deploy generated JAR file
- Create and manage systemd service
- Restart service only when changes occur (using handlers)
- Fully idempotent playbook (safe to run multiple times)

---

Project Structure

Ansible-JavaDeployment/
│
├── roles/
│ └── java/
│ ├── tasks/
│ │ └── main.yml
│ ├── handlers/
│ │ └── main.yml
│ ├── templates/
│ │ ├── maven.sh.j2
│ │ └── javaapp.service.j2
│ └── vars/
│ └── main.yml
│
├── app.yaml
└── README.md


How to Run

1. Clone the repository
2.  Update inventory file
3. Run playbook

Deployment Flow
Install Java and Git
Download and configure Maven
Clone application source code
Build JAR using Maven
Deploy JAR to target path
Configure systemd service
Start/restart service when needed

<img width="362" height="171" alt="image" src="https://github.com/user-attachments/assets/3aca0a9c-1176-4048-a36f-e34fb02156b3" />

