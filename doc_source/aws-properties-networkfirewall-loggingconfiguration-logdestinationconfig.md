# AWS::NetworkFirewall::LoggingConfiguration LogDestinationConfig<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfig"></a>

Defines where AWS Network Firewall sends logs for the firewall for one log type\. This is used in [AWS::NetworkFirewall::LoggingConfiguration](aws-resource-networkfirewall-loggingconfiguration.md)\. You can send each type of log to an Amazon S3 bucket, a CloudWatch log group, or a Kinesis Data Firehose delivery stream\.

Network Firewall generates logs for stateful rule groups\. You can save alert and flow log types\. The stateful rules engine records flow logs for all network traffic that it receives\. It records alert logs for traffic that matches stateful rules that have the rule action set to `DROP` or `ALERT`\. 

## Syntax<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfig-syntax.json"></a>

```
{
  "[LogDestination](#cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logdestination)" : {Key : Value, ...},
  "[LogDestinationType](#cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logdestinationtype)" : String,
  "[LogType](#cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logtype)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfig-syntax.yaml"></a>

```
  [LogDestination](#cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logdestination): 
    Key : Value
  [LogDestinationType](#cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logdestinationtype): String
  [LogType](#cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logtype): String
```

## Properties<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfig-properties"></a>

`LogDestination`  <a name="cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logdestination"></a>
The named location for the logs, provided in a key:value mapping that is specific to the chosen destination type\.   
+ For an Amazon S3 bucket, provide the name of the bucket, with key `bucketName`, and optionally provide a prefix, with key `prefix`\. The following example specifies an Amazon S3 bucket named `DOC-EXAMPLE-BUCKET` and the prefix `alerts`: 

   `"LogDestination": { "bucketName": "DOC-EXAMPLE-BUCKET", "prefix": "alerts" }` 
+ For a CloudWatch log group, provide the name of the CloudWatch log group, with key `logGroup`\. The following example specifies a log group named `alert-log-group`: 

   `"LogDestination": { "logGroup": "alert-log-group" }` 
+ For a Kinesis Data Firehose delivery stream, provide the name of the delivery stream, with key `deliveryStream`\. The following example specifies a delivery stream named `alert-delivery-stream`: 

   `"LogDestination": { "deliveryStream": "alert-delivery-stream" }` 
*Required*: Yes  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogDestinationType`  <a name="cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logdestinationtype"></a>
The type of storage destination to send these logs to\. You can send logs to an Amazon S3 bucket, a CloudWatch log group, or a Kinesis Data Firehose delivery stream\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CloudWatchLogs | KinesisDataFirehose | S3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogType`  <a name="cfn-networkfirewall-loggingconfiguration-logdestinationconfig-logtype"></a>
The type of log to send\. Alert logs report traffic that matches a stateful rule with an action setting that sends an alert log message\. Flow logs are standard network traffic flow logs\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALERT | FLOW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)