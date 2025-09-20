# Active-Directory-Security-Project
### Overview
This repository serves as a documentation for design and deployment of a Windows Active Directory(AD) Lab on AWS. It also Captures the Security Hardening and best practices done to secure the AD environment. Further, it highlights some of the offensive and defensive techniques for exploiting and mitigating AD vulnerabilities.

This repository serves as a documentation for the Step-by-step build up of a Windows Active Directory Lab on AWS. It also Captures the Security Hardening and best practices done to secure the AD environment. Further, it highlights some of the offensive and defensive techniques for exploiting and mitigating AD vulnerabilities.

### 📂 Repository Contents:

1. Introduction
2. Lab architecture
3. step by step Lab Build
4. AD Defensive measures and Security Hardening
5. AD Offensive security Test
6. References

### Introduction

Since moving in the professional arena, I’ve ovbserved that Microsoft Active Directory is the dominant solution for managing Windows domain networks within organisations. Because of its central role in the Windows domain management, adversaries are often attracted to discovering and exploiting vulnerabilities in the Active Directory ecosystem.

To continue developing skills as a Systems Security Analyst, I built a simple Active Directory penetration-testing lab on AWS using several online articles and YouTube videos (listed in the references). The aim of the lab is to provide a safe environment where I can practice both offensive and defensive techniques for exploiting and mitigating AD vulnerabilities.


###  Lab Architecture

The lab is built inside a dedicated AWS VPC and contains:

1 Domain Controller (DC01 i.e A Windows Server 2025 promoted to Domain Controller.

2 Window 11 workstations (WS01, WS02) EC2 instances joined to the AD domain.

1 Kali Linux VM as the attacker machine for offensive security practice.

A Jump/Bastion Host in public subnet: for secure access point for RDP/SSH into the private subnet.


#### Networking & Security Groups:

VPC: AD-Lab-VPC (CIDR: 10.0.0.0/16)

Public Subnet: 10.0.1.0/24 → for Jump/Bastion Host or NAT access.

Private Subnet: 10.0.2.0/24 → for DC, Workstations, Kali.

Security Groups configured for realistic AD communication (DNS, Kerberos, LDAP, SMB, RPC, RDP).

A NAT gateway for private instances to reach Internet for updates.

![AD Lab architecture diagram](./ADLabArchitecture.png)


#### The lab provides a safe and controlled environment to:

1. Understand how Windows Active Directory works in practice.

2. Explore common AD vulnerabilities exploited by attackers.

3. Practice defensive and hardening strategies for AD.

4. Gain hands-on experience with offensive security tools using Kali Linux.

⚠️ Disclaimer: This project is for educational and lab use only. The captured techniques are not for use in production environments or against systems you don’t own/authorize.


### ⚙️ Pre-requisites

- AWS account with free-tier enabled.

- Basic knowledge of EC2, VPC, and Security Groups.

- IAM user with sufficient privileges to create VPC, EC2, and IAM roles
  
- Knowledge of Domain Management using Windows Active directory
  
- Knowledge of System's Security and best practices
  

#### 📚 References

Ethical Hacking Lessons: Building Free Active Directory Lab in Azure

AWS Documentation: VPCs and Subnets

Microsoft Learn: Active Directory Domain Services

Various YouTube tutorials on AD labs & pentesting.


### 🙋 K. Zeddie
Graduate Electrical & Telecommunications Engineer, Systems & Security Enthusiast and Exploring Cloud and Network Security Architecture.
