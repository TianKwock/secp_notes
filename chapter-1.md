# Chapter 1 - Mastering Security Basics 

Security Objectives - 1.1, 1.2, 2.5, 3.2, 4.1, 4.4, 4.5, 4.9

### Understanding Core Security Goals

CIA Triad
- Confidentiality: Prevent the unauthorized disclosure of information.
  - Encryption, Access Controls (Identification, Authentication, Authorization)
- Integrity: Prevent the unauthorized alteration of information or systems.
  - Hashing
- Availability: Ensure authorized users are able to access information and systems when they need them.
  - Redundancy and Fault Tolerance, Scalability, Elasticity, Patching
 
Redundancy adds duplication to critical systems and provides fault tolerance. The goal is to remove a single point of failure (SPOF). 
  - Disk/Server/Network/Power redundancies.

Scalability is increasing the capacity of a system to meet new demand.
  - Horizontal scaling: Adding addtional servers.
  - Vertical scaling: Adds resources.

Elasticity automates scalability by having the system add/remove resources as needed.

Resiliency vs Availability - Maintaining a very high uptime requires eliminating all SPOFs and adding mulitple redundancies, which raises the total cost of ownership (TCO). Resiliency methods help systems heal themselves or recover from faults with minimal downtime. 

Resource Availability vs Security Constraints - Encryption consumes resources. 

### Introducing Basic Risk Concepts

Risk is the likelihood that a threat will explot a vulnerability, risk mitigation reduces the chaces that a threat will exploit a vulnerability or reduces the risk's impact by implementing security controls. 

### Selecting Effective Security Controls 

Control categories describe how a control works, control types describe the goal that the control is trying to achieve. 

#### Control Categories

Technical Controls: Using technology such as hardware, software, and firmware to reduce vulnerabilities.
  - Encryption, Antivirus software, IDS and IPS, Firewalls, Least privilege

Managerial Controls: Administrative controls typically documented in a security policy
  - Risk assessments, Vulnerability assessments

Operational Controls: Ensure the day-to-day operations of an organization comply with the overall security plan; implemented by the people who perform the day-to-day operations. 
  - Awareness and training, Configuration management, Media protection

Physical Controls 

#### Control Types 

Preventive Controls: Prevent security incidents
- Hardening, Training, Security guards, Account disablement process, IPS

Deterrent Controls: Discourage threats
- Warning signs, Login banners

Detective Controls: Detect when vulnerabilities have been exploited
- Log monitoring, SIEM systems, Security audit, Video surveillance, Motion detection, IDS

Corrective Controls: Attempt to reverse the impact of the incident/problem after it has occured
- Backups and system recovery, Incident handling processes

Compensating Controls: Alternative controls used instead of a primary control
- New employees using a TOTP instead of a smart card for authenticating to a system

Directive Controls: Provide instruction on how individuals should handle security-related situations
- Policies, standards, procedures, guidelines, change management

### Logging and Monitoring

Operating System / Endpoint Logs
- Windows Logs: Viewable using Windows Event Viewer
  - Security log, System log, Application log
- Linux Logs: Stored in the /var/log directory
  - /var/log/auth.log, /var/log/syslog, /var/log/messages, /var/log/secure 

Network Logs
- Firewall Logs, IDS/IPS Logs, Packet Captures

Application Logs
- Common Log format standardized by World Wide Web Consrtium (W3C)
- Metadata

Centralized Logging & Monitoring
- SIEM systems: Centralized solution for collecting, analyzing, and managing data from systems, applications, and infrastructure devices.
  - Log collectors, Data inputs, Log aggregation, Correlation engine, Automated reports, User behavior analysis (UBA), Security alerts, Automated triggers, Time synchronization, Archiving
- SIEM dashboard
  - Sensors, Alerts, Correlation, Trends

Syslog: Protocal specifying a general log entry format and details on how to transport log entries
- Used by most SIEM systems
- Systems sending syslog messages are originators, and they send log entries to a collector (syslog server)




