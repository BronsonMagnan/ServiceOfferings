---
title: "Microsoft server & enterprise infrastructure"
---

[Catalog](../) / [Services](./)

# Microsoft server & enterprise infrastructure

Design and modernize Windows Server, directory services, PKI, file services, and SQL Server infrastructure.


## Explore this service area

- [Windows Server architecture, deployment, and modernization](#windows-server)
- [Active Directory Domain Services design and administration](#active-directory-domain-services)
- [Active Directory forest and domain consolidation and migration](#directory-consolidation-migration)
- [Group Policy architecture, auditing, and modernization](#group-policy)
- [DNS, DHCP, NPS, and core network services](#core-network-services)
- [Network Time Protocol architecture, design, and implementation](#network-time-protocol)
- [Active Directory Certificate Services and PKI](#certificate-services-pki)
- [Microsoft Entra ID integration and hybrid identity](#hybrid-identity)
- [Windows Server Failover Clustering](#failover-clustering)
- [Remote Desktop Services infrastructure](#remote-desktop-services)
- [Highly available file server clusters and SMB services](#file-server-clusters-smb)
- [DFS Namespace design](#dfs-namespace-design)
- [File services and storage migration](#file-storage-migration)
- [Microsoft SQL Server infrastructure and Always On availability architecture](#sql-server-availability)
- [Windows Admin Center deployment and configuration](#windows-admin-center)
- [Server hardening, patching, and lifecycle management](#server-lifecycle)

## Windows Server architecture, deployment, and modernization
{: #windows-server}

Plan and deploy Windows Server environments around application requirements, management practices, and hardware constraints. Establish repeatable server builds and a staged approach to replacing older systems.

- Server role inventory and application dependency assessment
- Physical and virtual server sizing and placement
- Operating system installation and configuration standards
- Role and feature selection, service configuration, and prerequisite validation
- Upgrade versus replacement assessment and migration sequencing
- Monitoring, backup, and management agent integration
- Build acceptance checks, deployment documentation, and operational handoff

## Active Directory Domain Services design and administration
{: #active-directory-domain-services}

Design and maintain the directory services that support authentication, computer management, and application access. Review replication and DNS dependencies before changing domain controller placement or directory structure.

- Forest and domain architecture assessment
- Domain controller placement, sizing, and lifecycle planning
- Active Directory sites, subnets, and replication topology
- Organizational unit structure and administrative delegation
- DNS integration, global catalog placement, and operations master roles
- Directory health, replication, and authentication troubleshooting
- User, computer, group, and service account administration standards
- Directory backup, recovery procedures, and operational documentation

See [identity and privileged access security](identity-privileged-access-security.html) for detailed security assessments and privileged administration design.

## Active Directory forest and domain consolidation and migration
{: #directory-consolidation-migration}

Plan directory consolidation around application dependencies and continued user access. Define migration stages, coexistence requirements, and rollback decisions before moving identities or computers.

- Source and target forest inventory and dependency mapping
- Target domain, organizational unit, and delegation design
- Trust, DNS, and authentication dependency planning
- User, group, computer, and service account migration planning
- File permissions, application access, and profile transition assessment
- Group Policy reconciliation and target policy validation
- Pilot migrations, cutover sequencing, and rollback planning
- Post-migration access validation and source environment retirement

## Group Policy architecture, auditing, and modernization
{: #group-policy}

Review how Group Policy configures servers and users, then simplify policy structure and ownership. Test policy changes against representative workloads before wider deployment.

- Group Policy object inventory and configuration review
- Organizational unit links, inheritance, enforcement, and filtering analysis
- Conflicting, duplicate, and obsolete policy identification
- Administrative template and Central Store management
- Server and user configuration baseline development
- Security policy and Group Policy Preferences review
- Policy backup, version control, and change documentation
- Pilot deployment, resultant policy validation, and processing troubleshooting

## DNS, DHCP, NPS, and core network services
{: #core-network-services}

Design the name resolution, address assignment, and network access services that Windows infrastructure depends on. Plan service placement and recovery alongside the network and directory architecture.

- DNS zone design, delegation, forwarding, and conditional forwarding
- Active Directory-integrated DNS and secure dynamic update configuration
- DNS record lifecycle, scavenging review, and resolution troubleshooting
- DHCP scope, exclusion, reservation, and option design
- DHCP failover planning and service migration
- NPS RADIUS client configuration and network policy design
- Certificate and authentication dependency review for network access
- Configuration backup, service health checks, and recovery documentation

## Network Time Protocol architecture, design, and implementation
{: #network-time-protocol}

Design and implement time synchronization for Windows servers, virtualization hosts, and network infrastructure. Define time sources and synchronization paths, then validate clock offsets and behavior when a source becomes unavailable.

- Existing time source, client configuration, and synchronization dependency assessment
- Internal NTP service architecture and upstream time source selection
- Time source redundancy, network reachability, and firewall requirements
- Active Directory time hierarchy and forest-root PDC emulator configuration
- Windows Time service configuration through Group Policy and PowerShell
- NTP client configuration for standalone servers and network devices
- Hyper-V host and guest time provider review to identify conflicting sources or circular dependencies
- Clock offset, synchronization status, and time source monitoring
- Source failure testing, troubleshooting, and configuration documentation

Define accuracy requirements from the applications in scope and validate them against measured results.

## Active Directory Certificate Services and PKI
{: #certificate-services-pki}

Design certificate services for infrastructure authentication and encrypted communications. Establish issuance and renewal procedures that account for certificate consumers and certificate authority recovery.

- Certificate authority hierarchy and trust design
- Root and issuing certificate authority deployment planning
- Certificate template, enrollment permission, and issuance policy design
- Autoenrollment and application certificate enrollment configuration
- Certificate revocation and authority information publication planning
- Certificate renewal, replacement, and expiration monitoring
- Certificate authority backup, recovery, and migration planning
- Certificate chain, enrollment, and revocation troubleshooting

Coordinate certificate template and administrative access reviews with the [identity security assessment](identity-privileged-access-security.html#active-directory-security--paths-of-escalation-assessment).

## Microsoft Entra ID integration and hybrid identity
{: #hybrid-identity}

Connect on-premises directory services with Microsoft Entra ID. Plan identity synchronization and authentication around application requirements and the existing directory structure.

- Hybrid identity architecture and directory readiness assessment
- Identity matching, user principal name, and attribute cleanup planning
- Synchronization scope, filtering, and attribute mapping design
- Synchronization service deployment and health monitoring
- Authentication method and application sign-in dependency assessment
- Device identity and join requirements review
- Synchronization error and sign-in troubleshooting
- Change validation, recovery procedures, and operational handoff

## Windows Server Failover Clustering
{: #failover-clustering}

Design and deploy clusters for supported Windows Server workloads. Validate the compute, network, and storage configuration before placing applications into service.

- Cluster workload requirements and node sizing
- Hardware, operating system, network, and storage compatibility assessment
- Cluster network and storage configuration
- Quorum and witness design
- Cluster validation and deployment
- Clustered role configuration and dependency review
- Planned failover, node failure, and recovery testing
- Cluster-aware maintenance, patch sequencing, and troubleshooting
- Capacity planning and cluster lifecycle documentation

## Remote Desktop Services infrastructure
{: #remote-desktop-services}

Design Remote Desktop Services infrastructure for desktop sessions and RemoteApp delivery. Account for user profiles, application dependencies, access requirements, and service availability.

- RDS role placement and deployment architecture
- Connection Broker, Gateway, Web Access, and Session Host configuration
- High availability and multi-tenant delivery architecture
- Session collection and RemoteApp publishing configuration
- Profile storage and FSLogix integration
- Certificates, authentication, and external access configuration
- Session host sizing, capacity planning, and maintenance procedures
- RDS licensing infrastructure configuration
- Connection, session, and application availability testing

See [application hosting infrastructure](application-hosting.html) for application delivery, packaging, and hosting performance services.

## Highly available file server clusters and SMB services
{: #file-server-clusters-smb}

Design file services around workload access patterns and recovery requirements. Coordinate cluster configuration, SMB access, and storage availability with the applications that use the shares.

- File server workload assessment and capacity planning
- Clustered file server architecture and role selection
- Shared storage and network dependency design
- SMB share structure and NTFS permission planning
- Service account and application access configuration
- SMB security and performance configuration review
- DFS Namespace integration for consistent client paths
- Failover, client reconnection, and workload access testing
- Backup integration, restoration testing, and operational runbooks

## DFS Namespace design
{: #dfs-namespace-design}

Design a shared folder hierarchy that gives users and applications consistent paths across file servers. Plan namespace availability, folder targets, and referrals so the namespace can support storage changes and multiple datacenter locations.

- Domain-based and standalone namespace architecture
- Namespace naming standards, folder hierarchy, and target mapping
- Namespace server placement and redundancy
- Active Directory site-aware referrals, target priority, and client failback
- Access-based enumeration and alignment with SMB share and NTFS permissions
- Integration with highly available file server clusters
- Namespace consolidation and migration planning to preserve client paths where feasible
- PowerShell deployment, configuration export, and namespace validation
- Referral troubleshooting, availability testing, and operational documentation

The design addresses namespace availability and file-data availability separately. Replication and recovery requirements are defined for the underlying storage and workloads.

## File services and storage migration
{: #file-storage-migration}

Move file services with a documented plan for data integrity, permissions, and client access. Define validation and rollback steps before the production cutover.

- File share, data volume, and storage dependency inventory
- Target server, storage, and share layout planning
- File ownership, permissions, and access dependency assessment
- Data copy, synchronization, and migration tooling selection
- Open file and application dependency coordination
- DFS target changes and client path transition planning
- Pilot migration, cutover scheduling, and rollback procedures
- Data, permissions, and client access validation
- Source share retirement and migration documentation

## Microsoft SQL Server infrastructure and Always On availability architecture
{: #sql-server-availability}

Design the server, storage, and availability infrastructure for SQL Server workloads. Select the availability approach with the database owners and plan how applications reconnect after a failure.

- SQL Server infrastructure requirements and dependency assessment
- Compute, memory, storage, and network sizing
- Always On availability group and failover cluster instance architecture assessment
- Windows clustering, quorum, and witness planning where required
- Replica placement, synchronization mode, and failover policy planning
- Listener, DNS, connectivity, and application connection configuration
- Service account, certificate, and access requirements review
- Backup and recovery integration with database operations
- Failover testing, maintenance sequencing, and operational documentation

## Windows Admin Center deployment and configuration
{: #windows-admin-center}

Deploy Windows Admin Center for browser-based server and cluster administration. Define who can use the management gateway and how it reaches managed systems.

- Gateway placement and deployment planning
- Gateway certificate and connection configuration
- Administrator access and authentication configuration
- Managed server and cluster onboarding
- Remote management prerequisites and connectivity validation
- Extension selection and update planning
- Administrative workflow testing and troubleshooting
- Gateway maintenance and recovery documentation

## Server hardening, patching, and lifecycle management
{: #server-lifecycle}

Maintain server configurations and updates through tested change procedures. Plan replacement work before hardware or software support ends.

- Server inventory, support status, and lifecycle assessment
- Security baseline selection and workload compatibility review
- Unnecessary service, feature, and administrative access review
- Patch deployment groups, maintenance windows, and approval workflows
- Pre-update checks, staged deployment, and restart coordination
- Post-update service validation and rollback planning
- Configuration drift and patch compliance reporting
- Server rebuild, replacement, and retirement planning
- Maintenance runbooks and operational handoff

---

[All services](./) · [Engagement models](../engagements.html)
