# Active-Directory-Kill-Chain-Attack-Defense
Designed and implemented an isolated Active Directory environment to simulate realistic attack chains against Windows infrastructure, detect attacker behavior using Windows telemetry and SIEM-style monitoring, and systematically harden the environment using MITRE ATT&amp;CK-aligned defensive controls.
---------------------------------------------------------------------------------------------------------------------------------------------------------------
                         ┌───────────────────────┐
                         │      KALI LINUX       │
                         │   ATTACK PLATFORM     │
                         └───────────┬───────────┘
                                     │
                              ATTACK CHAIN
                                     │
                                     ▼
                         ┌───────────────────────┐
                         │   WIN11-CLIENT01      │
                         │                       │
                         │ Domain Workstation    │
                         │ Sysmon                │
                         │ Windows Defender      │
                         └───────────┬───────────┘
                                     │
                              LATERAL MOVEMENT
                                     │
                                     ▼
                         ┌───────────────────────┐
                         │       MAIN-DC         │
                         │ Windows Server 2022   │
                         │                       │
                         │ Active Directory      │
                         │ DNS                   │
                         │ GPO                   │
                         │ Sysmon                │
                         └───────────┬───────────┘
                                     │
                              SECURITY TELEMETRY
                                     │
                                     ▼
                         ┌───────────────────────┐
                         │        WAZUH          │
                         │                       │
                         │ SIEM / Monitoring     │
                         │ Detection             │
                         │ Alerting              │
                         └───────────┬───────────┘
                                     │
                           INCIDENT RESPONSE
                                     │
                                     ▼
                         ┌───────────────────────┐
                         │      HARDENING        │
                         │                       │
                         │ GPO                   │
                         │ Least Privilege       │
                         │ Kerberos              │
                         │ SMB / LDAP             │
                         │ Credential Security   │
                         └───────────────────────┘
