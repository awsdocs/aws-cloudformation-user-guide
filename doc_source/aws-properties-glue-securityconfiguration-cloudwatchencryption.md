# AWS::Glue::SecurityConfiguration CloudWatchEncryption<a name="aws-properties-glue-securityconfiguration-cloudwatchencryption"></a>

Specifies how Amazon CloudWatch data should be encrypted\.

## Syntax<a name="aws-properties-glue-securityconfiguration-cloudwatchencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-securityconfiguration-cloudwatchencryption-syntax.json"></a>

```
{
  "[CloudWatchEncryptionMode](#cfn-glue-securityconfiguration-cloudwatchencryption-cloudwatchencryptionmode)" : String,
  "[KmsKeyArn](#cfn-glue-securityconfiguration-cloudwatchencryption-kmskeyarn)" : String
}
```

### YAML<a name="aws-properties-glue-securityconfiguration-cloudwatchencryption-syntax.yaml"></a>

```
  [CloudWatchEncryptionMode](#cfn-glue-securityconfiguration-cloudwatchencryption-cloudwatchencryptionmode): String
  [KmsKeyArn](#cfn-glue-securityconfiguration-cloudwatchencryption-kmskeyarn): String
```

## Properties<a name="aws-properties-glue-securityconfiguration-cloudwatchencryption-properties"></a>

`CloudWatchEncryptionMode`  <a name="cfn-glue-securityconfiguration-cloudwatchencryption-cloudwatchencryptionmode"></a>
The encryption mode to use for CloudWatch data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-glue-securityconfiguration-cloudwatchencryption-kmskeyarn"></a>
The Amazon Resource Name \(ARN\) of the KMS key to be used to encrypt the data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
