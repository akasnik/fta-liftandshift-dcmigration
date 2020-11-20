
# Milestone: End to End Test Migration Wave

#### [prev](./replication.md) | [home](./welcome.md)  | [next](./migration.md)

The following content can be used as a checklist to incorporate within your migration project plan to ensure best practices.

## **1 Pre & Post  Migration Activities Defined** 

&nbsp;&nbsp;&nbsp;&nbsp;1.1\. Business
- &nbsp;&nbsp;&nbsp;&nbsp;Communication to Business Impact.
- &nbsp;&nbsp;&nbsp;&nbsp;Define Maintenance Window.
- &nbsp;&nbsp;&nbsp;&nbsp;Define POCs and support for:
    - &nbsp;&nbsp;&nbsp;&nbsp;Network Admins
    - &nbsp;&nbsp;&nbsp;&nbsp;Backup Admins
    - &nbsp;&nbsp;&nbsp;&nbsp;Server Admins
    - &nbsp;&nbsp;&nbsp;&nbsp;App Owners
    - &nbsp;&nbsp;&nbsp;&nbsp;Microsoft and/ partner Support
- &nbsp;&nbsp;&nbsp;&nbsp;Define soak period after cutover:

&nbsp;&nbsp;&nbsp;&nbsp;1.2\. Technical
- &nbsp;&nbsp;&nbsp;&nbsp;Pre-Migration Tasks:
    - &nbsp;&nbsp;&nbsp;&nbsp;Define Rollback Plan.
    - &nbsp;&nbsp;&nbsp;&nbsp;Take backup of servers on-premises.
    - &nbsp;&nbsp;&nbsp;&nbsp;Open Firewall Ports.
    - &nbsp;&nbsp;&nbsp;&nbsp;Get local admins accounts for login purposes.
    - &nbsp;&nbsp;&nbsp;&nbsp;Verify manual changes needed for Windows and Linux: https://docs.microsoft.com/en-us/azure/migrate/prepare-for-migration#verify-required-changes-before-migrating

- &nbsp;&nbsp;&nbsp;&nbsp;Post-Migration Tasks:
    - &nbsp;&nbsp;&nbsp;&nbsp;Validate login with local account for SSH or RDP.
    - &nbsp;&nbsp;&nbsp;&nbsp;Validate DNS resolves and DNS servers are configured in network settings (E.G. TCP/IP settings) for the OS.
    - &nbsp;&nbsp;&nbsp;&nbsp;Validate IP address has been assigned to server in network settings (E.G. TCP/IP settings) for the OS.
    - &nbsp;&nbsp;&nbsp;&nbsp;Validate access to OS licensing endpoints (E.G. Azure KMS endpoints).
    - &nbsp;&nbsp;&nbsp;&nbsp;Validate login with domain accounts.
    - &nbsp;&nbsp;&nbsp;&nbsp;Validate application URLs dependencies.
    - &nbsp;&nbsp;&nbsp;&nbsp;Update any existing CMDB
    - &nbsp;&nbsp;&nbsp;&nbsp;Install necessary Azure agents: 
        - &nbsp;&nbsp;&nbsp;&nbsp;Windows and/or WALinux VM agent.
        - &nbsp;&nbsp;&nbsp;&nbsp;Windows and/or Linux Log Analytics agent/extension.
        - &nbsp;&nbsp;&nbsp;&nbsp;Windows and/or Linux Dependency Map agent/extension.
        - &nbsp;&nbsp;&nbsp;&nbsp;Windows SQL Extension.
    - &nbsp;&nbsp;&nbsp;&nbsp; Validate VM monitoring via new or existing service.
    - &nbsp;&nbsp;&nbsp;&nbsp; Validate VM patching via new or existing service.
    - &nbsp;&nbsp;&nbsp;&nbsp; Validate VM backup via new or existing service.
    - &nbsp;&nbsp;&nbsp;&nbsp; Validate VM Antivirus/endpoint protection via new or existing service.
    - &nbsp;&nbsp;&nbsp;&nbsp; Tag Azure resources.
    - &nbsp;&nbsp;&nbsp;&nbsp; Postmortem and Learnings
                                            
## **2 Testing Plans Definition** 

&nbsp;&nbsp;&nbsp;&nbsp;2.1\. Define Smoke Test
- &nbsp;&nbsp;&nbsp;&nbsp; Select which post-migration tasks need will be executed. (E.G. Validate login with local accounts, validate TCP/IP settings for DNS and IPv4).
- &nbsp;&nbsp;&nbsp;&nbsp; This is usually led by server admins or migration partners.

&nbsp;&nbsp;&nbsp;&nbsp;2.2\. Define UAT Test
- &nbsp;&nbsp;&nbsp;&nbsp; Select which post-migration tasks need will be executed: (E.G. Validate application URL dependencies and access with domain accounts).
- &nbsp;&nbsp;&nbsp;&nbsp; This is usually led by application owners.

&nbsp;&nbsp;&nbsp;&nbsp;2.3\. Identify Test Landing Zone and Test Process

![Concept Diagram](https://github.com/Azure/fta-liftandshift-dcmigration/blob/main/png/testmigration-workflow.PNG)


## **3 Testing Execution** 

&nbsp;&nbsp;&nbsp;&nbsp;3.1\. Execute Smoke and UAT Test for each migration wave.
