Chapter 1: Mastering Security Basics

# Understanding Core Security Goals

## Ensuring Confidentiality

**Confidentiality** prevents the unauthorised disclosure of data

### 1\. Encryption

--\> Scrambles data to make it unreadable by unauthorised actors

### 2\. Access Controls

--\> Identification, authentication, and authorization combined provide access controls to ensure that only authorized people can access encrypted data

**Identification** \- users claim an identity with a unique username  
**Authentication** \- users prove their identity with authentication (e.g. password)  
**Authorization** \- can grant or restrict access to resources using an authentication method (e.g. permissions)

### 3\. Steganography and Obfuscation

**Steganography** \- hiding data within data. Obscures data and can be used to support obfuscation.  
**Obfuscation** methods - attempt to make something unclear or difficult to understand

e.g. security by obscurity

> **Note**: Best way to protect the confidentiality of data is by encrypting it  
> Access controls help protect confidentiality by restricting access  
> Steganography helps provide confidentiality by hiding data

## Ensuring Integrity

**Integrity** provides assurances that data has not changed (modified, tampered, corrupted)

### 1\. Hashing

--\> a **hash** is simply a number created by executing a hashing algorithm against data. If the data never changes, the resulting hash will always be the same.

Some email programs use a message authentication code (MAC) instead of a hash to verify integrity

> **Note**: Integrity verifies that data has not been modified. Loss of integrity can occur through unauthorised or unintended changes. Hashing algorithms, such as MD5, SHA-1, and HMAC, calculate hashes to verify integrity

### 2\. Digital Signatures, Certificates, and Non-Repudiation

**Digital signatures** \- anyone can look at it, no-one can modify it (it is difficult) - it can provide **authentication** (i.e. we know the sender)  
--> they also provide **non-repudiation**, i.e. the sender cannot deny sending a message they signed

Digital signatures require the use of certificates and a Public Key Infrastructure (PKI)  
**Certificates** include keys used for encryption  
The **PKI** provides the means to create, manage, and distribute certificates

> **Note**: Digital signatures can verify the integrity of emails and files and they also provide authentication and non-repudiation. Digital signatures require cerfiticates.

## Ensuring Availability

--\> **Availability** indicates that data and services are available when needed

### 1\. Redundancy and Fault Tolerance

**Redundancy** adds duplication to critical systems and provides fault tolerance. If a critical component has a fault, the duplication provided by the redundancy allows the service to continue without interruption

A system with fault tolerance can suffer a fault, but tolerate it and continue to operate

Common **goal** of fault tolerance and redundancy: remove each single point of failure (SPOF)  
If an SPOF fails, the entire system can fail

Common technique examples:

- Disk redundancies - Fault-tolerant disks, such as RAID-1, RAID-5, RAID-10, allow a system to continue to operate even if a disk fails
- Server redundancies - failover clusters include redundant servers to continue operations if a server fails. The service will switch from the failed server to an operational one in the same cluster. Virtualisation can also increase the availability of servers by reducing unplanned downtime
- Load balancing - uses multiple servers to support a single service (can increase availability of web-sites and web-based applications)
- Site redundancies - an alternate site can be a hot site (ready and available 24/7), a cold site (a location where equipment, personnel, data can be moved when needed e.g. natural disaster), or a warm site (a compromise in between)
- Backups - important data can be backed up and restored when needed
- Alternate power - Uninterruptible power supplies (UPSs) and power generators to provide energy if commercial power fails
- Cooling systems - Heating, ventilation and aircon (HVAC) systems improve availability by reducing outages from overheating

### 2\. Patching

**Patching** ensures systems stay up to date with current patches, to secure from bugs causing security issues and random crashes

## Resource versus Security Constraints

Organisations need to balance resource availability with security constraints  
E.g. we can encrypt everything but it consumes resources (costly in terms of processing power, space (e.g. encrypted data requires more space in memory) and time to encrypt/decrypt when needed)

Executives need to minimise costs without sacrificing security --> need to find the best balance between resource costs and security needs

* * *

# Introducing Basic Risk Concepts

