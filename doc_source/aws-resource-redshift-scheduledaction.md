# AWS::Redshift::ScheduledAction<a name="aws-resource-redshift-scheduledaction"></a>

Creates a scheduled action\. A scheduled action contains a schedule and an Amazon Redshift API action\. For example, you can create a schedule of when to run the `ResizeCluster` API operation\. 

## Syntax<a name="aws-resource-redshift-scheduledaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-scheduledaction-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ScheduledAction",
  "Properties" : {
      "[Enable](#cfn-redshift-scheduledaction-enable)" : Boolean,
      "[EndTime](#cfn-redshift-scheduledaction-endtime)" : String,
      "[IamRole](#cfn-redshift-scheduledaction-iamrole)" : String,
      "[Schedule](#cfn-redshift-scheduledaction-schedule)" : String,
      "[ScheduledActionDescription](#cfn-redshift-scheduledaction-scheduledactiondescription)" : String,
      "[ScheduledActionName](#cfn-redshift-scheduledaction-scheduledactionname)" : String,
      "[StartTime](#cfn-redshift-scheduledaction-starttime)" : String,
      "[TargetAction](#cfn-redshift-scheduledaction-targetaction)" : ScheduledActionType
    }
}
```

### YAML<a name="aws-resource-redshift-scheduledaction-syntax.yaml"></a>

```
Type: AWS::Redshift::ScheduledAction
Properties: 
  [Enable](#cfn-redshift-scheduledaction-enable): Boolean
  [EndTime](#cfn-redshift-scheduledaction-endtime): String
  [IamRole](#cfn-redshift-scheduledaction-iamrole): String
  [Schedule](#cfn-redshift-scheduledaction-schedule): String
  [ScheduledActionDescription](#cfn-redshift-scheduledaction-scheduledactiondescription): String
  [ScheduledActionName](#cfn-redshift-scheduledaction-scheduledactionname): String
  [StartTime](#cfn-redshift-scheduledaction-starttime): String
  [TargetAction](#cfn-redshift-scheduledaction-targetaction): 
    ScheduledActionType
```

## Properties<a name="aws-resource-redshift-scheduledaction-properties"></a>

`Enable`  <a name="cfn-redshift-scheduledaction-enable"></a>
If true, the schedule is enabled\. If false, the scheduled action does not trigger\. For more information about `state` of the scheduled action, see [AWS::Redshift::ScheduledAction](#aws-resource-redshift-scheduledaction)\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndTime`  <a name="cfn-redshift-scheduledaction-endtime"></a>
The end time in UTC when the schedule is no longer active\. After this time, the scheduled action does not trigger\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRole`  <a name="cfn-redshift-scheduledaction-iamrole"></a>
The IAM role to assume to run the scheduled action\. This IAM role must have permission to run the Amazon Redshift API operation in the scheduled action\. This IAM role must allow the Amazon Redshift scheduler \(Principal scheduler\.redshift\.amazonaws\.com\) to assume permissions on your behalf\. For more information about the IAM role to use with the Amazon Redshift scheduler, see [Using Identity\-Based Policies for Amazon Redshift](https://docs.aws.amazon.com/redshift/latest/mgmt/redshift-iam-access-control-identity-based.html) in the *Amazon Redshift Cluster Management Guide*\.   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-redshift-scheduledaction-schedule"></a>
The schedule for a one\-time \(at format\) or recurring \(cron format\) scheduled action\. Schedule invocations must be separated by at least one hour\.  
Format of at expressions is "`at(yyyy-mm-ddThh:mm:ss)`"\. For example, "`at(2016-03-04T17:27:00)`"\.  
Format of cron expressions is "`cron(Minutes Hours Day-of-month Month Day-of-week Year)`"\. For example, "`cron(0 10 ? * MON *)`"\. For more information, see [Cron Expressions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/ScheduledEvents.html#CronExpressions) in the *Amazon CloudWatch Events User Guide*\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduledActionDescription`  <a name="cfn-redshift-scheduledaction-scheduledactiondescription"></a>
The description of the scheduled action\.   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduledActionName`  <a name="cfn-redshift-scheduledaction-scheduledactionname"></a>
The name of the scheduled action\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartTime`  <a name="cfn-redshift-scheduledaction-starttime"></a>
The start time in UTC when the schedule is active\. Before this time, the scheduled action does not trigger\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetAction`  <a name="cfn-redshift-scheduledaction-targetaction"></a>
A JSON format string of the Amazon Redshift API operation with input parameters\.   
"`{\"ResizeCluster\":{\"NodeType\":\"ds2.8xlarge\",\"ClusterIdentifier\":\"my-test-cluster\",\"NumberOfNodes\":3}}`"\.   
*Required*: No  
*Type*: [ScheduledActionType](aws-properties-redshift-scheduledaction-scheduledactiontype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-redshift-scheduledaction-return-values"></a>

### Ref<a name="aws-resource-redshift-scheduledaction-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myScheduledActionName" }` 

For the Amazon Redshift `ScheduledActionName`, Ref returns the name of the scheduled action\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-redshift-scheduledaction-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-redshift-scheduledaction-return-values-fn--getatt-fn--getatt"></a>

`NextInvocations`  <a name="NextInvocations-fn::getatt"></a>
List of times when the scheduled action will run\. 

`State`  <a name="State-fn::getatt"></a>
The state of the scheduled action\. For example, `DISABLED`\. 