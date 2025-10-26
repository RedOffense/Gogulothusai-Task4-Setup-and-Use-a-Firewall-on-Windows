# Gogulothusai-Task4-Setup-and-Use-a-Firewall-on-Windows


Basic Firewall Configuration Lab – Windows
Overview
This project demonstrates how to configure and test basic firewall rules using Windows Defender Firewall. The objective is to block or allow network traffic on specific ports and verify those rules.

Steps Performed
Opened Windows Firewall

Accessed Windows Defender Firewall with Advanced Security from Control Panel.

Listed Current Firewall Rules

Navigated to "Inbound Rules" to review existing rules.

Added Rule to Block Port 23 (Telnet)

Created a new inbound rule to block TCP port 23.

Rule details:

Type: Port

Port: 23

Action: Block the connection

Profile: All (Domain, Private, Public)

Name: Block Telnet Port 23

Tested Block Rule

Used Telnet and PowerShell (Test-NetConnection -Port 23 -ComputerName localhost) to try connecting to port 23.

Connection failed, confirming the rule worked.

Allowed Rule for SSH (Port 22)

Added a new inbound rule to allow TCP port 22.

Rule details:

Port: 22

Action: Allow the connection

Name: Allow SSH Port 22

Removed Test Block Rule

Deleted the "Block Telnet Port 23" rule to restore settings.

Documentation

Screenshots of Inbound Rules, rule creation windows, and test results are included in the repo.

How Windows Firewall Filters Traffic
Windows Firewall filters incoming and outgoing network traffic based on rules you configure. Rules specify which ports, protocols, programs, and IP addresses are allowed or blocked. When a connection matches a block rule, traffic is dropped; when it matches an allow rule, traffic passes.
