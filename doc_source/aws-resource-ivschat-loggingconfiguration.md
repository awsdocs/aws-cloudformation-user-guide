# AWS::IVSChat::LoggingConfiguration<a name="aws-resource-ivschat-loggingconfiguration"></a>

The `AWS::IVSChat::LoggingConfiguration` resource specifies an Amazon IVS logging configuration that allows clients to store and record sent messages\. For more information, see [CreateLoggingConfiguration](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_CreateLoggingConfiguration.html) in the *Amazon Interactive Video Service Chat API Reference*\.

## Syntax<a name="aws-resource-ivschat-loggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ivschat-loggingconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::IVSChat::LoggingConfiguration",
  "Properties" : {
      "[DestinationConfiguration](#cfn-ivschat-loggingconfiguration-destinationconfiguration)" : DestinationConfiguration,
      "[Name](#cfn-ivschat-loggingconfiguration-name)" : String,
      "[Tags](#cfn-ivschat-loggingconfiguration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ivschat-loggingconfiguration-syntax.yaml"></a>

```
Type: AWS::IVSChat::LoggingConfiguration
Properties: 
  [DestinationConfiguration](#cfn-ivschat-loggingconfiguration-destinationconfiguration): 
    DestinationConfiguration
  [Name](#cfn-ivschat-loggingconfiguration-name): String
  [Tags](#cfn-ivschat-loggingconfiguration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ivschat-loggingconfiguration-properties"></a>

`DestinationConfiguration`  <a name="cfn-ivschat-loggingconfiguration-destinationconfiguration"></a>
The DestinationConfiguration is a complex type that contains information about where chat content will be logged\.  
*Required*: Yes  
*Type*: [DestinationConfiguration](aws-properties-ivschat-loggingconfiguration-destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ivschat-loggingconfiguration-name"></a>
Logging\-configuration name\. The value does not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9-_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ivschat-loggingconfiguration-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ivschat-loggingconfiguration-return-values"></a>

### Ref<a name="aws-resource-ivschat-loggingconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the logging\-configuration ARN\. For example:

 `{ "Ref": "myLoggingConfiguration" }` 

For the Amazon IVS logging configuration `myLoggingConfiguration`, `Ref` returns the logging\-configuration ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ivschat-loggingconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ivschat-loggingconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The logging\-configuration ARN\. For example: `arn:aws:ivschat:us-west-2:123456789012:logging-configuration/abcdABCDefgh`

`Id`  <a name="Id-fn::getatt"></a>
The logging\-configuration ID\. For example: `abcdABCDefgh`

`State`  <a name="State-fn::getatt"></a>
Indicates the current state of the logging configuration\. When the state is `ACTIVE`, the configuration is ready to log a chat session\. Valid values: `CREATING` \| `CREATE_FAILED` \| `DELETING` \| `DELETE_FAILED` \| `UPDATING` \| `UPDATE_FAILED` \| `ACTIVE`\.

## Examples<a name="aws-resource-ivschat-loggingconfiguration--examples"></a>



### Logging Configuration Template Examples<a name="aws-resource-ivschat-loggingconfiguration--examples--Logging_Configuration_Template_Examples"></a>

The following examples specify an Amazon IVS Chat Room that logs interactions to an S3 bucket\.

#### JSON<a name="aws-resource-ivschat-loggingconfiguration--examples--Logging_Configuration_Template_Examples--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "Bucket": {
      "Type": "AWS::S3::Bucket"
    },
    "LogGroup": {
      "Type": "AWS::Logs::LogGroup"
    },
    "DeliveryStreamRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": {
            "Effect": "Allow",
            "Principal": {
              "Service": "firehose.amazonaws.com"
            },
            "Action": "sts:AssumeRole"
          }
        }
      }
    },
    "DeliveryStream": {
      "Type": "AWS::KinesisFirehose::DeliveryStream",
      "Properties": {
        "S3DestinationConfiguration": {
          "BucketARN": {
            "Fn::GetAtt": [
              "Bucket",
              "Arn"
            ]
          },
          "RoleARN": {
            "Fn::GetAtt": [
              "DeliveryStreamRole",
              "Arn"
            ]
          }
        }
      }
    },
    "S3LoggingConfiguration": {
      "Type": "AWS::IVSChat::LoggingConfiguration",
      "Properties": {
        "Name": "S3",
        "DestinationConfiguration": {
          "S3": {
            "BucketName": {
              "Ref": "Bucket"
            }
          }
        }
      }
    },
    "CloudWatchLogsLoggingConfiguration": {
      "Type": "AWS::IVSChat::LoggingConfiguration",
      "Properties": {
        "Name": "CloudWatchLogs",
        "DestinationConfiguration": {
          "CloudWatchLogs": {
            "LogGroupName": {
              "Ref": "LogGroup"
            }
          }
        }
      }
    },
    "FirehoseLoggingConfiguration": {
      "Type": "AWS::IVSChat::LoggingConfiguration",
      "Properties": {
        "Name": "Firehose",
        "DestinationConfiguration": {
          "Firehose": {
            "DeliveryStreamName": {
              "Ref": "DeliveryStream"
            }
          }
        }
      }
    },
    "Room": {
      "Type": "AWS::IVSChat::Room",
      "Properties": {
        "Name": "LoggingRoom",
        "LoggingConfigurationIdentifiers": [
          { "Ref": "S3LoggingConfiguration" },
          { "Ref": "CloudWatchLogsLoggingConfiguration" },
          { "Ref": "FirehoseLoggingConfiguration" }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ivschat-loggingconfiguration--examples--Logging_Configuration_Template_Examples--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  Bucket:
    Type: AWS::S3::Bucket
  LogGroup:
    Type: AWS::Logs::LogGroup
  DeliveryStreamRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          Effect: Allow
          Principal:
            Service: firehose.amazonaws.com
          Action: sts:AssumeRole
  DeliveryStream:
    Type: AWS::KinesisFirehose::DeliveryStream
    Properties:
      S3DestinationConfiguration:
        BucketARN: !GetAtt Bucket.Arn
        RoleARN: !GetAtt DeliveryStreamRole.Arn
  S3LoggingConfiguration:
    Type: AWS::IVSChat::LoggingConfiguration
    Properties:
      Name: S3
      DestinationConfiguration:
        S3:
          BucketName: !Ref Bucket
  CloudWatchLogsLoggingConfiguration:
    Type: AWS::IVSChat::LoggingConfiguration
    Properties:
      Name: CloudWatchLogs
      DestinationConfiguration:
        CloudWatchLogs:
          LogGroupName: !Ref LogGroup
  FirehoseLoggingConfiguration:
    Type: AWS::IVSChat::LoggingConfiguration
    Properties:
      Name: Firehose
      DestinationConfiguration:
        Firehose:
          DeliveryStreamName: !Ref DeliveryStream
  Room:
    Type: AWS::IVSChat::Room
    Properties:
      Name: LoggingRoom
      LoggingConfigurationIdentifiers:
        - !Ref S3LoggingConfiguration
        - !Ref CloudWatchLogsLoggingConfiguration
        - !Ref FirehoseLoggingConfiguration
```

## See also<a name="aws-resource-ivschat-loggingconfiguration--seealso"></a>
+ [Getting Started with Amazon Interactive Video Service](https://docs.aws.amazon.com/ivs/latest/userguide/getting-started.html)
+ [LoggingConfigurationSummary](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_LoggingConfigurationSummary.html) API data type
+ [DestinationConfiguration](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_DestinationConfiguration.html) API data type
+ [CloudWatchLogsDestinationConfiguration](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_CloudWatchLogsDestinationConfiguration.html) API data type
+ [FirehoseDestinationConfiguration](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_FirehoseDestinationConfiguration.html) API data type
+ [S3DestinationConfiguration](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_S3DestinationConfiguration.html) API data type
+ [CreateLoggingConfiguration](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_CreateLoggingConfiguration.html) API endpoint