**Risk** is the possibility of a threat exploiting a vulnerability resulting in a loss  
**Threat** is any circumstance or event that has the potential to compromise any of CIA  
**Vulnerability** is a weakness  
**Security incident** is an adverse event or series of events that can negatively affect the CIA of IT systems and data  
**Risk mitigation** reduces the chances that a threat will exploit a vulnerability

- You reduce risks by implementing controls (also called countermeasures and safeguards)

> **Note**: Risk is the likelihood that a threat will exploit a vulnerability. Risk mitigation reduces the chances that a threat will exploit a vulnerability, or reduces the impact of the risk, by implementing security controls

## Understanding Control Types

--\> There are thousands of security controls that organisations can implement to reduce risk  
--\> we need a basic understanding of control types

How security controls are implemented:

- **Technical** \- use technology
- **Administrative** \- use admin or management methods
- **Physical** \- controls you can physically touch

Goals of the security control:

- **Preventive** \- attempt to prevent an incident from occuring
- **Detective** \- attempt to detect incidents after they have occured
- **Corrective** \- attempt to reverse the impact of an incident
- **Deterrent** \- attempt to discourage individuals from causing an incident
- **Compensating** \- alternative controls used when a primary control is not feasible

### 1\. **Technical** Controls

--\> They use technology to reduce vulnerabilities. An admin installs and configures a technical control, and the technical control provides the protection automatically.

Examples:

- Encryption
- Antivirus software
- Intrustion Detection Systems (IDS) and Intrusion Prevention Systems (IPS)
- Firewalls
- Least Privilege

> **Note**: technical physical security and environmental controls include motion detectors and fire suppression systems

### 2\. **Administrative** Controls

--\> use methods mandated by organisational policies or other guidelines  
Common administrative controls:

- Risk assessments - Risk assessments help quantify and qualify risks within an organisation so that the organisation can focus on the serious risks
    - Quantitative - uses cost and asset values to quantify risks based on monetary values
    - Qualitative - uses judgements to categorise risks based on probability and impact
- Vulnerability assessments - attempt to discover current vulnerabilities or weaknesses
- Penetration test - these not only discover but also attempt to exploit vulnerabilities

> **Note**: some admin controls focus on physical and environmental security - e.g. an access list that identifies individuals allowed in a secure area. Others are known as operational or management - they help ensure that day-to-day operations comply with an organisation's security plan (people - not technology - implement these controls)

Operational controls include:

- Awareness and training - helps maintain password security, follow a clean desk policy, understand threats such as phising and malware, and more
- Configuration and change management - uses baselines to ensure systems start in a secure, hardened state & ensure that changes don't result in unintended configuration errors
- Contigency planning - plan and prepare for potential system outages, goal is to reduce the overall impact on the organisation if an outage occurs
- Media protection - physical media such as USB flash drives, external and internal drives, and backup tapes
- Physical and environmental protection - includes physical controls such as cameras and door locks, and environmental controls such as heating and ventilation systems

### 3\. **Physical** Controls

--\> Any controls you can physically touch

- Lighting
- signs
- fences
- security guards
- environmental controls such as hot and cold aisles and fire suppression (they are also technical though, i.e. here: physical)
- and more

## Control Goals

Technical and administrative controls categorise the controls based on how they are implemented  
Can also classify based on control goals in relationship to security incidents  
Common classifications:

- preventive
- detective
- corrective
- deterrent
- compensating

\[NIST > part of US dept > includes comp sec division hosting ITL > ITL publishes SPs (Special Publications) including 800 series documents - SP 800\]

### 1\. **Preventive** Controls

--\> goal of precenting security incidents

- Hardening - making a system or application more secure than its default configuration
    - uses defense-in-depth strategy with layered security
    - disabling of unecessary ports and services
    - implementing secure protocols
    - using strong passwords along with robust password policy
    - disabling default and unnecessary accounts
- Security awareness and training - ensuring users are aware of security vulnerabilities and threats
- Security guards - prevent unauthorised access, verify user identities
- Change management - ensures changes don't result in unintended outages
- Account displacement policy - ensures user accounts are disabled when an employee leaves

### 2\. **Detective** Controls

