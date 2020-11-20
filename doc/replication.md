# Milestone: Replication of Migration Waves

#### [prev](./landingzone.md) | [home](./welcome.md)  | [next](./testing.md)

**1 Capacity Planning for cores quotas:** 

&nbsp;&nbsp;&nbsp;&nbsp;1.1\. Ensure subscription quotas has been increased for target VM SKU sizes and Azure resources needed to be created for the specific region.

**2 Replication Tools Planning and Implementation:** 

![Concept Diagram](https://github.com/Azure/fta-liftandshift-dcmigration/blob/main/png/replication-workflow.PNG)

- &nbsp;&nbsp;&nbsp;&nbsp;Reference Link A: https://docs.microsoft.com/en-us/azure/migrate/migrate-support-matrix-vmware-migration#vm-requirements-agentless
- &nbsp;&nbsp;&nbsp;&nbsp;Reference Link B: https://docs.microsoft.com/en-us/azure/migrate/tutorial-migrate-vmware-agent
- &nbsp;&nbsp;&nbsp;&nbsp;Reference Link C: https://docs.microsoft.com/en-us/azure/migrate/tutorial-migrate-vmware-powershell
- &nbsp;&nbsp;&nbsp;&nbsp;Reference Link D: https://docs.microsoft.com/en-us/azure/migrate/tutorial-migrate-hyper-v
- &nbsp;&nbsp;&nbsp;&nbsp;Reference Link E: 
    - &nbsp;&nbsp;&nbsp;&nbsp;Physical/Other hypervisors: https://docs.microsoft.com/en-us/azure/migrate/tutorial-migrate-physical-virtual-machines
    - &nbsp;&nbsp;&nbsp;&nbsp;AWS: https://docs.microsoft.com/en-us/azure/migrate/tutorial-migrate-aws-virtual-machines
    - &nbsp;&nbsp;&nbsp;&nbsp;GCP: https://docs.microsoft.com/en-us/azure/migrate/tutorial-migrate-gcp-virtual-machines

&nbsp;&nbsp;&nbsp;&nbsp;2.2\. Ensure hypervisor infrastructure has enough resources to handle additional load from replication appliances.

**3 Replication:** 

&nbsp;&nbsp;&nbsp;&nbsp;3.1\. Consider running deployment planner to define:

- &nbsp;&nbsp;&nbsp;&nbsp;How much bandwidth is needed and available for replications?
- &nbsp;&nbsp;&nbsp;&nbsp;How many VMs can be initially replicated at the same time?
- &nbsp;&nbsp;&nbsp;&nbsp;How many VMs can be left replicating at the same time?
- &nbsp;&nbsp;&nbsp;&nbsp;Is there a need to throttle replication within the replication appliance?

&nbsp;&nbsp;&nbsp;&nbsp;3.2\. Enable initial replication for a subset of the migration waves based on available bandwidth.
- &nbsp;&nbsp;&nbsp;&nbsp;Initial replication takes more bandwidth vs. delta replications.
- &nbsp;&nbsp;&nbsp;&nbsp;For each server configured for initial replication, monitor replication progress closely until successful before enabling initial replication for remaining servers.
- &nbsp;&nbsp;&nbsp;&nbsp;For each server with ongoing replication, monitor replication closely before enabling initial replication for remaining servers.