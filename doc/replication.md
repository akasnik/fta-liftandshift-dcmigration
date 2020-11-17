# Milestone: Replication of Migration Waves

#### [prev](./landingzone.md) | [home](./welcome.md)  | [next](./testing.md)

**1 Capacity Planning for cores quotas:** 

&nbsp;&nbsp;&nbsp;&nbsp;1.1\. Ensure subscription quotas has been increased for target VM SKU sizes and Azure resources needed to be created for the specific region.

**2 Migration Tools Planning and Implementation:** 

&nbsp;&nbsp;&nbsp;&nbsp;2.1\. Ensure subscription quotas has been increased for target VM SKU sizes and Azure resources needed to be created for the specific region.

&nbsp;&nbsp;&nbsp;&nbsp;2.2\. Validate access to provision appliances and agents.

&nbsp;&nbsp;&nbsp;&nbsp;2.3\. Plan and Implement for number of appliances based on hypervisor or physical infrastructure.

&nbsp;&nbsp;&nbsp;&nbsp;2.4\. Ensure replication appliances will scale (horizontal) to handle replication load.

&nbsp;&nbsp;&nbsp;&nbsp;2.5\. Ensure hypervisor infrastructure has enough resources to handle additional load from replication appliances.

&nbsp;&nbsp;&nbsp;&nbsp;2.6\. Plan and Implement for agent installation (mobility agent).

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