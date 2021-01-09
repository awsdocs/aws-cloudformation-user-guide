# Describing and listing your stacks<a name="using-cfn-describing-stacks"></a>

You can use two AWS CLI commands to get information about your AWS CloudFormation stacks: `[aws cloudformation list\-stacks](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-stacks.html)` and `[aws cloudformation describe\-stacks](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stacks.html)`\.

**Note**  
See [AWS CloudFormation resources](using-iam-template.md#resource-level-permissions) for a discussion of how IAM policies may limit what a user can do with these two AWS CLI commands\.

## aws cloudformation list\-stacks<a name="using-cfn-describing-stacks-list-stacks"></a>

The `aws cloudformation list-stacks` command enables you to get a list of any of the stacks you have created \(even those which have been deleted up to 90 days\)\. You can use an option to filter results by stack status, such as `CREATE_COMPLETE` and `DELETE_COMPLETE`\. The `aws cloudformation list-stacks` command returns summary information about any of your running or deleted stacks, including the name, stack identifier, template, and status\.

**Note**  
The aws cloudformation list\-stacks command returns information on deleted stacks for 90 days after they have been deleted\.

The following example shows a summary of all stacks that have a status of CREATE\_COMPLETE:

```
PROMPT> aws cloudformation list-stacks --stack-status-filter CREATE_COMPLETE
[
    {
        "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/
644df8e0-0dff-11e3-8e2f-5088487c4896",
        "TemplateDescription": "AWS CloudFormation Sample Template S3_Bucket: Sample template showing how to create a publicly accessible S3 bucket. **WARNING** This template creates an
S3 bucket. You will be billed for the AWS resources used if you create a stack from this template.",
        "StackStatusReason": null,
        "CreationTime": "2013-08-26T03:27:10.190Z",
        "StackName": "myteststack",
        "StackStatus": "CREATE_COMPLETE"
    }
]
```

## aws cloudformation describe\-stacks<a name="using-cfn-describing-stacks-describe-stacks"></a>

The `aws cloudformation describe-stacks` command provides information on your running stacks\. You can use an option to filter results on a stack name\. This command returns information about the stack, including the name, stack identifier, and status\.

 The following example shows summary information for the `myteststack` stack: 

```
PROMPT> aws cloudformation describe-stacks --stack-name myteststack
{
    "Stacks":  [
        {
            "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/a69442d0-0b8f-11e3-8b8a-500150b352e0",
            "Description": "AWS CloudFormation Sample Template S3_Bucket: Sample template showing how to create a publicly accessible S3 bucket. **WARNING** This template creates an S3 bucket.
You will be billed for the AWS resources used if you create a stack from this template.",
            "Tags": [],
            "Outputs": [
                {
                    "Description": "Name of S3 bucket to hold website content",
                    "OutputKey": "BucketName",
                    "OutputValue": "myteststack-s3bucket-jssofi1zie2w"
                }
            ],
            "StackStatusReason": null,
            "CreationTime": "2013-08-23T01:02:15.422Z",
            "Capabilities": [],
            "StackName": "myteststack",
            "StackStatus": "CREATE_COMPLETE",
            "DisableRollback": false
        }
    ]
}
```

If you don't use the `--stack-name` option to limit the output to one stack, information on all your running stacks is returned\.

## Stack status codes<a name="w7739ab1c23c15c17c11"></a>

You can specify one or more stack status codes to list only stacks with the specified status codes\. The following table describes each stack status code:

### <a name="w7739ab1c23c15c17c11b4"></a>


| Stack Status | Description | 
| --- | --- | 
|  `CREATE_COMPLETE`  |  Successful creation of one or more stacks\.  | 
|  `CREATE_IN_PROGRESS`  |  Ongoing creation of one or more stacks\.  | 
|  `CREATE_FAILED`  |  Unsuccessful creation of one or more stacks\. View the stack events to see any associated error messages\. Possible reasons for a failed creation include insufficient permissions to work with all resources in the stack, parameter values rejected by an AWS service, or a timeout during resource creation\.  | 
|  `DELETE_COMPLETE`  |  Successful deletion of one or more stacks\. Deleted stacks are retained and viewable for 90 days\.  | 
|  `DELETE_FAILED`  |  Unsuccessful deletion of one or more stacks\. Because the delete failed, you might have some resources that are still running; however, you cannot work with or update the stack\. Delete the stack again or view the stack events to see any associated error messages\.  | 
|  `DELETE_IN_PROGRESS`  |  Ongoing removal of one or more stacks\.  | 
|  `REVIEW_IN_PROGRESS` | Ongoing creation of one or more stacks with an expected StackId but without any templates or resources\. A stack with this status code counts against the [maximum possible number of stacks](cloudformation-limits.md)\.  | 
|  `ROLLBACK_COMPLETE`  |  Successful removal of one or more stacks after a failed stack creation or after an explicitly canceled stack creation\. Any resources that were created during the create stack action are deleted\. This status exists only after a failed stack creation\. It signifies that all operations from the partially created stack have been appropriately cleaned up\. When in this state, only a delete operation can be performed\.  | 
|  `ROLLBACK_FAILED`  |  Unsuccessful removal of one or more stacks after a failed stack creation or after an explicitly canceled stack creation\. Delete the stack or view the stack events to see any associated error messages\.  | 
|  `ROLLBACK_IN_PROGRESS`  |  Ongoing removal of one or more stacks after a failed stack creation or after an explicitly cancelled stack creation\.  | 
|  `UPDATE_COMPLETE`  | Successful update of one or more stacks\. | 
|  `UPDATE_COMPLETE_CLEANUP_IN_PROGRESS`  |  Ongoing removal of old resources for one or more stacks after a successful stack update\. For stack updates that require resources to be replaced, AWS CloudFormation creates the new resources first and then deletes the old resources to help reduce any interruptions with your stack\. In this state, the stack has been updated and is usable, but AWS CloudFormation is still deleting the old resources\.  | 
|  `UPDATE_FAILED`  | Unsuccessful update of one or more stacks\. View the stack events to see any associated error messages\. | 
|  `UPDATE_IN_PROGRESS`  |  Ongoing update of one or more stacks\.  | 
|  `UPDATE_ROLLBACK_COMPLETE`  |  Successful return of one or more stacks to a previous working state after a failed stack update\.  | 
|  `UPDATE_ROLLBACK_COMPLETE_CLEANUP_IN_PROGRESS`  |  Ongoing removal of new resources for one or more stacks after a failed stack update\. In this state, the stack has been rolled back to its previous working state and is usable, but AWS CloudFormation is still deleting any new resources it created during the stack update\.  | 
|  `UPDATE_ROLLBACK_FAILED`  |  Unsuccessful return of one or more stacks to a previous working state after a failed stack update\. When in this state, you can delete the stack or [continue rollback](using-cfn-updating-stacks-continueupdaterollback.md)\. You might need to fix errors before your stack can return to a working state\. Or, you can contact customer support to restore the stack to a usable state\.  | 
|  `UPDATE_ROLLBACK_IN_PROGRESS`  |  Ongoing return of one or more stacks to the previous working state after failed stack update\.  | 
|  `IMPORT_IN_PROGRESS`  |  The import operation is currently in progress\.  | 
|  `IMPORT_COMPLETE`  |  The import operation successfully completed for all resources in the stack that support `resource import`\.   | 
|  `IMPORT_ROLLBACK_IN_PROGRESS`  |  Import will roll back to the previous template configuration\.  | 
|  `IMPORT_ROLLBACK_FAILED`  |  The import rollback operation failed for at least one resource in the stack\. Results will be available for the resources CloudFormation successfully imported\.  | 
|  `IMPORT_ROLLBACK_COMPLETE`  |  Import successfully rolled back to the previous template configuration\.  | 