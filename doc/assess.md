# Milestone: Assess and Select Migration Wave

#### [prev](./scan.md) | [home](./welcome.md)  | [next](./landingzone.md)

## Key Tasks

**1 Identify VM Readiness:** 

&nbsp;&nbsp;&nbsp;&nbsp;1.1\.  Identify VMs marked as "ready" for migration based on assessment.

&nbsp;&nbsp;&nbsp;&nbsp;1.2\. Identify remediation plan for "conditionally ready" VMs based on assessment.

&nbsp;&nbsp;&nbsp;&nbsp;1.3\. Identify which workloads will need lite optimization? E.G. Load Balancers, WSFC.  

&nbsp;&nbsp;&nbsp;&nbsp;1.4\. Identify potential workloads with plans beyond lift and shift, such as replatform or modernization.

**2 Assessment questionnaire:** 

&nbsp;&nbsp;&nbsp;&nbsp;2.1\.  Develope a questionnaire with the following points to cover:
- &nbsp;&nbsp;&nbsp;&nbsp;Business criticality (environment)
- &nbsp;&nbsp;&nbsp;&nbsp;Firewall Rules (Host and Network): Ports and Protocols 
- &nbsp;&nbsp;&nbsp;&nbsp;Backup mechanism 
- &nbsp;&nbsp;&nbsp;&nbsp;Monitor mechanism 
- &nbsp;&nbsp;&nbsp;&nbsp;Patching mechanism 
- &nbsp;&nbsp;&nbsp;&nbsp;Licensing mechanism (OS and Software)
- &nbsp;&nbsp;&nbsp;&nbsp;Re-IP server ok? (Best practice is to Re-IP)

**3 Identify owner of VMs for questionnaire:** 

&nbsp;&nbsp;&nbsp;&nbsp;3.1\.  Have workload owners been interviewed? 

&nbsp;&nbsp;&nbsp;&nbsp;3.2\. Is it clear who will be interviewing app owners?

**4 Identify owner of applications for questionnaire:** 

&nbsp;&nbsp;&nbsp;&nbsp;4.1\.  Have workload owners been interviewed? 

&nbsp;&nbsp;&nbsp;&nbsp;4.2\. Is it clear who will be interviewing app owners?

**5 Validate dependencies of VMs based on scan:** 

&nbsp;&nbsp;&nbsp;&nbsp;5.1\. Review data from the below tools have been successfully collected:  
- &nbsp;&nbsp;&nbsp;&nbsp;Azure Migrate Assessment Appliance Discovered Servers and pertaining readiness in Azure Migrate Project. 
- &nbsp;&nbsp;&nbsp;&nbsp;Agent based or agentless dependency mapping and app discovery in Azure Migrate Project. 

**6 Assessment Grouping and Tuning:** 

&nbsp;&nbsp;&nbsp;&nbsp;6.1\. Grouping of migration waves based on questionnaires and dependency analysis tooling. Typically a migration wave is a single application, however in tighly coupled environments a migration wave may be multiple applications. 

>**Tip**: If agentless dependency mapping was used and PowerBI access is available, leverage the Azure Migrate PowerBI integration to help visualize dependencies of groups of servers: https://github.com/Azure/azure-docs-powershell-samples/tree/master/azure-migrate/dependencies-at-scale

&nbsp;&nbsp;&nbsp;&nbsp;6.2\. Creation and tuning of performance based assessments per migration wave in the Azure Migrate Project.
