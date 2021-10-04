# AWS::MediaLive::Channel InputLossFailoverSettings<a name="aws-properties-medialive-channel-inputlossfailoversettings"></a>

MediaLive will perform a failover if content is not detected in this input for the specified period\.

The parent of this entity is FailoverConditionSettings\.

## Syntax<a name="aws-properties-medialive-channel-inputlossfailoversettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputlossfailoversettings-syntax.json"></a>

```
{
  "[InputLossThresholdMsec](#cfn-medialive-channel-inputlossfailoversettings-inputlossthresholdmsec)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-inputlossfailoversettings-syntax.yaml"></a>

```
  [InputLossThresholdMsec](#cfn-medialive-channel-inputlossfailoversettings-inputlossthresholdmsec): Integer
```

## Properties<a name="aws-properties-medialive-channel-inputlossfailoversettings-properties"></a>

`InputLossThresholdMsec`  <a name="cfn-medialive-channel-inputlossfailoversettings-inputlossthresholdmsec"></a>
The amount of time \(in milliseconds\) that no input is detected\. After that time, an input failover will occur\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)