# AWS-Cloud-Cost-Optimization

## Identifying Stale EBS Snapshots

In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

### Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

1.Create an EC2 Instance,

2.Create a Snapshot for the volume of created EC2,

3.Create a Lambda Function with Python as a run time,

4.Copy the script and past it in the code editor of lambda function created,

5.Test it by manually,

6.If face issues with Describing Snapshots and Instances, Add those policies for this Lambda-function role which can be found in the configuration tab of Lambda Function,

7.Test it again by deleting the Instances created,

8.Snapshot will remain stored so test it again to delete it.

9.We can integerate with CloudWatch.
