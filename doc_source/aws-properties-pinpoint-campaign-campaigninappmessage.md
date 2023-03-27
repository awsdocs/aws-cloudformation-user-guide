# AWS::Pinpoint::Campaign CampaignInAppMessage<a name="aws-properties-pinpoint-campaign-campaigninappmessage"></a>

Specifies the appearance of an in\-app message, including the message type, the title and body text, text and background colors, and the configurations of buttons that appear in the message\.

## Syntax<a name="aws-properties-pinpoint-campaign-campaigninappmessage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-campaigninappmessage-syntax.json"></a>

```
{
  "[Content](#cfn-pinpoint-campaign-campaigninappmessage-content)" : [ InAppMessageContent, ... ],
  "[CustomConfig](#cfn-pinpoint-campaign-campaigninappmessage-customconfig)" : Json,
  "[Layout](#cfn-pinpoint-campaign-campaigninappmessage-layout)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-campaigninappmessage-syntax.yaml"></a>

```
  [Content](#cfn-pinpoint-campaign-campaigninappmessage-content): 
    - InAppMessageContent
  [CustomConfig](#cfn-pinpoint-campaign-campaigninappmessage-customconfig): Json
  [Layout](#cfn-pinpoint-campaign-campaigninappmessage-layout): String
```

## Properties<a name="aws-properties-pinpoint-campaign-campaigninappmessage-properties"></a>

`Content`  <a name="cfn-pinpoint-campaign-campaigninappmessage-content"></a>
An array that contains configurtion information about the in\-app message for the campaign, including title and body text, text colors, background colors, image URLs, and button configurations\.  
*Required*: No  
*Type*: List of [InAppMessageContent](aws-properties-pinpoint-campaign-inappmessagecontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomConfig`  <a name="cfn-pinpoint-campaign-campaigninappmessage-customconfig"></a>
Custom data, in the form of key\-value pairs, that is included in an in\-app messaging payload\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Layout`  <a name="cfn-pinpoint-campaign-campaigninappmessage-layout"></a>
A string that describes how the in\-app message will appear\. You can specify one of the following:  
+  `BOTTOM_BANNER` – a message that appears as a banner at the bottom of the page\.
+  `TOP_BANNER` – a message that appears as a banner at the top of the page\.
+  `OVERLAYS` – a message that covers entire screen\.
+  `MOBILE_FEED` – a message that appears in a window in front of the page\.
+  `MIDDLE_BANNER` – a message that appears as a banner in the middle of the page\.
+  `CAROUSEL` – a scrollable layout of up to five unique messages\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)