--\> attempt to detect vulnerabilities that have been exploited, resulting in a security incident. They discover the event after it has occured

- Log monitoring - investigate different logs that record details of activity (manually or automatically)
- Trend analysis - monitor logs to detect trends (e.g. IDS, analysing past alerts etc.)
- Security audit - can examine the security posture of an organisation (e.g. password audit to check passwords, periodic review of user rights to detect permissions)
- Video surveillance - CCTV to record activity and detect what's occured
- Motion detection - detect motion from potential intruders and raise alarms

### Detection versus Prevention Controls

--\> a detective control can't predict when an incident will occur and can't prevent it  
--\> a prevention control can stop the incident from occuring at all

### 3\. **Corrective** Controls

--\> attempt to reverse the impact of an incident or problem after it has occured  
Examples:

- IPS - attempts to detect attacks and then modify the environment or block the attack from continuing
- Backups and system recovery - recover data if it is lost or corrupted and have recovery procedures to recover a system after failure

### 4\. **Deterrent** Controls

--\> attempt to discourage a threat and potential attackers or employees from violating security  
--\> many preventive controls are also deterrent (e.g. security guard)  
Examples:

- Cable locks - secure laptops to furniture (stealing becomes less easy)
- Hardware locks - secure wiring closets or server rooms

### 5\. **Compensating** controls

--\> alternative controls used instead of a primary control  
e.g. an organisation might require employees to use smart cards to authenticate but provide access using a Time-based-One-Time Password (TOTP)as a compensating control, until the smart cards are delivered

### Combining Control Types and Goals

The control types (technical, administrative, physical) and control goals (preventive, detective, corrective, deterrent, compensating) are not mutually exclusive. Most controls belong to more than one category.

Example: encryption is a preventive technical control (prevents loss of confidentiality but is also implemented with technology)

* * *

# Implementing Virtualization

**Virtualisation**: a popular technology used within large data centres but also on regular PC's  
Allows us to host one or more virtual systems, or virtual machines (VMs), on a single physical system. We can host an entire virtual network within a single physical system. This is great for reducing costs.

Terminology:

- **Hypervisor** \- software that creates, runs, and manages the VMs
    - Virtualisation technologies such as VMware products, Microsoft Hyper-V, Oracle VM VirtualBox, have their own hypervisor software
- **Host** \- the physical system hosting the VM's
- **Guest** \- operating systems running on the host system
- **Host Elasticity and scalability** \- ability to resize computing capacity based on the load (can do so from our host system and based on its resources)

