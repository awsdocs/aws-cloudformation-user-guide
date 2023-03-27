# Managing events with AWS CloudFormation and Amazon EventBridge<a name="stacks-event-bridge"></a>

AWS CloudFormation can send events to Amazon EventBridge whenever a create, update, delete, or drift\-detection operation performs on your stack\. AWS CloudFormation also sends events to Amazon EventBridge for status changes to StackSets\. You can use EventBridge rules to route events to your defined targets\. These events will be delivered on a best\-effort basis, and they might be delivered out of order\.

Discover CloudFormation events and setup additional workflows based on those events\. CloudFormation provides information about changes to CloudFormation stacks or StackSets and its resources, so you can subscribe to and imitate workflows associated with respective events\. For example:
+ Create stack or StackSet specific tags on all resource provisioned through AWS CloudFormation\.
+ Establish an association between a CloudFormation stack or StackSet and an Amazon WorkSpaces Application Manager \(Amazon WAM\)\.
+ Specify an association with an AppRegistry for the created stack or StackSet\.

## Supported events<a name="supported-events"></a>

All events are provided by the create, update, delete \(CUD\), and drift\-detection actions associated with stack and StackSet operations\. For more information, see [Event type message structure](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/eventbridge-events.html)\.

The following events are supported by CloudFormation\.


| Event type | Description | 
| --- |--- |
| Resource status | Any updates performed on a stack which changes underlying resource properties\. For a complete list of supported AWS resource types, see [AWS resource and property types reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html) | 
| Stack status | Any status change updates on a stack provisioned by the user\. For a complete list of stack status codes, see [Stack status codes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html#cli-stack-status-codes)\. | 
| Drift detection status |  User initiated drift detection updates on stacks\. For a complete list of fully mutable and immutable types that support drift detection, see [Resources that support import and drift detection operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)  | 
| StackSet status | Status changes for a specific StackSet\. The statuses are limited to ACTIVE and DELETED\. | 
| StackSet stack instance status | Status changes for a specific StackSet Stack instance\. For a complete list of status codes for stack instances within a StackSet, see [Stack instance status codes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html#stack-instance-status-codes)\. | 
| StackSet operation status | Status changes for a given StackSet operation\. For a complete list of status codes for StackSet operations, see [StackSet status codes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html#stackset-status-codes)\. | 