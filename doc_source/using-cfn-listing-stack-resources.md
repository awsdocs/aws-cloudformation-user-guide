# Listing Resources<a name="using-cfn-listing-stack-resources"></a>

Immediately after you run the `[aws cloudformation create\-stack](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)` command, you can list its resources using the [http://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-stack-resources.html](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-stack-resources.html) command\. This command lists a summary of each resource in the stack that you specify with the `--stack-name` parameter\. The report includes a summary of the stack, including the creation or deletion status\.

The following example shows the resources for the `myteststack` stack:

```
PROMPT> aws cloudformation list-stack-resources --stack-name myteststack

{
    "StackResourceSummaries": [
        {
            "ResourceStatus": "CREATE_COMPLETE",
            "ResourceType": "AWS::S3::Bucket",
            "ResourceStatusReason": null,
            "LastUpdatedTimestamp": "2013-08-23T01:02:28.025Z",
            "PhysicalResourceId": "myteststack-s3bucket-sample",
            "LogicalResourceId": "S3Bucket"
        }
    ]
}
```

AWS CloudFormation reports resource details on any running or deleted stack\. If you specify the name of a stack whose status is `CREATE_IN_PROCESS`, AWS CloudFormation reports only those resources whose status is `CREATE_COMPLETE`\.

**Note**  
The aws cloudformation describe\-stack\-resources command returns information on deleted stacks for 90 days after they have been deleted\.