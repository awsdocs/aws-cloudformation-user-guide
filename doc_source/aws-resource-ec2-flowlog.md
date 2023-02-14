# AWS::EC2::FlowLog<a name="aws-resource-ec2-flowlog"></a>

Specifies a VPC flow log that captures IP traffic for a specified network interface, subnet, or VPC\. To view the log data, use Amazon CloudWatch Logs \(CloudWatch Logs\) to help troubleshoot connection issues\. For example, you can use a flow log to investigate why certain traffic isn't reaching an instance, which can help you diagnose overly restrictive security group rules\. For more information, see [VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html) in the *Amazon VPC User Guide*\.

## Syntax<a name="aws-resource-ec2-flowlog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-flowlog-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::FlowLog",
  "Properties" : {
      "[DeliverLogsPermissionArn](#cfn-ec2-flowlog-deliverlogspermissionarn)" : String,
      "[DestinationOptions](#cfn-ec2-flowlog-destinationoptions)" : DestinationOptions,
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
  [DestinationOptions](#cfn-ec2-flowlog-destinationoptions): 
    DestinationOptions
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
The ARN of the IAM role that allows Amazon EC2 to publish flow logs to a CloudWatch Logs log group in your account\.  
This parameter is required if the destination type is `cloud-watch-logs` and unsupported otherwise\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationOptions`  <a name="cfn-ec2-flowlog-destinationoptions"></a>
The destination options\. The following options are supported:  
+ `FileFormat` \- The format for the flow log \(`plain-text` \| `parquet`\)\. The default is `plain-text`\.
+ `HiveCompatiblePartitions` \- Indicates whether to use Hive\-compatible prefixes for flow logs stored in Amazon S3 \(`true` \| `false`\)\. The default is `false`\.
+ `PerHourPartition` \- Indicates whether to partition the flow log per hour \(`true` \| `false`\)\. The default is `false`\.
*Required*: No  
*Type*: [DestinationOptions](aws-properties-ec2-flowlog-destinationoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogDestination`  <a name="cfn-ec2-flowlog-logdestination"></a>
The destination for the flow log data\. The meaning of this parameter depends on the destination type\.  
+ If the destination type is `cloud-watch-logs`, specify the ARN of a CloudWatch Logs log group\. For example:

  arn:aws:logs:*region*:*account\_id*:log\-group:*my\_group* 

  Alternatively, use the `LogGroupName` parameter\.
+ If the destination type is `s3`, specify the ARN of an S3 bucket\. For example:

  arn:aws:s3:::*my\_bucket*/*my\_subfolder*/

  The subfolder is optional\. Note that you can't use `AWSLogs` as a subfolder name\.
+ If the destination type is `kinesis-data-firehose`, specify the ARN of a Kinesis Data Firehose delivery stream\. For example:

  arn:aws:firehose:*region*:*account\_id*:deliverystream:*my\_stream* 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogDestinationType`  <a name="cfn-ec2-flowlog-logdestinationtype"></a>
The type of destination for the flow log data\.  
Default: `cloud-watch-logs`   
*Required*: No  
*Type*: String  
*Allowed values*: `cloud-watch-logs | kinesis-data-firehose | s3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogFormat`  <a name="cfn-ec2-flowlog-logformat"></a>
The fields to include in the flow log record, in the order in which they should appear\. If you omit this parameter, the flow log is created using the default format\. If you specify this parameter, you must include at least one field\. For more information about the available fields, see [Flow log records](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html#flow-log-records) in the *Amazon VPC User Guide* or [Transit Gateway Flow Log records](https://docs.aws.amazon.com/vpc/latest/tgw/tgw-flow-logs.html#flow-log-records) in the *AWS Transit Gateway Guide*\.  
Specify the fields using the `${field-id}` format, separated by spaces\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogGroupName`  <a name="cfn-ec2-flowlog-loggroupname"></a>
The name of a new or existing CloudWatch Logs log group where Amazon EC2 publishes your flow logs\.  
This parameter is valid only if the destination type is `cloud-watch-logs`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxAggregationInterval`  <a name="cfn-ec2-flowlog-maxaggregationinterval"></a>
The maximum interval of time during which a flow of packets is captured and aggregated into a flow log record\. The possible values are 60 seconds \(1 minute\) or 600 seconds \(10 minutes\)\. This parameter must be 60 seconds for transit gateway resource types\.  
When a network interface is attached to a [Nitro\-based instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances), the aggregation interval is always 60 seconds or less, regardless of the value that you specify\.  
Default: 600  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceId`  <a name="cfn-ec2-flowlog-resourceid"></a>
The ID of the resource to monitor\. For example, if the resource type is `VPC`, specify the ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceType`  <a name="cfn-ec2-flowlog-resourcetype"></a>
The type of resource to monitor\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `NetworkInterface | Subnet | TransitGateway | TransitGatewayAttachment | VPC`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-flowlog-tags"></a>
The tags to apply to the flow logs\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficType`  <a name="cfn-ec2-flowlog-traffictype"></a>
The type of traffic to monitor \(accepted traffic, rejected traffic, or all traffic\)\. This parameter is not supported for transit gateway resource types\. It is required for the other resource types\.  
*Required*: No  
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
    LogFormat: ${version} ${vpc-id} ${subnet-id} ${instance-id} ${srcaddr} ${dstaddr} ${srcport} ${dstport} ${protocol} ${tcp-flags} ${type} ${pkt-srcaddr} ${pkt-dstaddr}
    MaxAggregationInterval: 60
    Tags:
      - Key: Name
        Value: FlowLogForSubnetA
      - Key: Purpose
        Value: RejectTraffic
```

### Publish a custom format flow log to Amazon S3 for ACCEPT traffic<a name="aws-resource-ec2-flowlog--examples--Publish_a_custom_format_flow_log_to_Amazon_S3_for_ACCEPT_traffic"></a>

The following example creates a flow log for the specified subnet and captures ACCEPT traffic\. The flow log uses a custom log format \(the `LogFormat` property uses the `${field-id}` format, separated by spaces\)\. Amazon EC2 aggregates the logs over 60 second intervals, and publishes the logs to an Amazon S3 bucket that's referenced by its ARN, `MyS3Bucket.Arn`\. The logs are published in parquet format in Hive\-compatible prefixes partitioned on an hourly basis\. The flow log is created with two tags\.

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
      "DestinationOptions": {
        "FileFormat": "parquet",
        "HiveCompatiblePartitions": true,
        "PerHourPartition": true
      },
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
    LogFormat: ${version} ${vpc-id} ${subnet-id} ${instance-id} ${srcaddr} ${dstaddr} ${srcport} ${dstport} ${protocol} ${tcp-flags} ${type} ${pkt-srcaddr} ${pkt-dstaddr}
    MaxAggregationInterval: 60
    DestinationOptions:
      FileFormat: parquet
      HiveCompatiblePartitions: true
      PerHourPartition: true
    Tags:
      - Key: Name
        Value: FlowLogForSubnetB
      - Key: Purpose
        Value: AcceptTraffic
```