# Active-Directory-Kill-Chain-Attack-Defense
Designed and implemented an isolated Active Directory environment to simulate realistic attack chains against Windows infrastructure, detect attacker behavior using Windows telemetry and SIEM-style monitoring, and systematically harden the environment using MITRE ATT&amp;CK-aligned defensive controls.

                             YOUR PHYSICAL WINDOWS PC
                              │
                              │
                     VMware Workstation 17
                              │
                ┌─────────────┴─────────────┐
                │                           │
                │     ISOLATED AD LAB       │
                │                           │
                │     192.168.100.0/24      │
                │                           │
                │   ┌───────────────────┐   │
                │   │     MAIN-DC       │   │
                │   │ Windows Server     │   │
                │   │ 2022               │   │
                │   │                    │   │
                │   │ AD DS              │   │
                │   │ DNS                │   │
                │   │ Group Policy       │   │
                │   │                    │   │
                │   │ 192.168.100.10     │   │
                │   └─────────┬─────────┘   │
                │             │             │
                │          AD / DNS         │
                │             │             │
                │   ┌─────────▼─────────┐   │
                │   │ WIN11-CLIENT01    │   │
                │   │ Windows 11 Pro    │   │
                │   │                    │   │
                │   │ Domain Client     │   │
                │   │                    │   │
                │   │ 192.168.100.20    │   │
                │   └───────────────────┘   │
                │                           │
                │   ┌───────────────────┐   │
                │   │ KALI-ATTACKER     │   │
                │   │ Kali Linux        │   │
                │   │                    │   │
                │   │ Attack Platform   │   │
                │   │                    │   │
                │   │ 192.168.100.30    │   │
                │   └───────────────────┘   │
                │                           │
                └───────────────────────────┘



              
