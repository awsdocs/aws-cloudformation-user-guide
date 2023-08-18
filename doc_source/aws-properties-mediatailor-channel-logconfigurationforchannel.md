# AWS::MediaTailor::Channel LogConfigurationForChannel<a name="aws-properties-mediatailor-channel-logconfigurationforchannel"></a>

The log configuration for the channel\.

## Syntax<a name="aws-properties-mediatailor-channel-logconfigurationforchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-channel-logconfigurationforchannel-syntax.json"></a>

```
{
  "[LogTypes](#cfn-mediatailor-channel-logconfigurationforchannel-logtypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-mediatailor-channel-logconfigurationforchannel-syntax.yaml"></a>

```
  [LogTypes](#cfn-mediatailor-channel-logconfigurationforchannel-logtypes): 
    - String
```

## Properties<a name="aws-properties-mediatailor-channel-logconfigurationforchannel-properties"></a>

`LogTypes`  <a name="cfn-mediatailor-channel-logconfigurationforchannel-logtypes"></a>
The log types\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)