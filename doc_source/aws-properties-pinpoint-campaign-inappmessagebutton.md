# AWS::Pinpoint::Campaign InAppMessageButton<a name="aws-properties-pinpoint-campaign-inappmessagebutton"></a>

Specifies the configuration of a button that appears in an in\-app message\.

## Syntax<a name="aws-properties-pinpoint-campaign-inappmessagebutton-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-inappmessagebutton-syntax.json"></a>

```
{
  "[Android](#cfn-pinpoint-campaign-inappmessagebutton-android)" : OverrideButtonConfiguration,
  "[DefaultConfig](#cfn-pinpoint-campaign-inappmessagebutton-defaultconfig)" : DefaultButtonConfiguration,
  "[IOS](#cfn-pinpoint-campaign-inappmessagebutton-ios)" : OverrideButtonConfiguration,
  "[Web](#cfn-pinpoint-campaign-inappmessagebutton-web)" : OverrideButtonConfiguration
}
```

### YAML<a name="aws-properties-pinpoint-campaign-inappmessagebutton-syntax.yaml"></a>

```
  [Android](#cfn-pinpoint-campaign-inappmessagebutton-android): 
    OverrideButtonConfiguration
  [DefaultConfig](#cfn-pinpoint-campaign-inappmessagebutton-defaultconfig): 
    DefaultButtonConfiguration
  [IOS](#cfn-pinpoint-campaign-inappmessagebutton-ios): 
    OverrideButtonConfiguration
  [Web](#cfn-pinpoint-campaign-inappmessagebutton-web): 
    OverrideButtonConfiguration
```

## Properties<a name="aws-properties-pinpoint-campaign-inappmessagebutton-properties"></a>

`Android`  <a name="cfn-pinpoint-campaign-inappmessagebutton-android"></a>
An object that defines the default behavior for a button in in\-app messages sent to Android\.  
*Required*: No  
*Type*: [OverrideButtonConfiguration](aws-properties-pinpoint-campaign-overridebuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultConfig`  <a name="cfn-pinpoint-campaign-inappmessagebutton-defaultconfig"></a>
An object that defines the default behavior for a button in an in\-app message\.  
*Required*: No  
*Type*: [DefaultButtonConfiguration](aws-properties-pinpoint-campaign-defaultbuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IOS`  <a name="cfn-pinpoint-campaign-inappmessagebutton-ios"></a>
An object that defines the default behavior for a button in in\-app messages sent to iOS devices\.  
*Required*: No  
*Type*: [OverrideButtonConfiguration](aws-properties-pinpoint-campaign-overridebuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Web`  <a name="cfn-pinpoint-campaign-inappmessagebutton-web"></a>
An object that defines the default behavior for a button in in\-app messages for web applications\.  
*Required*: No  
*Type*: [OverrideButtonConfiguration](aws-properties-pinpoint-campaign-overridebuttonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)