---
title: "Application hosting infrastructure"
---

[Catalog](../) / [Services](./)

# Application hosting infrastructure

Design, deploy, and maintain Microsoft application hosting environments. Services cover RDS, virtual desktops, application delivery, tenant access, and the infrastructure that supports them.

## Explore this service area

- [Multi-tenant application hosting architecture](#multi-tenant-hosting)
- [Dedicated and shared hosting infrastructure design](#dedicated-shared-hosting)
- [Application delivery infrastructure assessment](#delivery-assessment)
- [Highly available, multi-tenant Remote Desktop Services architecture and RemoteApp deployment](#remote-desktop-services)
- [On-premises VDI architecture and deployment](#on-premises-vdi)
- [App-V infrastructure deployment and management](#app-v)
- [Application packaging and deployment preparation](#application-packaging)
- [Azure Virtual Desktop architecture and migration](#azure-virtual-desktop)
- [FSLogix profile management and optimization](#fslogix)
- [Application server sizing and performance tuning](#application-server-performance)
- [Session-host performance and density optimization](#session-host-density)
- [Application availability and dependency analysis](#availability-dependencies)
- [Hosting environment standardization](#hosting-standardization)
- [Tenant isolation and security architecture](#tenant-isolation)
- [Application deployment, update, and rollback processes](#deployment-updates-rollback)
- [Hosting infrastructure monitoring and service health](#monitoring-service-health)
- [Application hosting scalability and capacity planning](#scalability-capacity)

## Multi-tenant application hosting architecture
{: #multi-tenant-hosting}

Design how customer environments use the hosting platform. Define which services each tenant receives, which infrastructure is shared, and who administers it.

- Tenant identity, application, and data requirements
- Placement of tenant workloads and shared infrastructure services
- Tenant-specific configuration and resource allocation
- Customer onboarding, change, and removal procedures
- Administrative ownership and support access documentation

## Dedicated and shared hosting infrastructure design
{: #dedicated-shared-hosting}

Choose dedicated or shared infrastructure for each workload based on application requirements, resource use, and customer constraints.

- Dedicated VM and shared session-host placement options
- Application compatibility with shared operating systems
- CPU, memory, storage, and network resource allocation
- Maintenance and outage implications of shared dependencies
- Capacity and cost comparison for the proposed configurations

## Application delivery infrastructure assessment
{: #delivery-assessment}

Review how users reach and run hosted applications. Identify infrastructure faults, unsupported dependencies, and configuration changes that warrant further testing.

- Application, server, and delivery method inventory
- Sign-in, connection, and application launch review
- Identity, profile, storage, and database dependency mapping
- Review of reported failures and available logs
- Prioritized findings with supporting evidence and proposed next steps

## Highly available, multi-tenant Remote Desktop Services architecture and RemoteApp deployment
{: #remote-desktop-services}

Design RDS and RemoteApp delivery for multiple customers. Plan availability for the connection services and their dependencies, then test failure and recovery behavior.

- Connection Broker, Gateway, Web Access, and Session Host placement
- Broker database and connection-service availability planning
- Tenant-specific collections, application assignments, and access controls
- RemoteApp publishing and connection configuration
- Certificate, DNS, profile storage, and licensing service integration
- Planned maintenance, reconnection, and component failure testing

See [Remote Desktop Services infrastructure](microsoft-server-infrastructure.html#remote-desktop-services) for the underlying Windows Server services.

## On-premises VDI architecture and deployment
{: #on-premises-vdi}

Deploy Windows virtual desktops on on-premises infrastructure. Match desktop allocation and image maintenance to user requirements and application behavior.

- Pooled and personal desktop requirements assessment
- Hyper-V compute and storage capacity planning
- Desktop image, application, and profile configuration
- Desktop provisioning and user assignment
- Connection, sign-in, and application testing
- Desktop rebuild, update, and retirement procedures

## App-V infrastructure deployment and management
{: #app-v}

Configure App-V application delivery and manage the packages it publishes. Check the deployed server and client versions before selecting an implementation approach.

- Existing App-V infrastructure and package inventory
- Management, publishing, and content distribution configuration
- Client configuration and package publishing
- Package version changes and application assignment
- Publishing, loading, and application launch troubleshooting

Application sequencing and package preparation are covered in the [next section](#application-packaging).

## Application packaging and deployment preparation
{: #application-packaging}

Prepare applications for repeatable installation or App-V delivery. Test the package in the intended hosting environment with the application owner.

- Installer, prerequisite, and application configuration review
- Unattended installation and removal command preparation
- App-V sequencing where the application is suitable
- Installation order and dependency handling
- Standard-user launch and required application function testing
- Package version records and deployment instructions

## Azure Virtual Desktop architecture and migration
{: #azure-virtual-desktop}

Design Azure Virtual Desktop deployments and plan transitions from existing desktop or application hosting environments. Use a pilot to validate applications, profiles, and connectivity before moving users.

- Host pool, workspace, and application group design
- Session-host identity and network dependency planning
- Image preparation and session-host deployment
- FSLogix profile storage and access configuration
- Desktop and RemoteApp publishing and user assignment
- Pilot migration, user cutover, and recovery planning

See [AVD deployment automation](automation/azure-virtual-desktop.html) for provisioning and maintenance workflows.

## FSLogix profile management and optimization
{: #fslogix}

Configure FSLogix profile containers and investigate profile-related sign-in problems. Review storage performance and permissions alongside the session-host configuration.

- Profile requirements and existing configuration assessment
- Container storage location, capacity, and access permissions
- FSLogix installation and profile policy configuration
- Profile attachment, sign-in, and sign-out troubleshooting
- Container growth, storage latency, and available capacity review
- Profile migration and recovery procedure testing

## Application server sizing and performance tuning
{: #application-server-performance}

Size application servers from workload requirements and observed resource use. Compare measurements before and after a change to determine whether it addressed the bottleneck.

- CPU, memory, disk latency, and network utilization collection
- Application service and infrastructure dependency review
- VM resource sizing and host contention analysis
- Storage and network configuration review
- Workload testing and before-and-after measurement
- Documentation of remaining application or database constraints

## Session-host performance and density optimization
{: #session-host-density}

Determine how many concurrent sessions a host can support for the actual application mix. Measure resource use and user response times during representative workloads.

- Concurrent session and application usage assessment
- Sign-in peak and steady-state resource measurements
- CPU, memory, and storage contention investigation
- Profile and application startup analysis
- Session-host sizing and workload placement adjustments
- Repeat testing to establish a measured capacity baseline

## Application availability and dependency analysis
{: #availability-dependencies}

Map the services an application needs to start and remain usable. Review failure scenarios with the application owner and identify which dependencies need recovery procedures or redundancy.

- Authentication, DNS, certificate, database, and file-share dependencies
- Service accounts, network connections, and startup order
- Single points of failure and shared dependency analysis
- Maintenance impact and recovery sequence planning
- Failure and recovery tests agreed with the application owner

## Hosting environment standardization
{: #hosting-standardization}

Define repeatable host and application configurations so administrators can compare deployments and rebuild them consistently.

- Server naming, role, and configuration standards
- Image, application version, and prerequisite baselines
- Profile, policy, and management agent configuration
- Environment-specific settings and documented exceptions
- Build validation and configuration comparison
- Deployment documentation and maintenance ownership

## Tenant isolation and security architecture
{: #tenant-isolation}

Define and verify the access boundaries between customers. Review user access and administrative access across the shared hosting infrastructure.

- Identity groups, permissions, and administrative delegation
- Tenant network segmentation and allowed traffic
- File-share, profile storage, and application data permissions
- Service account scope and privileged access review
- Cross-tenant access checks using representative accounts
- Findings and remediation validation

See [identity and privileged access security](identity-privileged-access-security.html) for privileged administration design and directory security assessments.

## Application deployment, update, and rollback processes
{: #deployment-updates-rollback}

Document how application changes reach production and how a failed change is handled. Establish rollback feasibility with the application owner before deployment, including any changes to stored data.

- Application version, prerequisite, and configuration records
- Test deployment and application-owner acceptance checks
- Maintenance windows and active-session coordination
- Package or image deployment sequencing
- Backup requirements and rollback decision points
- Post-deployment launch, access, and service checks

## Hosting infrastructure monitoring and service health
{: #monitoring-service-health}

Monitor the infrastructure conditions needed to deliver hosted applications. Define checks and alerts that give operators enough information to investigate a failure.

- Host, service, connection, and profile-storage health checks
- Windows event log and platform diagnostic collection
- Resource and capacity alert thresholds
- Application launch or access checks where practical
- Alert routing, escalation ownership, and response instructions
- Review of recurring alerts and missed failures

## Application hosting scalability and capacity planning
{: #scalability-capacity}

Plan when additional hosting capacity will be needed using measured demand and expected customer growth. Account for hosts taken out of service for maintenance or failure.

- User concurrency, application mix, and resource usage trends
- Session-host and application-server capacity estimates
- Compute, storage, profile, and network growth forecasts
- Spare capacity requirements for maintenance and recovery
- Expansion thresholds and provisioning lead times
- Capacity checks after workload or customer changes

---

[All services](./) · [Engagement models](../engagements.html)
