# AWS::SSMContacts::Plan ChannelTargetInfo<a name="aws-properties-ssmcontacts-plan-channeltargetinfo"></a>

Information about the contact channel that Incident Manager uses to engage the contact\.

## Syntax<a name="aws-properties-ssmcontacts-plan-channeltargetinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmcontacts-plan-channeltargetinfo-syntax.json"></a>

```
{
  "[ChannelId](#cfn-ssmcontacts-plan-channeltargetinfo-channelid)" : String,
  "[RetryIntervalInMinutes](#cfn-ssmcontacts-plan-channeltargetinfo-retryintervalinminutes)" : Integer
}
```

### YAML<a name="aws-properties-ssmcontacts-plan-channeltargetinfo-syntax.yaml"></a>

```
  [ChannelId](#cfn-ssmcontacts-plan-channeltargetinfo-channelid): String
  [RetryIntervalInMinutes](#cfn-ssmcontacts-plan-channeltargetinfo-retryintervalinminutes): Integer
```

## Properties<a name="aws-properties-ssmcontacts-plan-channeltargetinfo-properties"></a>

`ChannelId`  <a name="cfn-ssmcontacts-plan-channeltargetinfo-channelid"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryIntervalInMinutes`  <a name="cfn-ssmcontacts-plan-channeltargetinfo-retryintervalinminutes"></a>
The number of minutes to wait before retrying to send engagement if the engagement initially failed\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `60`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)