# AWS::NetworkFirewall::LoggingConfiguration<a name="aws-resource-networkfirewall-loggingconfiguration"></a>

Use the [AWS::NetworkFirewall::LoggingConfiguration](#aws-resource-networkfirewall-loggingconfiguration) to define the destinations and logging options for an [AWS::NetworkFirewall::Firewall](aws-resource-networkfirewall-firewall.md)\. 

You must change the logging configuration by changing one `LogDestinationConfig` setting at a time in your `LogDestinationConfigs`\. 

You can make only one of the following changes to your [AWS::NetworkFirewall::LoggingConfiguration](#aws-resource-networkfirewall-loggingconfiguration) resource: 
+ Create a new log destination object by adding a single `LogDestinationConfig` array element to `LogDestinationConfigs`\.
+ Delete a log destination object by removing a single `LogDestinationConfig` array element from `LogDestinationConfigs`\.
+ Change the `LogDestination` setting in a single `LogDestinationConfig` array element\.

You can't change the `LogDestinationType` or `LogType` in a `LogDestinationConfig`\. To change these settings, delete the existing `LogDestinationConfig` object and create a new one, in two separate modifications\. 

## Syntax<a name="aws-resource-networkfirewall-loggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkfirewall-loggingconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkFirewall::LoggingConfiguration",
  "Properties" : {
      "[FirewallArn](#cfn-networkfirewall-loggingconfiguration-firewallarn)" : String,
      "[FirewallName](#cfn-networkfirewall-loggingconfiguration-firewallname)" : String,
      "[LoggingConfiguration](#cfn-networkfirewall-loggingconfiguration-loggingconfiguration)" : LoggingConfiguration
    }
}
```

### YAML<a name="aws-resource-networkfirewall-loggingconfiguration-syntax.yaml"></a>

```
Type: AWS::NetworkFirewall::LoggingConfiguration
Properties: 
  [FirewallArn](#cfn-networkfirewall-loggingconfiguration-firewallarn): String
  [FirewallName](#cfn-networkfirewall-loggingconfiguration-firewallname): String
  [LoggingConfiguration](#cfn-networkfirewall-loggingconfiguration-loggingconfiguration): 
    LoggingConfiguration
```

## Properties<a name="aws-resource-networkfirewall-loggingconfiguration-properties"></a>

`FirewallArn`  <a name="cfn-networkfirewall-loggingconfiguration-firewallarn"></a>
The Amazon Resource Name \(ARN\) of the [AWS::NetworkFirewall::Firewall](aws-resource-networkfirewall-firewall.md) that the logging configuration is associated with\. You can't change the firewall specification after you create the logging configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FirewallName`  <a name="cfn-networkfirewall-loggingconfiguration-firewallname"></a>
The name of the firewall that the logging configuration is associated with\. You can't change the firewall specification after you create the logging configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingConfiguration`  <a name="cfn-networkfirewall-loggingconfiguration-loggingconfiguration"></a>
Defines how AWS Network Firewall performs logging for a [AWS::NetworkFirewall::Firewall](aws-resource-networkfirewall-firewall.md)\.   
*Required*: Yes  
*Type*: [LoggingConfiguration](aws-properties-networkfirewall-loggingconfiguration-loggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-networkfirewall-loggingconfiguration-return-values"></a>

### Ref<a name="aws-resource-networkfirewall-loggingconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the firewall that the logging configuration is associated with\. For example: 

 `{ "Ref": "arn:aws:network-firewall:us-east-1:012345678901:firewall/myFirewallName" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-networkfirewall-loggingconfiguration--examples"></a>



### Create a logging configuration for CloudWatch Logs and Kinesis Data Firehose<a name="aws-resource-networkfirewall-loggingconfiguration--examples--Create_a_logging_configuration_for_CloudWatch_Logs_and_Kinesis_Data_Firehose_"></a>

The following shows example logging configuration specifications for alert logs that go to an AWS CloudWatch Logs log group and flow logs that go to an Amazon Kinesis Data Firehose delivery stream\. 

#### JSON<a name="aws-resource-networkfirewall-loggingconfiguration--examples--Create_a_logging_configuration_for_CloudWatch_Logs_and_Kinesis_Data_Firehose_--json"></a>

```
"SampleLoggingConfiguration": {
    "Type": "AWS::NetworkFirewall::LoggingConfiguration",
    "Properties": {
        "FirewallArn": {
            "Ref": "SampleFirewallArn"
        },
        "LoggingConfiguration": {
            "LogDestinationConfigs": [
                {
                    "LogType": "ALERT",
                    "LogDestinationType": "CloudWatchLogs",
                    "LogDestination": {
                        "logGroup": "SampleLogGroup"
                    }
                },
                {
                    "LogType": "FLOW",
                    "LogDestinationType": "KinesisDataFirehose",
                    "LogDestination": {
                        "deliveryStream": "SampleStream"
                    }
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-networkfirewall-loggingconfiguration--examples--Create_a_logging_configuration_for_CloudWatch_Logs_and_Kinesis_Data_Firehose_--yaml"></a>

```
SampleLoggingConfiguration:
  Type: 'AWS::NetworkFirewall::LoggingConfiguration'
  Properties:
    FirewallArn: !Ref SampleFirewallArn
    LoggingConfiguration:
      LogDestinationConfigs:
        - LogType: ALERT
          LogDestinationType: CloudWatchLogs
          LogDestination:
            logGroup: SampleLogGroup
        - LogType: FLOW
          LogDestinationType: KinesisDataFirehose
          LogDestination:
            deliveryStream: SampleStream
```

### Create a logging configuration for Amazon S3<a name="aws-resource-networkfirewall-loggingconfiguration--examples--Create_a_logging_configuration_for_Amazon_S3"></a>

The following shows example logging configuration specifications for flow logs that go to an Amazon S3 bucket\. 

#### JSON<a name="aws-resource-networkfirewall-loggingconfiguration--examples--Create_a_logging_configuration_for_Amazon_S3--json"></a>

```
"SampleLoggingConfiguration": {
    "Type": "AWS::NetworkFirewall::LoggingConfiguration",
    "Properties": {
        "FirewallArn": {
            "Ref": "SampleFirewallArn"
        },
        "LoggingConfiguration": {
            "LogDestinationConfigs": [
                {
                    "LogType": "FLOW",
                    "LogDestinationType": "S3",
                    "LogDestination": {
                        "bucketName": "sample-bucket-name",
                        "prefix": "sample/s3/prefix"
                    }
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-networkfirewall-loggingconfiguration--examples--Create_a_logging_configuration_for_Amazon_S3--yaml"></a>

```
SampleLoggingConfiguration:
  Type: 'AWS::NetworkFirewall::LoggingConfiguration'
  Properties:
    FirewallArn: !Ref SampleFirewallArn
    LoggingConfiguration:
      LogDestinationConfigs:
        - LogType: FLOW
          LogDestinationType: S3
          LogDestination:
            bucketName: sample-bucket-name
            prefix: sample/s3/prefix
```