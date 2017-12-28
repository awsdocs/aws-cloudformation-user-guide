# AWS::EC2::FlowLog<a name="aws-resource-ec2-flowlog"></a>

The `AWS::EC2::FlowLog` resource creates an Amazon Elastic Compute Cloud \(Amazon EC2\) flow log that captures IP traffic for a specified network interface, subnet, or VPC\. To view the log data, use Amazon CloudWatch Logs \(CloudWatch Logs\) to help troubleshoot connection issues\. For example, you can use a flow log to investigate why certain traffic isn't reaching an instance, which can help you diagnose overly restrictive security group rules\. For more information, see [VPC Flow Logs](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/flow-logs.html) in the *Amazon VPC User Guide*\.


+ [Syntax](#aws-resource-ec2-flowlog-syntax)
+ [Properties](#w3ab2c21c10d364b9)
+ [Return Value](#w3ab2c21c10d364c11)
+ [Example](#w3ab2c21c10d364c13)

## Syntax<a name="aws-resource-ec2-flowlog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-flowlog-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::FlowLog",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-deliverlogspermissionarn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-loggroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-resourceid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-resourcetype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-traffictype)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-flowlog-syntax.yaml"></a>

```
Type: "AWS::EC2::FlowLog"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-deliverlogspermissionarn) : String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-loggroupname) : String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-resourceid) : String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-resourcetype) : String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-flowlog-traffictype) : String
```

## Properties<a name="w3ab2c21c10d364b9"></a>

`DeliverLogsPermissionArn`  
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that permits Amazon EC2 to publish flow logs to a CloudWatch Logs log group in your account\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`LogGroupName`  
The name of a new or existing CloudWatch Logs log group where Amazon EC2 publishes your flow logs\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`ResourceId`  
The ID of the subnet, network interface, or VPC for which you want to create a flow log\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`ResourceType`  
The type of resource that you specified in the `ResourceId` property\. For example, if you specified a VPC ID for the `ResourceId` property, specify `VPC` for this property\. For valid values, see the `ResourceType` parameter for the [CreateFlowLogs](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFlowLogs.html) action in the *Amazon EC2 API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`TrafficType`  
The type of traffic to log\. You can log traffic that the resource accepts or rejects, or all traffic\. For valid values, see the `TrafficType` parameter for the [CreateFlowLogs](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFlowLogs.html) action in the *Amazon EC2 API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Return Value<a name="w3ab2c21c10d364c11"></a>

### Ref<a name="w3ab2c21c10d364c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the flow log ID, such as `fl-1a23b456`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d364c13"></a>

The following example creates a flow log for the VPC called `MyVPC` and logs all traffic types\. Amazon EC2 publishes the logs to the `FlowLogsGroup` log group\.

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