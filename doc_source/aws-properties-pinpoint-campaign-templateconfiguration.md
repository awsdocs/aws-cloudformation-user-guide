# AWS::Pinpoint::Campaign TemplateConfiguration<a name="aws-properties-pinpoint-campaign-templateconfiguration"></a>

Specifies the message template to use for the message, for each type of channel\.

## Syntax<a name="aws-properties-pinpoint-campaign-templateconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-templateconfiguration-syntax.json"></a>

```
{
  "[EmailTemplate](#cfn-pinpoint-campaign-templateconfiguration-emailtemplate)" : Template,
  "[PushTemplate](#cfn-pinpoint-campaign-templateconfiguration-pushtemplate)" : Template,
  "[SMSTemplate](#cfn-pinpoint-campaign-templateconfiguration-smstemplate)" : Template,
  "[VoiceTemplate](#cfn-pinpoint-campaign-templateconfiguration-voicetemplate)" : Template
}
```

### YAML<a name="aws-properties-pinpoint-campaign-templateconfiguration-syntax.yaml"></a>

```
  [EmailTemplate](#cfn-pinpoint-campaign-templateconfiguration-emailtemplate): 
    Template
  [PushTemplate](#cfn-pinpoint-campaign-templateconfiguration-pushtemplate): 
    Template
  [SMSTemplate](#cfn-pinpoint-campaign-templateconfiguration-smstemplate): 
    Template
  [VoiceTemplate](#cfn-pinpoint-campaign-templateconfiguration-voicetemplate): 
    Template
```

## Properties<a name="aws-properties-pinpoint-campaign-templateconfiguration-properties"></a>

`EmailTemplate`  <a name="cfn-pinpoint-campaign-templateconfiguration-emailtemplate"></a>
The email template to use for the message\.  
*Required*: No  
*Type*: [Template](aws-properties-pinpoint-campaign-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PushTemplate`  <a name="cfn-pinpoint-campaign-templateconfiguration-pushtemplate"></a>
The push notification template to use for the message\.  
*Required*: No  
*Type*: [Template](aws-properties-pinpoint-campaign-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SMSTemplate`  <a name="cfn-pinpoint-campaign-templateconfiguration-smstemplate"></a>
The SMS template to use for the message\.  
*Required*: No  
*Type*: [Template](aws-properties-pinpoint-campaign-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VoiceTemplate`  <a name="cfn-pinpoint-campaign-templateconfiguration-voicetemplate"></a>
The voice template to use for the message\. This object isn't supported for campaigns\.  
*Required*: No  
*Type*: [Template](aws-properties-pinpoint-campaign-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)