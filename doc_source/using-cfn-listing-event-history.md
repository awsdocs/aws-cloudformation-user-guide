# Viewing stack event history<a name="using-cfn-listing-event-history"></a>

You can track the status of the resources AWS CloudFormation is creating and deleting with the `[aws cloudformation describe\-stack\-events](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-events.html)` command\. The amount of time to create or delete a stack depends on the complexity of your stack\.

In the following example, a sample stack is created from a template file by using the `[aws cloudformation create\-stack](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)` command\. After the stack is created, the events that were reported during stack creation are shown by using the aws cloudformation describe\-stack\-events command\.

The following example creates a stack with the name `myteststack` using the `sampletemplate.json` template file: 

```
 1. PROMPT> aws cloudformation create-stack --stack-name myteststack --template-body file:///home/local/test/sampletemplate.json  
 2. [
 3.     {
 4.         "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
 5.         "Description": "AWS CloudFormation Sample Template S3_Bucket: Sample template showing how to create a publicly accessible S3 bucket. **WARNING** This template creates an S3 bucket.
 6. You will be billed for the AWS resources used if you create a stack from this template.",
 7.         "Tags": [],
 8.         "Outputs": [
 9.             {
10.                 "Description": "Name of S3 bucket to hold website content",
11.                 "OutputKey": "BucketName",
12.                 "OutputValue": "myteststack-s3bucket-jssofi1zie2w"
13.             }
14.         ],
15.         "StackStatusReason": null,
16.         "CreationTime": "2013-08-23T01:02:15.422Z",
17.         "Capabilities": [],
18.         "StackName": "myteststack",
19.         "StackStatus": "CREATE_COMPLETE",
20.         "DisableRollback": false
21.     }
22. ]
```

The following example describes the `myteststack` stack events:

```
 1. PROMPT> aws cloudformation describe-stack-events --stack-name myteststack
 2. {
 3.     "StackEvents": [
 4.         {
 5.             "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
 6.             "EventId": "af67ef60-0b8f-11e3-8b8a-500150b352e0",
 7.             "ResourceStatus": "CREATE_COMPLETE",
 8.             "ResourceType": "AWS::CloudFormation::Stack",
 9.             "Timestamp": "2013-08-23T01:02:30.070Z",
10.             "StackName": "myteststack",
11.             "PhysicalResourceId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/a69442d0-0b8f-11e3-8b8a-500150b352e0",
12.             "LogicalResourceId": "myteststack"
13.         },
14.         {
15.             "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
16.             "EventId": "S3Bucket-CREATE_COMPLETE-1377219748025",
17.             "ResourceStatus": "CREATE_COMPLETE",
18.             "ResourceType": "AWS::S3::Bucket",
19.             "Timestamp": "2013-08-23T01:02:28.025Z",
20.             "StackName": "myteststack",
21.             "ResourceProperties": "{\"AccessControl\":\"PublicRead\"}",
22.             "PhysicalResourceId": "myteststack-s3bucket-jssofi1zie2w",
23.             "LogicalResourceId": "S3Bucket"
24.         },
25.         {
26.             "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
27.             "EventId": "S3Bucket-CREATE_IN_PROGRESS-1377219746688",
28.             "ResourceStatus": "CREATE_IN_PROGRESS",
29.             "ResourceType": "AWS::S3::Bucket",
30.             "Timestamp": "2013-08-23T01:02:26.688Z",
31.             "ResourceStatusReason": "Resource creation Initiated",
32.             "StackName": "myteststack",
33.             "ResourceProperties": "{\"AccessControl\":\"PublicRead\"}",
34.             "PhysicalResourceId": "myteststack-s3bucket-jssofi1zie2w",
35.             "LogicalResourceId": "S3Bucket"
36.         },
37.         {
38.             "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
39.             "EventId": "S3Bucket-CREATE_IN_PROGRESS-1377219743862",
40.             "ResourceStatus": "CREATE_IN_PROGRESS",
41.             "ResourceType": "AWS::S3::Bucket",
42.             "Timestamp": "2013-08-23T01:02:23.862Z",
43.             "StackName": "myteststack",
44.             "ResourceProperties": "{\"AccessControl\":\"PublicRead\"}",
45.             "PhysicalResourceId": null,
46.             "LogicalResourceId": "S3Bucket"
47.         },
48.         {
49.             "StackId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
50.             "EventId": "a69469e0-0b8f-11e3-8b8a-500150b352e0",
51.             "ResourceStatus": "CREATE_IN_PROGRESS",
52.             "ResourceType": "AWS::CloudFormation::Stack",
53.             "Timestamp": "2013-08-23T01:02:15.422Z",
54.             "ResourceStatusReason": "User Initiated",
55.             "StackName": "myteststack",
56.             "PhysicalResourceId": "arn:aws:cloudformation:us-east-2:123456789012:stack/myteststack/a69442d0-0b8f-11e3-8b8a-500150b352e0",
57.             "LogicalResourceId": "myteststack"
58.         }
59.     ]
60. }
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