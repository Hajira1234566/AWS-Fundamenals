# AWS Cloud COST-OPTIMIZATION -identify stale resources 


GOAL: to identify stale resources using Lambda functions

Here we create a Lambda function to identifies EBS snapshots that are no longer associated with any active EC2 instance  and delete them to save storage Cost.


Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
