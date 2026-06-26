# 🖥️ Active Directory Home Lab

## 📌 Overview

This project is about building a basic Active Directory lab using virtual machines and to create GPO policies.

## 🎯 Objectives

Set up a Windows Server 2022 Domain Controller

Create Windows 10 client machines

Configure networking

Add users and join machines to the domain

## 🧰 Lab Setup
💻 Host Machine

Windows 11

16 GB RAM (recommended)

SSD storage

## 🖥️ Virtual Machines

Server: Windows Server 2022 (Domain Controller)

Client(s): Windows 10 or 11 (1–2 machines)

## 🔧 Tools
VirtualBox

## ⚙️ Create Virtual Machines

Windows 10 VM

Windows server 2022

Create a NAT Network in your hypervisor

Enable DHCP

Attach ALL VMs to this network


## 👤 Initial Setup
On Windows 10 Clients
Choose “Domain Join” during setup

Create local user accounts

## 🔌 Configure DNS (Important)

On Server:

ipconfig

Copy IPv4 address

On each Windows 10 VM:
Network Settings > Adapter > IPv4

Set DNS = Server IP


## 🏢 Install Active Directory

On Server:

Open Server Manager

Click Add Roles and Features

Select Active Directory Domain Services
Install

Click Promote to Domain Controller

Configure Domain

Create new forest

## 👥 Create Users
Active Directory Users and Computers

Navigate to Users

Right click > New > User

## 🔐 Group Policy Configuration

### Password Policy
Enforces minimum password length of 12
 
Complexity requirements enabled
  
Applied to entire domain
  
## 📚 Lessons Learned

DNS is critical for domain join and policy enforcement.

Active Directory controls authentication & authorization.

GPOs allow powerful, centralized configuration of users environment.
