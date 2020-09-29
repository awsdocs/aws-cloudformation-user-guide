# AWS::KinesisFirehose::DeliveryStream HttpEndpointDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration"></a>

Describes the configuration of the HTTP endpoint destination\. Kinesis Firehose supports any custom HTTP endpoint or HTTP endpoints owned by supported third\-party service providers, including Datadog, MongoDB, and New Relic\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-syntax.json"></a>

```
{
  "[BufferingHints](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-bufferinghints)" : BufferingHints,
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-cloudwatchloggingoptions)" : CloudWatchLoggingOptions,
  "[EndpointConfiguration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-endpointconfiguration)" : HttpEndpointConfiguration,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-processingconfiguration)" : ProcessingConfiguration,
  "[RequestConfiguration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-requestconfiguration)" : HttpEndpointRequestConfiguration,
  "[RetryOptions](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-retryoptions)" : RetryOptions,
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-rolearn)" : String,
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-s3backupmode)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-s3configuration)" : S3DestinationConfiguration
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-syntax.yaml"></a>

```
  [BufferingHints](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-bufferinghints): 
    BufferingHints
  [CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-cloudwatchloggingoptions): 
    CloudWatchLoggingOptions
  [EndpointConfiguration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-endpointconfiguration): 
    HttpEndpointConfiguration
  [ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-processingconfiguration): 
    ProcessingConfiguration
  [RequestConfiguration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-requestconfiguration): 
    HttpEndpointRequestConfiguration
  [RetryOptions](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-retryoptions): 
    RetryOptions
  [RoleARN](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-rolearn): String
  [S3BackupMode](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-s3backupmode): String
  [S3Configuration](#cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-s3configuration): 
    S3DestinationConfiguration
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-properties"></a>

`BufferingHints`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-bufferinghints"></a>
The buffering options that can be used before data is delivered to the specified destination\. Kinesis Data Firehose treats these options as hints, and it might choose to use more optimal values\. The SizeInMBs and IntervalInSeconds parameters are optional\. However, if you specify a value for one of them, you must also provide a value for the other\.   
*Required*: No  
*Type*: [BufferingHints](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-cloudwatchloggingoptions"></a>
Describes the Amazon CloudWatch logging options for your delivery stream\.  
*Required*: No  
*Type*: [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-endpointconfiguration"></a>
The configuration of the HTTP endpoint selected as the destination\.  
*Required*: Yes  
*Type*: [HttpEndpointConfiguration](aws-properties-kinesisfirehose-deliverystream-httpendpointconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-processingconfiguration"></a>
Describes the data processing configuration\.  
*Required*: No  
*Type*: [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-requestconfiguration"></a>
 The configuration of the request sent to the HTTP endpoint specified as the destination\.   
*Required*: No  
*Type*: [HttpEndpointRequestConfiguration](aws-properties-kinesisfirehose-deliverystream-httpendpointrequestconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryOptions`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-retryoptions"></a>
Describes the retry behavior in case Kinesis Data Firehose is unable to deliver data to the specified HTTP endpoint destination, or if it doesn't receive a valid acknowledgment of receipt from the specified HTTP endpoint destination\.   
*Required*: No  
*Type*: [RetryOptions](aws-properties-kinesisfirehose-deliverystream-retryoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-rolearn"></a>
Kinesis Data Firehose uses this IAM role for all the permissions that the delivery stream needs\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-s3backupmode"></a>
Describes the S3 bucket backup options for the data that Kinesis Data Firehose delivers to the HTTP endpoint destination\. You can back up all documents \(AllData\) or only the documents that Kinesis Data Firehose could not deliver to the specified HTTP endpoint destination \(FailedDataOnly\)\.   
*Required*: No  
*Type*: String  
*Allowed values*: `AllData | FailedDataOnly`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointdestinationconfiguration-s3configuration"></a>
Describes the configuration of a destination in Amazon S3\.  
*Required*: Yes  
*Type*: [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)