# AWS::Pinpoint::Campaign InAppMessageContent<a name="aws-properties-pinpoint-campaign-inappmessagecontent"></a>

Specifies the configuration and contents of an in\-app message\.

## Syntax<a name="aws-properties-pinpoint-campaign-inappmessagecontent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-inappmessagecontent-syntax.json"></a>

```
{
  "[BackgroundColor](#cfn-pinpoint-campaign-inappmessagecontent-backgroundcolor)" : String,
  "[BodyConfig](#cfn-pinpoint-campaign-inappmessagecontent-bodyconfig)" : InAppMessageBodyConfig,
  "[HeaderConfig](#cfn-pinpoint-campaign-inappmessagecontent-headerconfig)" : InAppMessageHeaderConfig,
  "[ImageUrl](#cfn-pinpoint-campaign-inappmessagecontent-imageurl)" : String,
  "[PrimaryBtn](#cfn-pinpoint-campaign-inappmessagecontent-primarybtn)" : InAppMessageButton,
  "[SecondaryBtn](#cfn-pinpoint-campaign-inappmessagecontent-secondarybtn)" : InAppMessageButton
}
```

### YAML<a name="aws-properties-pinpoint-campaign-inappmessagecontent-syntax.yaml"></a>

```
  [BackgroundColor](#cfn-pinpoint-campaign-inappmessagecontent-backgroundcolor): String
  [BodyConfig](#cfn-pinpoint-campaign-inappmessagecontent-bodyconfig): 
    InAppMessageBodyConfig
  [HeaderConfig](#cfn-pinpoint-campaign-inappmessagecontent-headerconfig): 
    InAppMessageHeaderConfig
  [ImageUrl](#cfn-pinpoint-campaign-inappmessagecontent-imageurl): String
  [PrimaryBtn](#cfn-pinpoint-campaign-inappmessagecontent-primarybtn): 
    InAppMessageButton
  [SecondaryBtn](#cfn-pinpoint-campaign-inappmessagecontent-secondarybtn): 
    InAppMessageButton
```

## Properties<a name="aws-properties-pinpoint-campaign-inappmessagecontent-properties"></a>

`BackgroundColor`  <a name="cfn-pinpoint-campaign-inappmessagecontent-backgroundcolor"></a>
The background color for an in\-app message banner, expressed as a hex color code \(such as \#000000 for black\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BodyConfig`  <a name="cfn-pinpoint-campaign-inappmessagecontent-bodyconfig"></a>
Specifies the configuration of main body text in an in\-app message template\.  
*Required*: No  
*Type*: [InAppMessageBodyConfig](aws-properties-pinpoint-campaign-inappmessagebodyconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderConfig`  <a name="cfn-pinpoint-campaign-inappmessagecontent-headerconfig"></a>
Specifies the configuration and content of the header or title text of the in\-app message\.  
*Required*: No  
*Type*: [InAppMessageHeaderConfig](aws-properties-pinpoint-campaign-inappmessageheaderconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageUrl`  <a name="cfn-pinpoint-campaign-inappmessagecontent-imageurl"></a>
The URL of the image that appears on an in\-app message banner\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryBtn`  <a name="cfn-pinpoint-campaign-inappmessagecontent-primarybtn"></a>
An object that contains configuration information about the primary button in an in\-app message\.  
*Required*: No  
*Type*: [InAppMessageButton](aws-properties-pinpoint-campaign-inappmessagebutton.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryBtn`  <a name="cfn-pinpoint-campaign-inappmessagecontent-secondarybtn"></a>
An object that contains configuration information about the secondary button in an in\-app message\.  
*Required*: No  
*Type*: [InAppMessageButton](aws-properties-pinpoint-campaign-inappmessagebutton.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)