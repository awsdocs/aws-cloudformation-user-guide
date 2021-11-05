# AWS::Pinpoint::Campaign InAppMessageHeaderConfig<a name="aws-properties-pinpoint-campaign-inappmessageheaderconfig"></a>

Configuration information related to the title of the in\-app message\.

## Syntax<a name="aws-properties-pinpoint-campaign-inappmessageheaderconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-inappmessageheaderconfig-syntax.json"></a>

```
{
  "[Alignment](#cfn-pinpoint-campaign-inappmessageheaderconfig-alignment)" : String,
  "[Header](#cfn-pinpoint-campaign-inappmessageheaderconfig-header)" : String,
  "[TextColor](#cfn-pinpoint-campaign-inappmessageheaderconfig-textcolor)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-inappmessageheaderconfig-syntax.yaml"></a>

```
  [Alignment](#cfn-pinpoint-campaign-inappmessageheaderconfig-alignment): String
  [Header](#cfn-pinpoint-campaign-inappmessageheaderconfig-header): String
  [TextColor](#cfn-pinpoint-campaign-inappmessageheaderconfig-textcolor): String
```

## Properties<a name="aws-properties-pinpoint-campaign-inappmessageheaderconfig-properties"></a>

`Alignment`  <a name="cfn-pinpoint-campaign-inappmessageheaderconfig-alignment"></a>
The text alignment of the title of the message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Header`  <a name="cfn-pinpoint-campaign-inappmessageheaderconfig-header"></a>
Configuration information related to the title of an in\-app message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextColor`  <a name="cfn-pinpoint-campaign-inappmessageheaderconfig-textcolor"></a>
The color of the body text, expressed as a hex color code \(such as \#000000 for black\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)