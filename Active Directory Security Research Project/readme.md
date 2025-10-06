# USAGE.md — AD Pentesting Lab Exercises

> Practical exercises (offensive & defensive) for your AWS Active Directory lab.
> Use only in your isolated lab environment. Take AMIs/snapshots before any offensive testing.

---

## Table of contents
1. [Overview & Purpose](#overview--purpose)
2. [Prerequisites](#prerequisites)
3. [Lab preparation & safety checklist](#lab-preparation--safety-checklist)
4. [Environment setup commands (safe)](#environment-setup-commands-safe)
5. [Defensive exercises & monitoring](#defensive-exercises--monitoring)
   - [Enable and collect Windows logging](#enable-and-collect-windows-logging)
   - [Hunt rules and detection ideas](#hunt-rules-and-detection-ideas)
   - [Hardening & remediation steps](#hardening--remediation-steps)
7. [Restore & cleanup](#restore--cleanup)
8. [References & further reading](#references--further-reading)

---

## Overview & Purpose
This document gives you a **structured set of lab exercises** to practice both offensive techniques and defensive detections in an Active Directory environment. Each exercise includes objectives, prerequisites, safe commands to prepare the environment, and high-level steps to perform and defend against the technique. Do **not** perform these attacks outside environments you own or are authorized to test.

---

## Prerequisites
- AWS lab up with: `DC01` (Domain Controller), `WS01` and `WS02` (domain-joined workstations), `KALI01` (attacker). See `README.md`.
- Administrative access to DC or ability to create domain users and groups.
- Tools (install on Kali / Windows as needed): `impacket`, `crackmapexec`, `bloodhound/SharpHound`, `Responder`, `hashcat` (for offline cracking), `PowerView` (PowerShell AD enumeration), `Mimikatz` (use with caution), `Rubeus` (Kerberos), `ldapsearch/ldap3`.
- Snapshots / AMIs of DC and workstations created before tests.