# AWS::IVSChat::LoggingConfiguration S3DestinationConfiguration<a name="aws-properties-ivschat-loggingconfiguration-s3destinationconfiguration"></a>

The S3DestinationConfiguration property type specifies an S3 location where chat logs will be stored\.

## Syntax<a name="aws-properties-ivschat-loggingconfiguration-s3destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivschat-loggingconfiguration-s3destinationconfiguration-syntax.json"></a>

```
{
  "[BucketName](#cfn-ivschat-loggingconfiguration-s3destinationconfiguration-bucketname)" : String
}
```

### YAML<a name="aws-properties-ivschat-loggingconfiguration-s3destinationconfiguration-syntax.yaml"></a>

```
  [BucketName](#cfn-ivschat-loggingconfiguration-s3destinationconfiguration-bucketname): String
```

## Properties<a name="aws-properties-ivschat-loggingconfiguration-s3destinationconfiguration-properties"></a>

`BucketName`  <a name="cfn-ivschat-loggingconfiguration-s3destinationconfiguration-bucketname"></a>
Name of the Amazon S3 bucket where chat activity will be logged\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `^[a-z0-9-.]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)