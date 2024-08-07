# Honeynet-Configuration

## Objective
The objective of this lab project is to create a honeynet within the Microsoft Azure cloud platform. A honeynet is a network set up with intentional vulnerabilities to attract and monitor cyberattackers. By setting up a honeynet, I aim to observe and analyze the behaviors and techniques of attackers, thereby gaining insights into current threat landscapes and improving certain defensive measures.

## Technologies Employed
Microsoft Azure: Cloud computing platform used for creating and managing virtual machines and network configurations.
Windows and Linux Virtual Machines: Instances set up to mimic real-world systems for attackers to target.
Network Security Groups (NSGs): Azure’s firewall service used to control inbound and outbound traffic to virtual machines.
SQL Server: Database server configured as an additional honeypot resource to attract database-specific attacks.

## Methodologies And Execution
### Create Three Different Virtual Machines:

![image](https://github.com/user-attachments/assets/64647148-a1cd-4a73-818a-e0c47b2c0a3c)

- Set up two Windows-based virtual machines and one Linux-based virtual machine in Azure. These VMs will serve as the primary targets for potential attackers.
- Ensure each VM is configured with basic operating system installations and necessary network settings.

### Configure the NSGs Inbound Traffic Rule to Allow All Public Traffic to Access Them:

![image](https://github.com/user-attachments/assets/26fd855d-4a75-49d2-aa7a-80bc568d7b5d)

- Create and attach NSGs to each virtual machine, configuring them to allow all inbound traffic from any source. This makes the VMs easily accessible to attackers, increasing the likelihood of attracting malicious activity.
- Specific rules in the NSGs will permit all types of traffic, removing any restrictions that might prevent an attack.

### Disable the Firewalls on the Windows and Linux Machines:

![image](https://github.com/user-attachments/assets/c16a64c7-c893-48ea-b736-bd3e52e88a08)
![image](https://github.com/user-attachments/assets/cee0c247-4670-4fd7-a9f9-2f128f12b72c)

- Disable the built-in firewalls on both Windows and Linux VMs to further expose them and ensure no network traffic is filtered out, making the systems more appealing targets.

### Set Up and Configure a SQL Server as Additional Honeypot Resource:

![image](https://github.com/user-attachments/assets/7ac0addb-d77c-47bc-8868-9b2dcc12f08f)

- Install and configure an SQL Server instance on a separate VM or within one of the existing VMs.
- Configure the SQL Server to accept inbound connections from any source, making it an attractive target for database attacks.

> Upon completing the honeynet setup and monitoring, I observed a wide range of attack vectors, but most notably the brute-force login attempts. Common patterns in attacker behaviors, such as the use of specific IP ranges and techniques to exploit well-known vulnerabilities, were identified. A notable portion of these attacks originated from specific geographic regions, illustrating the global nature of cyber threats. The disabled firewalls on the VMs resulted in numerous successful exploitations, emphasizing the critical need for robust security configurations in real-world environments.

## Conclusion
The honeynet project in Microsoft Azure was a valuable exercise in understanding and mitigating cyber threats. By setting up vulnerable systems and observing attacker behaviors, I have gained critical insights into the techniques and tools used by adversaries. This project not only enhanced my practical skills and knowledge but also highlighted the importance of proactive and well-configured security measures in protecting against cyberattacks. The findings and experiences from this project will undoubtedly inform future cybersecurity initiatives and contribute to the ongoing effort to secure digital environments.






