# AWS::MediaPackage::Channel LogConfiguration<a name="aws-properties-mediapackage-channel-logconfiguration"></a>

The access log configuration parameters for your channel\.

## Syntax<a name="aws-properties-mediapackage-channel-logconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-channel-logconfiguration-syntax.json"></a>

```
{
  "[LogGroupName](#cfn-mediapackage-channel-logconfiguration-loggroupname)" : String
}
```

### YAML<a name="aws-properties-mediapackage-channel-logconfiguration-syntax.yaml"></a>

```
  [LogGroupName](#cfn-mediapackage-channel-logconfiguration-loggroupname): String
```

## Properties<a name="aws-properties-mediapackage-channel-logconfiguration-properties"></a>

`LogGroupName`  <a name="cfn-mediapackage-channel-logconfiguration-loggroupname"></a>
Sets a custom Amazon CloudWatch log group name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)