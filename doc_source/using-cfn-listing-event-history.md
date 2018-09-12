# Viewing Stack Event History<a name="using-cfn-listing-event-history"></a>

You can track the status of the resources AWS CloudFormation is creating and deleting with the `[aws cloudformation describe\-stack\-events](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-events.html)` command\. The amount of time to create or delete a stack depends on the complexity of your stack\.

In the following example, a sample stack is created from a template file by using the `[aws cloudformation create\-stack](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)` command\. After the stack is created, the events that were reported during stack creation are shown by using the aws cloudformation describe\-stack\-events command\.

The following example creates a stack with the name `myteststack` using the `sampletemplate.json` template file: 

`aws cloudformation create-stack --stack-name myteststack --template-body file:///home/local/test/sampletemplate.json `

```
 [
     {
         "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
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
```

The following example describes the `myteststack` stack:

`aws cloudformation describe-stack-events --stack-name myteststack`

```
{
    "StackEvents": [
        {
            "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
            "EventId": "af67ef60-0b8f-11e3-8b8a-500150b352e0",
            "ResourceStatus": "CREATE_COMPLETE",
            "ResourceType": "AWS::CloudFormation::Stack",
            "Timestamp": "2013-08-23T01:02:30.070Z",
            "StackName": "myteststack",
            "PhysicalResourceId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/a69442d0-0b8f-11e3-8b8a-500150b352e0",
            "LogicalResourceId": "myteststack"
        },
        {
            "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
            "EventId": "S3Bucket-CREATE_COMPLETE-1377219748025",
            "ResourceStatus": "CREATE_COMPLETE",
            "ResourceType": "AWS::S3::Bucket",
            "Timestamp": "2013-08-23T01:02:28.025Z",
            "StackName": "myteststack",
            "ResourceProperties": "{\"AccessControl\":\"PublicRead\"}",
            "PhysicalResourceId": "myteststack-s3bucket-jssofi1zie2w",
            "LogicalResourceId": "S3Bucket"
        },
        {
            "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
            "EventId": "S3Bucket-CREATE_IN_PROGRESS-1377219746688",
            "ResourceStatus": "CREATE_IN_PROGRESS",
            "ResourceType": "AWS::S3::Bucket",
            "Timestamp": "2013-08-23T01:02:26.688Z",
            "ResourceStatusReason": "Resource creation Initiated",
            "StackName": "myteststack",
            "ResourceProperties": "{\"AccessControl\":\"PublicRead\"}",
            "PhysicalResourceId": "myteststack-s3bucket-jssofi1zie2w",
            "LogicalResourceId": "S3Bucket"
        },
        {
            "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
            "EventId": "S3Bucket-CREATE_IN_PROGRESS-1377219743862",
            "ResourceStatus": "CREATE_IN_PROGRESS",
            "ResourceType": "AWS::S3::Bucket",
            "Timestamp": "2013-08-23T01:02:23.862Z",
            "StackName": "myteststack",
            "ResourceProperties": "{\"AccessControl\":\"PublicRead\"}",
            "PhysicalResourceId": null,
            "LogicalResourceId": "S3Bucket"
        },
        {
            "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
            "EventId": "a69469e0-0b8f-11e3-8b8a-500150b352e0",
            "ResourceStatus": "CREATE_IN_PROGRESS",
            "ResourceType": "AWS::CloudFormation::Stack",
            "Timestamp": "2013-08-23T01:02:15.422Z",
            "ResourceStatusReason": "User Initiated",
            "StackName": "myteststack",
            "PhysicalResourceId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/a69442d0-0b8f-11e3-8b8a-500150b352e0",
            "LogicalResourceId": "myteststack"
        }
    ]
}
```

**Note**  
You can run the aws cloudformation describe\-stack\-events command while the stack is being created to view events as they are reported\.

The most recent events are reported first\. The following table describe the fields returned by the aws cloudformation describe\-stack\-events command:


| Field | Description | 
| --- | --- | 
|  EventId  |  Event identifier  | 
|  StackName  |  Name of the stack that the event corresponds to  | 
|  StackId  |  Identifier of the stack that the event corresponds to  | 
|  LogicalResourceId  |  Logical identifier of the resource  | 
|  PhysicalResourceId  |  Physical identifier of the resource  | 
|  ResourceProperties  |  Properties of the resource  | 
|  ResourceType  |  Type of the resource  | 
|  Timestamp  |  Time when the event occurred  | 
|  ResourceStatus  |  The status of the resource, which can be one of the following status codes: `CREATE_COMPLETE` \| `CREATE_FAILED` \| `CREATE_IN_PROGRESS` \| `DELETE_COMPLETE` \| `DELETE_FAILED` \| `DELETE_IN_PROGRESS` \| `DELETE_SKIPPED` \| `UPDATE_COMPLETE` \| `UPDATE_FAILED` \| `UPDATE_IN_PROGRESS`\. The `DELETE_SKIPPED` status applies to resources with a deletion policy attribute of retain\.  | 
|  ResourceStatusReason  |  More information on the status  | 