# Listing resources<a name="using-cfn-listing-stack-resources"></a>

Immediately after you run the `[aws cloudformation create\-stack](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)` command, you can list its resources using the [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-stack-resources.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-stack-resources.html) command\. This command lists a summary of each resource in the stack that you specify with the `--stack-name` parameter\. The report includes a summary of the stack, including the creation or deletion status\.

The following example shows the resources for the `myteststack` stack:

```
 1. PROMPT> aws cloudformation list-stack-resources --stack-name myteststack
 2. {
 3.     "StackResourceSummaries": [
 4.         {
 5.             "ResourceStatus": "CREATE_COMPLETE",
 6.             "ResourceType": "AWS::S3::Bucket",
 7.             "ResourceStatusReason": null,
 8.             "LastUpdatedTimestamp": "2013-08-23T01:02:28.025Z",
 9.             "PhysicalResourceId": "myteststack-s3bucket-sample",
10.             "LogicalResourceId": "S3Bucket"
11.         }
12.     ]
13. }
```

AWS CloudFormation reports resource details on any running or deleted stack\. If you specify the name of a stack whose status is `CREATE_IN_PROCESS`, AWS CloudFormation reports only those resources whose status is `CREATE_COMPLETE`\.

**Note**  
The aws cloudformation describe\-stack\-resources command returns information on deleted stacks for 90 days after they have been deleted\.