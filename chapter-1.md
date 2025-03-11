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
