# AWS::EC2::FlowLog<a name="aws-resource-ec2-flowlog"></a>

Specifies an Amazon Elastic Compute Cloud \(Amazon EC2\) flow log that captures IP traffic for a specified network interface, subnet, or VPC\. To view the log data, use Amazon CloudWatch Logs \(CloudWatch Logs\) to help troubleshoot connection issues\. For example, you can use a flow log to investigate why certain traffic isn't reaching an instance, which can help you diagnose overly restrictive security group rules\. For more information, see [VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html) in the *Amazon VPC User Guide*\.

## Syntax<a name="aws-resource-ec2-flowlog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-flowlog-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::FlowLog",
  "Properties" : {
      "[DeliverLogsPermissionArn](#cfn-ec2-flowlog-deliverlogspermissionarn)" : String,
      "[LogDestination](#cfn-ec2-flowlog-logdestination)" : String,
      "[LogDestinationType](#cfn-ec2-flowlog-logdestinationtype)" : String,
      "[LogGroupName](#cfn-ec2-flowlog-loggroupname)" : String,
      "[ResourceId](#cfn-ec2-flowlog-resourceid)" : String,
      "[ResourceType](#cfn-ec2-flowlog-resourcetype)" : String,
      "[TrafficType](#cfn-ec2-flowlog-traffictype)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-flowlog-syntax.yaml"></a>

```
Type: AWS::EC2::FlowLog
Properties: 
  [DeliverLogsPermissionArn](#cfn-ec2-flowlog-deliverlogspermissionarn): String
  [LogDestination](#cfn-ec2-flowlog-logdestination): String
  [LogDestinationType](#cfn-ec2-flowlog-logdestinationtype): String
  [LogGroupName](#cfn-ec2-flowlog-loggroupname): String
  [ResourceId](#cfn-ec2-flowlog-resourceid): String
  [ResourceType](#cfn-ec2-flowlog-resourcetype): String
  [TrafficType](#cfn-ec2-flowlog-traffictype): String
```

## Properties<a name="aws-resource-ec2-flowlog-properties"></a>

`DeliverLogsPermissionArn`  <a name="cfn-ec2-flowlog-deliverlogspermissionarn"></a>
The ARN for the IAM role that permits Amazon EC2 to publish flow logs to a CloudWatch Logs log group in your account\.  
If you specify `LogDestinationType` as `s3`, do not specify `DeliverLogsPermissionArn` or `LogGroupName`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogDestination`  <a name="cfn-ec2-flowlog-logdestination"></a>
Specifies the destination to which the flow log data is to be published\. Flow log data can be published to a CloudWatch Logs log group or an Amazon S3 bucket\. The value specified for this parameter depends on the value specified for `LogDestinationType`\.  
If LogDestinationType is not specified or `cloud-watch-logs`, specify the Amazon Resource Name \(ARN\) of the CloudWatch Logs log group\.  
If LogDestinationType is `s3`, specify the ARN of the Amazon S3 bucket\. You can also specify a subfolder in the bucket\. To specify a subfolder in the bucket, use the following ARN format: `bucket_ARN/subfolder_name/`\. For example, to specify a subfolder named `my-logs` in a bucket named `my-bucket`, use the following ARN: `arn:aws:s3:::my-bucket/my-logs/`\. You cannot use `AWSLogs` as a subfolder name\. This is a reserved term\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogDestinationType`  <a name="cfn-ec2-flowlog-logdestinationtype"></a>
Specifies the type of destination to which the flow log data is to be published\. Flow log data can be published to CloudWatch Logs or Amazon S3\. To publish flow log data to CloudWatch Logs, specify `cloud-watch-logs`\. To publish flow log data to Amazon S3, specify `s3`\.  
If you specify `LogDestinationType` as `s3`, do not specify `DeliverLogsPermissionArn` or `LogGroupName`\.  
Default: `cloud-watch-logs`   
*Required*: No  
*Type*: String  
*Allowed Values*: `cloud-watch-logs | s3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogGroupName`  <a name="cfn-ec2-flowlog-loggroupname"></a>
The name of a new or existing CloudWatch Logs log group where Amazon EC2 publishes your flow logs\.  
If you specify `LogDestinationType` as `s3`, do not specify `DeliverLogsPermissionArn` or `LogGroupName`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceId`  <a name="cfn-ec2-flowlog-resourceid"></a>
The ID of the subnet, network interface, or VPC for which you want to create a flow log\.  
Constraints: Maximum of 1000 resources  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceType`  <a name="cfn-ec2-flowlog-resourcetype"></a>
The type of resource for which to create the flow log\. For example, if you specified a VPC ID for the `ResourceId` property, specify `VPC` for this property\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `NetworkInterface | Subnet | VPC`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TrafficType`  <a name="cfn-ec2-flowlog-traffictype"></a>
The type of traffic to log\. You can log traffic that the resource accepts or rejects, or all traffic\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `ACCEPT | ALL | REJECT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-ec2-flowlog-return-values"></a>

### Ref<a name="aws-resource-ec2-flowlog-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the flow log ID, such as `fl-1a23b456`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-flowlog--examples"></a>

### Creating a flow log that monitors all traffic types<a name="aws-resource-ec2-flowlog--examples--Creating_a_flow_log_that_monitors_all_traffic_types"></a>

The following example creates a flow log for the VPC called MyVPC and logs all traffic types\. Amazon EC2 publishes the logs to the `FlowLogsGroup` log group\.

#### JSON<a name="aws-resource-ec2-flowlog--examples--Creating_a_flow_log_that_monitors_all_traffic_types--json"></a>

```
"MyFlowLog" : {
  "Type" : "AWS::EC2::FlowLog",
  "Properties" : {
    "DeliverLogsPermissionArn" : { "Fn::GetAtt" : ["FlowLogRole", "Arn"] },
    "LogGroupName" : "FlowLogsGroup",
    "ResourceId" : { "Ref" : "MyVPC" },
    "ResourceType" : "VPC",
    "TrafficType" : "ALL"
  }
}
```

#### YAML<a name="aws-resource-ec2-flowlog--examples--Creating_a_flow_log_that_monitors_all_traffic_types--yaml"></a>

```
MyFlowLog:
  Type: AWS::EC2::FlowLog
  Properties:
    DeliverLogsPermissionArn: !GetAtt FlowLogRole.Arn
    LogGroupName: FlowLogsGroup
    ResourceId: !Ref MyVPC
    ResourceType: VPC
    TrafficType: ALL
```