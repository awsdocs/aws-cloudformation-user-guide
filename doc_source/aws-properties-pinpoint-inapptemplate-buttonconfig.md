# AWS::Pinpoint::InAppTemplate ButtonConfig<a name="aws-properties-pinpoint-inapptemplate-buttonconfig"></a>

Specifies the behavior of buttons that appear in an in\-app message template\.

## Syntax<a name="aws-properties-pinpoint-inapptemplate-buttonconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-inapptemplate-buttonconfig-syntax.json"></a>

```
{
  "[Android](#cfn-pinpoint-inapptemplate-buttonconfig-android)" : OverrideButtonConfiguration,
  "[DefaultConfig](#cfn-pinpoint-inapptemplate-buttonconfig-defaultconfig)" : DefaultButtonConfiguration,
  "[IOS](#cfn-pinpoint-inapptemplate-buttonconfig-ios)" : OverrideButtonConfiguration,
  "[Web](#cfn-pinpoint-inapptemplate-buttonconfig-web)" : OverrideButtonConfiguration
}
```

### YAML<a name="aws-properties-pinpoint-inapptemplate-buttonconfig-syntax.yaml"></a>

```
  [Android](#cfn-pinpoint-inapptemplate-buttonconfig-android): 
    OverrideButtonConfiguration
  [DefaultConfig](#cfn-pinpoint-inapptemplate-buttonconfig-defaultconfig): 
    DefaultButtonConfiguration
  [IOS](#cfn-pinpoint-inapptemplate-buttonconfig-ios): 
    OverrideButtonConfiguration
  [Web](#cfn-pinpoint-inapptemplate-buttonconfig-web): 
    OverrideButtonConfiguration
```

## Properties<a name="aws-properties-pinpoint-inapptemplate-buttonconfig-properties"></a>

`Android`  <a name="cfn-pinpoint-inapptemplate-buttonconfig-android"></a>
Optional button configuration to use for in\-app messages sent to Android devices\. This button configuration overrides the default button configuration\.  
*Required*: No  
*Type*: [OverrideButtonConfiguration](aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultConfig`  <a name="cfn-pinpoint-inapptemplate-buttonconfig-defaultconfig"></a>
Specifies the default behavior of a button that appears in an in\-app message\. You can optionally add button configurations that specifically apply to iOS, Android, or web browser users\.  
*Required*: No  
*Type*: [DefaultButtonConfiguration](aws-properties-pinpoint-inapptemplate-defaultbuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IOS`  <a name="cfn-pinpoint-inapptemplate-buttonconfig-ios"></a>
Optional button configuration to use for in\-app messages sent to iOS devices\. This button configuration overrides the default button configuration\.  
*Required*: No  
*Type*: [OverrideButtonConfiguration](aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Web`  <a name="cfn-pinpoint-inapptemplate-buttonconfig-web"></a>
Optional button configuration to use for in\-app messages sent to web applications\. This button configuration overrides the default button configuration\.  
*Required*: No  
*Type*: [OverrideButtonConfiguration](aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)