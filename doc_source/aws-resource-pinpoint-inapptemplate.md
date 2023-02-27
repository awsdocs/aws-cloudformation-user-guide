# AWS::Pinpoint::InAppTemplate<a name="aws-resource-pinpoint-inapptemplate"></a>

Creates a message template that you can use to send in\-app messages\. A message template is a set of content and settings that you can define, save, and reuse in messages for any of your Amazon Pinpoint applications\.

## Syntax<a name="aws-resource-pinpoint-inapptemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-inapptemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::InAppTemplate",
  "Properties" : {
      "[Content](#cfn-pinpoint-inapptemplate-content)" : [ InAppMessageContent, ... ],
      "[CustomConfig](#cfn-pinpoint-inapptemplate-customconfig)" : Json,
      "[Layout](#cfn-pinpoint-inapptemplate-layout)" : String,
      "[Tags](#cfn-pinpoint-inapptemplate-tags)" : Json,
      "[TemplateDescription](#cfn-pinpoint-inapptemplate-templatedescription)" : String,
      "[TemplateName](#cfn-pinpoint-inapptemplate-templatename)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-inapptemplate-syntax.yaml"></a>

```
Type: AWS::Pinpoint::InAppTemplate
Properties: 
  [Content](#cfn-pinpoint-inapptemplate-content): 
    - InAppMessageContent
  [CustomConfig](#cfn-pinpoint-inapptemplate-customconfig): Json
  [Layout](#cfn-pinpoint-inapptemplate-layout): String
  [Tags](#cfn-pinpoint-inapptemplate-tags): Json
  [TemplateDescription](#cfn-pinpoint-inapptemplate-templatedescription): String
  [TemplateName](#cfn-pinpoint-inapptemplate-templatename): String
```

## Properties<a name="aws-resource-pinpoint-inapptemplate-properties"></a>

`Content`  <a name="cfn-pinpoint-inapptemplate-content"></a>
An object that contains information about the content of an in\-app message, including its title and body text, text colors, background colors, images, buttons, and behaviors\.  
*Required*: No  
*Type*: List of [InAppMessageContent](aws-properties-pinpoint-inapptemplate-inappmessagecontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomConfig`  <a name="cfn-pinpoint-inapptemplate-customconfig"></a>
Custom data, in the form of key\-value pairs, that is included in an in\-app messaging payload\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Layout`  <a name="cfn-pinpoint-inapptemplate-layout"></a>
A string that determines the appearance of the in\-app message\. You can specify one of the following:  
+  `BOTTOM_BANNER` – a message that appears as a banner at the bottom of the page\.
+  `TOP_BANNER` – a message that appears as a banner at the top of the page\.
+  `OVERLAYS` – a message that covers entire screen\.
+  `MOBILE_FEED` – a message that appears in a window in front of the page\.
+  `MIDDLE_BANNER` – a message that appears as a banner in the middle of the page\.
+  `CAROUSEL` – a scrollable layout of up to five unique messages\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-pinpoint-inapptemplate-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateDescription`  <a name="cfn-pinpoint-inapptemplate-templatedescription"></a>
An optional description of the in\-app template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-pinpoint-inapptemplate-templatename"></a>
The name of the in\-app message template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-pinpoint-inapptemplate-return-values"></a>

### Fn::GetAtt<a name="aws-resource-pinpoint-inapptemplate-return-values-fn--getatt"></a>

#### <a name="aws-resource-pinpoint-inapptemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the message template\.