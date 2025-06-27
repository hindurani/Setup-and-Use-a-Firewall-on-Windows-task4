# Setup-and-Use-a-Firewall-on-Windows-Linux-task4
Objective:
Configure and test basic firewall rules using Windows Defender Firewall to allow or block network traffic, as part of the Eleyate Cybersecurity Internship Task 4.

Task Description:
This task involves setting up firewall rules to block inbound traffic on port 23 (Telnet), testing the rule, and documenting the process. The deliverables include screenshots, configuration steps, a summary of firewall traffic filtering, and answers to provided interview questions.

Steps Performed:
Opened Windows Defender Firewall:
Used Win + R, typed control firewall.cpl, and pressed Enter to access the firewall settings.
Listed Current Firewall Rules:
Navigated to Advanced Settings > Inbound Rules in Windows Defender Firewall with Advanced Security.
Captured a screenshot of the existing rules.

Added a Rule to Block Inbound Traffic on Port 23 (Telnet):
In Advanced Settings, selected Inbound Rules > New Rule.
Chose Port > TCP > Specific local ports: 23 > Block the connection.
Applied the rule to all profiles (Domain, Private, Public).
Named the rule "Block Telnet Port 23" and saved it.
Took a screenshot of the new rule.

Tested the Rule:
Used PowerShell to run Test-NetConnection -ComputerName localhost -Port 23.
Observed the connection failed, confirming the rule worked.
Documented the command and output with a screenshot.

Removed the Test Block Rule:
In Advanced Settings, located the "Block Telnet Port 23" rule, right-clicked, and deleted it.
Verified removal with a screenshot of the updated Inbound Rules list.

Documented the Process:
Recorded all steps in firewall_steps.txt.
Included screenshots for each major step.

Firewall Traffic Filtering:
A firewall filters network traffic by evaluating packets against predefined rules based on attributes like port, protocol, and source/destination IP. In this task, Windows Defender Firewall was configured to block inbound traffic on port 23 (Telnet), preventing unauthorized access to this insecure protocol. This demonstrates how firewalls control network access to enhance security by allowing only permitted connections while blocking potential threats.

Screenshots:
Initial Rules: screenshots/initial_rules.png
Block Rule Creation: screenshots/block_port23.png
Test Result: screenshots/test_result.png
Rule Deletion: screenshots/after_rule_deletion.png

Files:
firewall_steps.txt: Detailed steps and commands used for firewall configuration.
screenshots/: Folder containing screenshots of the firewall configuration process.

Tools Used:
Windows Defender Firewall (built-in Windows tool).
PowerShell for testing connectivity (Test-NetConnection).
Windows Snipping Tool for capturing screenshots.

Notes:
Administrative access was required to modify firewall settings.
Telnet client was not enabled by default; used Test-NetConnection for testing to avoid enabling unnecessary services.
All steps were performed on a Windows 11 machine.
