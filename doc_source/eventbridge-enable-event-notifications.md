# Enabling Amazon EventBridge<a name="eventbridge-enable-event-notifications"></a>

CloudFormation sends events to Amazon EventBridge by default\. Specify the rules and targets to match to the events using the CloudFormation console and AWS Command Line Interface \(AWS CLI\)\.

When EventBridge receives an event, it applies a rule to route the event to a target\. Rules match events to target based on either the structure of the event or on a schedule\.

## AWS Management Console<a name="eventbridge-console"></a>

1. To get started, log in to the EventBridge console\.

1. From the navigation pane, select **Rules**\.

1. Select **Create rule**\.

1. From the **Create rule** page, enter the following:

   1. Enter a name and description for the rule\.

   1. For **Define pattern**, choose **Event pattern**\.

      Select, **Pre\-defined pattern by service** followed by, **AWS**, **CloudFormation**, and your event type\.

   1. For **Select event bus**, choose **AWS default event bus**\. You can only create scheduled rules on the default event bus\.

   1. For **Select targets**, choose **Batch job queue** and specify the following fields appropriately:
      + **Job queue:** Enter the Amazon Resource Name \(ARN\) of the job queue to schedule your job in\.
      + **Job definition:** Enter the name and revision or full ARN of the job definition to use for your job\.
      + **Job name:** Enter a name for your job\.
      + **Array size:** \(Optional\) Enter an array size for your job to run more than one copy\.
      + **Job attempts:** \(Optional\) Enter the number of times to retry your job if it fails\.

1. For **Batch job queue** target types, EventBridge needs permission to send events to the target\. EventBridge can create the IAM role needed for your rule to run\. Do one of these things:
   + To create an IAM role automatically, choose **Create a new role for this specific resource**\.
   + To use an IAM role that you created before, choose **Use existing role**\.

1. For **Retry policy and dead\-letter queue:**, under **Retry policy**:

   1. For **Maximum age of event**, enter a value between 1 minute \(00:01\) and 24 hours \(24:00\)\.

   1. For **Retry attempts**, enter a number between 0 and 185\.

1. For **Dead\-letter queue**, choose whether to use a standard Amazon SQS queue as a dead\-letter queue\. EventBridge sends events that match this rule to the dead\-letter queue if it can't deliver them to the target\. Do one of the following:
   + Choose **None** to not use a dead\-letter queue\.
   + Choose **Select an Amazon SQS queue in the current AWS account to use as the dead\-letter queue** and then select the queue to use from the drop down list\.
   + Choose **Select an Amazon SQS queue in an other AWS account as a dead\-letter queue** and then enter the ARN of the queue to use\. You must attach a resource\-based policy to the queue that grants EventBridge permission to send messages to it\.

1. \(Optional\) Enter one or more tags for the rule\.

1. Choose **Create**\.

## EventBridge Event pattern<a name="console-event-pattern"></a>

The following are examples event patterns used in the EventBridge console\. Use these to create rules and send notifications\.

### Resource status event<a name="resource-status-event-event-pattern"></a>

The following example sends a notification to Amazon EventBridge when an event causes a change in the resource status\.

![\[Resource status event.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/event-bridge-resource-status-change.png)

### Stack status event<a name="stack-status-event-event-pattern"></a>

The following example sends a notification to Amazon EventBridge when an event causes a change in the stack status\.

![\[Stack status event.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/event-bridge-stack-status-change.png)

### Drift detection status event<a name="drift-detection-status-event-pattern"></a>

The following example sends a notification to Amazon EventBridge when drift detection identifies a status event\.

![\[Drift detection status event.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/event-bridge-drift-detection-status.png)

### StackSet status event<a name="stackset-status-event-pattern"></a>

The following example sends a notification to Amazon EventBridge when an event causes a change in the StackSet status\.

![\[StackSet status event.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/CloudFormation StackSet Status Change.png)

### StackSet stack instance status event<a name="stackset-stack-instance-status-event-pattern"></a>

The following example sends a notification to Amazon EventBridge when an event causes a change in the StackSet stack instance status\.

![\[StackSet stack instance status event.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/CloudFormation StackSet StackInstance Status Change.png)

### StackSet operation status event<a name="stackset-operation-status-event-pattern"></a>

The following example sends a notification to Amazon EventBridge when an event causes a change in the StackSet operation status\.

![\[StackSet operation status event.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/CloudFormation StackSet Operation Status Change.png)

## AWS CLI<a name="eventbridge-cli"></a>

Use the `create-stack`, `update-stack`, and `delete-stack` to send the generated events to Amazon EventBridge\.

The following example creates a stack and sends a notification to Amazon EventBridge \.

```
aws cloudformation create-stack --stack-name myteststack --template-body file://sampletemplate.json --parameters ParameterKey=KeyPairName,ParameterValue=TestKey ParameterKey=SubnetIDs,ParameterValue=SubnetID1\\,SubnetID2
```

The following example updates a stack and sends a notification to Amazon EventBridge \.

```
aws cloudformation update-stack --stack-name myteststack --template-url https://s3.amazonaws.com/sample/sampletemplate.json --parameters ParameterKey=KeyPairName,ParameterValue=SampleKeyPair ParameterKey=SubnetIDs,ParameterValue=SampleSubnetID1\\,SampleSubnetID2
```

The following example deletes a stack and sends a notification to Amazon EventBridge \.

```
aws cloudformation delete-stack --stack-name myteststack
```

The following example detects drift on a stack and sends a notification to Amazon EventBridge\.

```
aws cloudformation detect-stack-drift --stack-name myteststack
```

## Amazon EventBridge permissions<a name="eventbridge-permissions"></a>

AWS CloudFormation doesn't require any additional permissions to deliver events to Amazon EventBridge\.

The events contain information which is already available through CloudFormation's API operations\.

## Amazon EventBridge troubleshooting<a name="eventbridge-troubleshooting"></a>

For information about how to troubleshoot EventBridge, see [Troubleshooting Amazon EventBridge](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-troubleshooting.html) in the *Amazon EventBridge User Guide*\.