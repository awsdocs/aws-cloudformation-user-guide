# AWS::SSMContacts::Contact ChannelTargetInfo<a name="aws-properties-ssmcontacts-contact-channeltargetinfo"></a>

Information about the contact channel that Incident Manager uses to engage the contact\.

## Syntax<a name="aws-properties-ssmcontacts-contact-channeltargetinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmcontacts-contact-channeltargetinfo-syntax.json"></a>

```
{
  "[ChannelId](#cfn-ssmcontacts-contact-channeltargetinfo-channelid)" : String,
  "[RetryIntervalInMinutes](#cfn-ssmcontacts-contact-channeltargetinfo-retryintervalinminutes)" : Integer
}
```

### YAML<a name="aws-properties-ssmcontacts-contact-channeltargetinfo-syntax.yaml"></a>

```
  [ChannelId](#cfn-ssmcontacts-contact-channeltargetinfo-channelid): String
  [RetryIntervalInMinutes](#cfn-ssmcontacts-contact-channeltargetinfo-retryintervalinminutes): Integer
```

## Properties<a name="aws-properties-ssmcontacts-contact-channeltargetinfo-properties"></a>

`ChannelId`  <a name="cfn-ssmcontacts-contact-channeltargetinfo-channelid"></a>
The Amazon Resource Name \(ARN\) of the contact channel\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:(aws|aws-cn|aws-us-gov):ssm-contacts:[-\w+=\/,.@]*:[0-9]+:([\w+=\/,.@:-]+)*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryIntervalInMinutes`  <a name="cfn-ssmcontacts-contact-channeltargetinfo-retryintervalinminutes"></a>
The number of minutes to wait to retry sending engagement in the case the engagement initially fails\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `60`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)