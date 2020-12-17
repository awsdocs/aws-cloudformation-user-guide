# AWS::PinpointEmail::ConfigurationSet SendingOptions<a name="aws-properties-pinpointemail-configurationset-sendingoptions"></a>

Used to enable or disable email sending for messages that use this configuration set in the current AWS Region\.

## Syntax<a name="aws-properties-pinpointemail-configurationset-sendingoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationset-sendingoptions-syntax.json"></a>

```
{
  "[SendingEnabled](#cfn-pinpointemail-configurationset-sendingoptions-sendingenabled)" : Boolean
}
```

### YAML<a name="aws-properties-pinpointemail-configurationset-sendingoptions-syntax.yaml"></a>

```
  [SendingEnabled](#cfn-pinpointemail-configurationset-sendingoptions-sendingenabled): Boolean
```

## Properties<a name="aws-properties-pinpointemail-configurationset-sendingoptions-properties"></a>

`SendingEnabled`  <a name="cfn-pinpointemail-configurationset-sendingoptions-sendingenabled"></a>
If `true`, email sending is enabled for the configuration set\. If `false`, email sending is disabled for the configuration set\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)