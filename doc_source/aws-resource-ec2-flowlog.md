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
      "[LogFormat](#cfn-ec2-flowlog-logformat)" : String,
      "[LogGroupName](#cfn-ec2-flowlog-loggroupname)" : String,
      "[MaxAggregationInterval](#cfn-ec2-flowlog-maxaggregationinterval)" : Integer,
      "[ResourceId](#cfn-ec2-flowlog-resourceid)" : String,
      "[ResourceType](#cfn-ec2-flowlog-resourcetype)" : String,
      "[Tags](#cfn-ec2-flowlog-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
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
  [LogFormat](#cfn-ec2-flowlog-logformat): String
  [LogGroupName](#cfn-ec2-flowlog-loggroupname): String
  [MaxAggregationInterval](#cfn-ec2-flowlog-maxaggregationinterval): Integer
  [ResourceId](#cfn-ec2-flowlog-resourceid): String
  [ResourceType](#cfn-ec2-flowlog-resourcetype): String
  [Tags](#cfn-ec2-flowlog-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
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
If `LogDestinationType` is not specified or `cloud-watch-logs`, specify the Amazon Resource Name \(ARN\) of the CloudWatch Logs log group\. For example, to publish to a log group called `my-logs`, specify `arn:aws:logs:us-east-1:123456789012:log-group:my-logs`\. Alternatively, use `LogGroupName` instead\.  
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
*Allowed values*: `cloud-watch-logs | s3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogFormat`  <a name="cfn-ec2-flowlog-logformat"></a>
The fields to include in the flow log record, in the order in which they should appear\. For a list of available fields, see [Flow Log Records](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html#flow-log-records)\. If you omit this parameter, the flow log is created using the default format\. If you specify this parameter, you must specify at least one field\.  
Specify the fields using the `${field-id}` format, separated by spaces\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogGroupName`  <a name="cfn-ec2-flowlog-loggroupname"></a>
The name of a new or existing CloudWatch Logs log group where Amazon EC2 publishes your flow logs\.  
If you specify `LogDestinationType` as `s3`, do not specify `DeliverLogsPermissionArn` or `LogGroupName`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxAggregationInterval`  <a name="cfn-ec2-flowlog-maxaggregationinterval"></a>
The maximum interval of time during which a flow of packets is captured and aggregated into a flow log record\. You can specify 60 seconds \(1 minute\) or 600 seconds \(10 minutes\)\.  
When a network interface is attached to a [Nitro\-based instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances), the aggregation interval is always 60 seconds or less, regardless of the value that you specify\.  
Default: 600  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceId`  <a name="cfn-ec2-flowlog-resourceid"></a>
The ID of the subnet, network interface, or VPC for which you want to create a flow log\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceType`  <a name="cfn-ec2-flowlog-resourcetype"></a>
The type of resource for which to create the flow log\. For example, if you specified a VPC ID for the `ResourceId` property, specify `VPC` for this property\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `NetworkInterface | Subnet | VPC`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-flowlog-tags"></a>
The tags for the flow log\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficType`  <a name="cfn-ec2-flowlog-traffictype"></a>
The type of traffic to log\. You can log traffic that the resource accepts or rejects, or all traffic\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ACCEPT | ALL | REJECT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-flowlog-return-values"></a>

### Ref<a name="aws-resource-ec2-flowlog-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the flow log ID, such as `fl-123456abc123abc1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-flowlog-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-flowlog-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the flow log\. For example, `fl-123456abc123abc1`\.

## Examples<a name="aws-resource-ec2-flowlog--examples"></a>

### Publish a flow log to CloudWatch Logs to monitor all traffic<a name="aws-resource-ec2-flowlog--examples--Publish_a_flow_log_to_CloudWatch_Logs_to_monitor_all_traffic"></a>

The following example creates a flow log for the specified VPC, and captures all traffic types\. Amazon EC2 publishes the logs to the `FlowLogsGroup` log group\.

#### JSON<a name="aws-resource-ec2-flowlog--examples--Publish_a_flow_log_to_CloudWatch_Logs_to_monitor_all_traffic--json"></a>

```
{
  "MyFlowLog": {
    "Type": "AWS::EC2::FlowLog",
    "Properties": {
      "DeliverLogsPermissionArn": {
        "Fn::GetAtt": [
          "FlowLogRole",
          "Arn"
        ]
      },
      "LogGroupName": "FlowLogsGroup",
      "ResourceId": {
        "Ref": "MyVPC"
      },
      "ResourceType": "VPC",
      "TrafficType": "ALL"
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-flowlog--examples--Publish_a_flow_log_to_CloudWatch_Logs_to_monitor_all_traffic--yaml"></a>

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

### Publish a custom format flow log to CloudWatch Logs for REJECT traffic<a name="aws-resource-ec2-flowlog--examples--Publish_a_custom_format_flow_log_to_CloudWatch_Logs_for_REJECT_traffic"></a>

The following example creates a flow log for the specified subnet and captures REJECT traffic\. The flow log uses a custom log format \(the `LogFormat` property uses the `${field-id}` format, separated by spaces\)\. Amazon EC2 aggregates the logs over 60 second intervals, and publishes the logs to the `FlowLogsGroup` log group\. The flow log is created with two tags\.

#### JSON<a name="aws-resource-ec2-flowlog--examples--Publish_a_custom_format_flow_log_to_CloudWatch_Logs_for_REJECT_traffic--json"></a>

```
{
  "MyDetailedFlowLogDeliveringToCloudWatchLogs": {
    "Type": "AWS::EC2::FlowLog",
    "Properties": {
      "ResourceId": {
        "Ref": "MySubnet"
      },
      "ResourceType": "Subnet",
      "TrafficType": "REJECT",
      "LogGroupName": "FlowLogsGroup",
      "DeliverLogsPermissionArn": {
        "Fn::GetAtt": [
          "FlowLogRole",
          "Arn"
        ]
      },
      "LogFormat": "${version} ${vpc-id} ${subnet-id} ${instance-id} ${srcaddr} ${dstaddr} ${srcport} ${dstport} ${protocol} ${tcp-flags} ${type} ${pkt-srcaddr} ${pkt-dstaddr}",
      "MaxAggregationInterval": 60,
      "Tags": [
        {
          "Key": "Name",
          "Value": "FlowLogForSubnetA"
        },
        {
          "Key": "Purpose",
          "Value": "RejectTraffic"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-flowlog--examples--Publish_a_custom_format_flow_log_to_CloudWatch_Logs_for_REJECT_traffic--yaml"></a>

```
MyDetailedFlowLogDeliveringToCloudWatchLogs:
  Type: AWS::EC2::FlowLog
  Properties: 
    ResourceId: !Ref MySubnet
    ResourceType: Subnet
    TrafficType: REJECT
    LogGroupName: FlowLogsGroup
    DeliverLogsPermissionArn: !GetAtt FlowLogRole.Arn
    LogFormat: '${version} ${vpc-id} ${subnet-id} ${instance-id} ${srcaddr} ${dstaddr} ${srcport} ${dstport} ${protocol} ${tcp-flags} ${type} ${pkt-srcaddr} ${pkt-dstaddr}'
    MaxAggregationInterval: 60
    Tags:
      -
        Key: Name
        Value: FlowLogForSubnetA
      -
        Key: Purpose
        Value: RejectTraffic
```

### Publish a custom format flow log to Amazon S3 for ACCEPT traffic<a name="aws-resource-ec2-flowlog--examples--Publish_a_custom_format_flow_log_to_Amazon_S3_for_ACCEPT_traffic"></a>

The following example creates a flow log for the specified subnet and captures ACCEPT traffic\. The flow log uses a custom log format \(the `LogFormat` property uses the `${field-id}` format, separated by spaces\)\. Amazon EC2 aggregates the logs over 60 second intervals, and publishes the logs to an Amazon S3 bucket that's referenced by its ARN, `MyS3Bucket.Arn`\. The flow log is created with two tags\.

#### JSON<a name="aws-resource-ec2-flowlog--examples--Publish_a_custom_format_flow_log_to_Amazon_S3_for_ACCEPT_traffic--json"></a>

```
{
  "MyFlowLogDeliveringToS3": {
    "Type": "AWS::EC2::FlowLog",
    "Properties": {
      "ResourceId": {
        "Ref": "MySubnet"
      },
      "ResourceType": "Subnet",
      "TrafficType": "ACCEPT",
      "LogDestination": {
        "Fn::GetAtt": [
          "MyS3Bucket",
          "Arn"
        ]
      },
      "LogDestinationType": "s3",
      "LogFormat": "${version} ${vpc-id} ${subnet-id} ${instance-id} ${srcaddr} ${dstaddr} ${srcport} ${dstport} ${protocol} ${tcp-flags} ${type} ${pkt-srcaddr} ${pkt-dstaddr}",
      "MaxAggregationInterval": 60,
      "Tags": [
        {
          "Key": "Name",
          "Value": "FlowLogForSubnetB"
        },
        {
          "Key": "Purpose",
          "Value": "AcceptTraffic"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-flowlog--examples--Publish_a_custom_format_flow_log_to_Amazon_S3_for_ACCEPT_traffic--yaml"></a>

```
MyFlowLogDeliveringToS3:
  Type: AWS::EC2::FlowLog
  Properties: 
    ResourceId: !Ref MySubnet
    ResourceType: Subnet
    TrafficType: ACCEPT
    LogDestination: !GetAtt MyS3Bucket.Arn
    LogDestinationType: s3
    LogFormat: '${version} ${vpc-id} ${subnet-id} ${instance-id} ${srcaddr} ${dstaddr} ${srcport} ${dstport} ${protocol} ${tcp-flags} ${type} ${pkt-srcaddr} ${pkt-dstaddr}'
    MaxAggregationInterval: 60
    Tags:
      -
        Key: Name
        Value: FlowLogForSubnetB
      -
        Key: Purpose
        Value: AcceptTraffic
```