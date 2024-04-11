**AWS Cloud Cost Optimization - Identifying Stale Resources**
In this example, we'll develop a Lambda function tasked with detecting EBS snapshots that aren't linked to any active EC2 instance. The function will then proceed to remove these snapshots to reduce storage expenses.

**Description:**
The Lambda function retrieves all EBS snapshots belonging to the same account ('self') and gathers a list of active EC2 instances, including both running and stopped instances. For each snapshot, it verifies whether the associated volume, if it exists, is not linked to any active instance. If a snapshot is found to be stale, meaning it is no longer associated with any active instance, it is deleted, thereby optimizing storage costs.