--\> Virtualisation provides the best ROI when an organisation has many underutilised servers  
e.g. can convert underutilised (e.g. using 20% of their processing power, memory and disk space) physical servers to virtual hosts and run multiple guest servers on each physical server (this wouldn't cost any more money for the physical servers), getting rid of additional underutilised servers (+ less electricity, heating and ventilation to maintain)

## Comparing Hypervisors

Hypervisor virtualisatoin divided into primarily two different types:

- **Type I.** \- Type I hypervisors run directly on the system hardware
    - often called bare-metal hypervisors because they don't need to run within an operating system
- **Type II.** \- Type II hypervisors run as software within a host operating system
    - e.g. Microsoft Hyper-V runs within a Microsoft OS
    - each guest has a full operating system and its own kernel

Overall: when implementing virtualisation on a PC, we will use Type II hypervisor-based virtualisation. Virtualisation in large-scale data centres typically uses Type I virtualisation

> Type II: Host Computer Hardware -> Host Operating System -> Hypervisor (control VMs) -> Guest OS 1 (Isolated OS Kernel and Apps), 2, 3, ...

## Application Cell or Container Virtualisation

**Application cell** virtualisation or **container** virtualisation runs services or applications within isolated application cells (or containers).

--\> the containers don't host an entire OS. Instead, the host's OS and kernel run the service or app within each of the containers  
--\> Because they are running on separate containers, none of the services or apps can interfere with services and apps in different containers

> Host Computer Hardware -> Host Operating System Kernel -> Container 1 (Isolared Service or App), 2, 3 ...

Benefits: container virtualisation uses fewer resources and can be more efficient than a system using a traditional Type II hypervisor virtualisation

- ISP's often use it for customers who need specific applications  
    Drawbacks: containers must use the OS of the host (e.g. if host is running Linux, all containers must run Linux)

## Secure Network Architecture

It is possible to use virtualisation as part of an overall secure network architecture  
VMs can provide segregation, segmentation, and isolation of individual systems

- One way of doing so is to disable the network interface card (NIC) in the VM
- This prevents it from transmitting any data in or out of the VM

### Snapshots

A **snapshot** provides us with a copy of the VM at a moment in time, which we can use as a backup  
Administrators commonly take snapshots of systems prior to performing any risky operation (e.g. before applying patches or updates, testing security controls, and installing new applications)

### VDI/VDE and Non-Persistence

In addition to virtualisation servers, it is possible to virtualise Desktops  
In a Virtual Desktop Infrastructure (VDI) or Virtual Desktop Environment (VDE), a user's desktop OS runs as a VM on a server  
Benefit of VDI/VDE: a user's PC can have limited hardware resources, if the PC can connect to a server over a network, it can run a full-featured desktop OS from the server

Primary consideration: whether VDI's will support persistence or non-persistence  
In a persistent VDI, each user has a custom desktop image; can customise and save data on the image. Drawback: the server needs to support unique desktop images for all users

VDI's that support non-persistence serve the same desktop for all users, provided from a preconfigured snapshot. Users can make changes while using it but it will revert back to the original snapshot when they log off

### VMs as Files

VMs are simply files. Because the VM is just a group of files, we can easily move them from one physical server to another

Some virtual server management software makes this as simple as dragging and dropping the virtual server files from one host to another. If we create a backup of the files and the VM fails we can just restore it (much quicker than rebuilding it)

Many virtualisation products allow us to manage multiple virtual systems on a single server, even when the virtual servers are running no separate physical hosts

## Risks asociated with Virtualisation

### 1\. VM Escape

--\> An attack that allows an attacker to access the host system form within the virtual system  
--\> The attacker can run code on the virtual system and interact with the hypervisor  
Also, most virtual systems run on a physical server with elevated privileges, similar to administrator privileges. A successful VM escape attack gives the attacker unlimited control over the host system and the virtual systems within the host

Need to install patches as soon as possible for both physical and virtual hosts

### 2\. VM Sprawl

--\> when an organisation has many VMs that aren't managed properly  
--\> e.g. keep people informed when creating new VMs so they will be patched  
Additionaly, each VM adds additional load onto a server and if unauthorised VMs are added to the physical servers, they can consume system resources causing other VMs to slow down or crash

### 3\. Loss of Confidentiality

Each virtual system or virtual machine is just one or more files -> this makes it easy for them to be stolen

Many VMs inclue OS and data so it might contain PPI, personal, proprietary, financial, data

* * *

### Running Kali Linux in a VM

### Using Command-Line Tools

### Windows Command Line

### Linux Terminal

### Ping

E.g. windows switch for help:`ping /?` or `ping -?`  
while for Linux: `man ping` or `ping | help`  
Windows are not case sensitive but Linux are  
On Windows, ping does 4 requests, can replicate on Linux doing `ping -c 4 <IP>`  
On Linux, ping does indefinite requests until Ctrl+C, can replicate this doing `ping -t <IP>`

In some cases malware changes the name resolution process to prevent systems from reaching the Windows Update server and getting updates (or any other services)  
Can check by pinging the domain e.g. `ping google.com`

### Beware of Firewalls

If a ping command fails, it doesn't necessarily mean it is not operational or not reachable. Ping might show the "Reply Timed Out" even if it is operating fine. Many DoS attacks use ICMP to disrupt services on Internet-based systems. **Firewalls** commonly block ICMP traffic to prevent these attacks from succeeding.  
We might be able to connect to a server from our browser but a ping to it might still fail (this means that a firewall is blocking ICMP)

### Using ping to test security posture

--\> can verify whether firewalls and routers are actually blocking ping traffic (such as a DDoS) or if an IPS is blocking it

### ipconfig, ifconfig, ip

- **ipconfig** shows the TCP/IP configuration information for a system including:
    - computer's IP address
    - subnet mask
    - default gateway
    - MAC address
    - address of a DNS server
    - configuration for all NICs on a system (both wired and wireless info)
- On Linux we use **ip a** instead

Windows detailed info:

- `ipconfig /all` shows a comprehensive listing of TCP/IP configuration information for each NIC. Includes MAC address, address assigned to DNS servers and address of DHCP client
- `ipconfig /displaydns` shows the contents of the DNS cache, including the host name to IP addresses included on the hosts file
- `ipconfig /flushdns` can erase the contents of the DNS cache with this command (use this when the cache has incorrect information and you want to ensure DNS is queried for up-to-date information)

Normally, a NIC uses non-promiscious mode and only processes packets addressed directly to its IP address. When you put it in promiscious mode, it processes all packets regardless of the IP address. This allows the protocol analyser to capture all packets that reach the NIC

- `ip link show` shows the interfaces along with some details on them
- `ip link set eth0 up` enables a network interface
- `ip -s link` shows statistics on the network interfaces  
    The ip command in Linux allows to view and manipulate NIC settings

### Netstat

(Network statistics) allows us to view statistics for TCP/IP protocols on a system. Also gives us the ability to **view active TCP/IP network connections**  
Can also identify connections from an infected computer to a remote computer using netstat

- `netstat` displays a listing of all open TCP connections
- `netstat -a` displays a listing of all TCP and UDP ports that a system is listening on, in addition to all open connections
- `netstat -r` displays the routing table
- `netstat -e` displays details on network statistics, including how many bytes the system sent and received
- `netstat -s` displays statistics of packets sent or received for specific protocols, such as IP, ICMP, TCP and UDP
- `netstat -n` displays addresses and port numbers in numerical order
- `netstat -p protocol` shows statistics on a specific protocol such as TCP or UDP (e.g. netstat -p tcp)  
    Can combine netstat switches to show information together e.g. `netstat -anp tct` shows a listing of ports the system is listening on, listed in numerical order, only for the TCP protocol.

Common states of connection that netstat will indicate

- **ESTABLISHED** \- the normal state for the data transfer phase of a connection. Indicates an active open connection
- **LISTEN** \- indicates the system is waiting for a connection request
- **CLOSE_WAIT** \- indicates the system is waiting for a connection termination request
- **TIME_WAIT** \- indicates the system is waiting for enough time to pass to be sure the remote system received a TCP-based acknowledgment of the connection
- **SYN_SENT** \- indicates system sent a tcp SYN
- **SYN_RECEIVED** \- indicates system sent tcp SYN-ACK after receiving a SYN, still waiting for ACK to establish the connection

> An excessive number of SYN_RECEIVED states indicates a SYN flooding attack (flood of SYN packets without ending ACK)

### Tracert

--\> lists the routers between two systems. In this context, each router is reffered to as a hop  
--\> sometimes identifies the IP address and the host name of each hop in addition to the Round trip times (RTTs) for each hop

Windows-based use `tracert` and Linux-based use `traceroute`

Network admins use tracert to identify faulty routers on the network  
Ping tells them if they can reach a distant server. If the ping fails, they can use tracert to identify where the traffic stops - some of the hops will succeed but at some point, tracert will identify where packets are lost, giving them insights into where the problem has occured. They might also see where the RTTs increase as traffic is routed around a faulty router  
Can also use tracert to trace a path to an ip or service and check if there is potentially a MITM redirection

### Arp

--\> a command-line-tool related to the Address Resolution Protocol; however the arp command and ARP (the protocol). ARP resolves IP addresses to MAC addresses and stores the result in the ARP cache  
Can use the **arp** to view and manipulate the ARP cache. Examples:

- `arp` \- without a switch, shows help Windows
- `arp` \- without a switch, shows the ARP cache on Linux
- `arp -a` \- shows the ARP cache on Windows
- `arp -a 192.168.1.1` \- display the ARP cache entry for the specified IP address  
    Can also use arp to identify the MAC address of other systems on our local network

e.g. can ping server1 and ARP will identify server1's IP address, can then arp -a to show the ARP cache, which includes the MAC address for server1