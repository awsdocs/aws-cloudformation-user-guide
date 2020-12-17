# AWS::Pinpoint::EmailTemplate<a name="aws-resource-pinpoint-emailtemplate"></a>

The AWS::Pinpoint::EmailTemplate resource is a message template that you can use in messages that are sent through the email channel\. A *message template* is a set of content and settings that you can define, save, and reuse in messages for one or more Amazon Pinpoint applications\.

## Syntax<a name="aws-resource-pinpoint-emailtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-emailtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::EmailTemplate",
  "Properties" : {
      "[DefaultSubstitutions](#cfn-pinpoint-emailtemplate-defaultsubstitutions)" : String,
      "[HtmlPart](#cfn-pinpoint-emailtemplate-htmlpart)" : String,
      "[Subject](#cfn-pinpoint-emailtemplate-subject)" : String,
      "[Tags](#cfn-pinpoint-emailtemplate-tags)" : Json,
      "[TemplateDescription](#cfn-pinpoint-emailtemplate-templatedescription)" : String,
      "[TemplateName](#cfn-pinpoint-emailtemplate-templatename)" : String,
      "[TextPart](#cfn-pinpoint-emailtemplate-textpart)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-emailtemplate-syntax.yaml"></a>

```
Type: AWS::Pinpoint::EmailTemplate
Properties: 
  [DefaultSubstitutions](#cfn-pinpoint-emailtemplate-defaultsubstitutions): String
  [HtmlPart](#cfn-pinpoint-emailtemplate-htmlpart): String
  [Subject](#cfn-pinpoint-emailtemplate-subject): String
  [Tags](#cfn-pinpoint-emailtemplate-tags): Json
  [TemplateDescription](#cfn-pinpoint-emailtemplate-templatedescription): String
  [TemplateName](#cfn-pinpoint-emailtemplate-templatename): String
  [TextPart](#cfn-pinpoint-emailtemplate-textpart): String
```

## Properties<a name="aws-resource-pinpoint-emailtemplate-properties"></a>

`DefaultSubstitutions`  <a name="cfn-pinpoint-emailtemplate-defaultsubstitutions"></a>
A JSON object that specifies the default values to use for message variables in the message template\. This object is a set of key\-value pairs\. Each key defines a message variable in the template\. The corresponding value defines the default value for that variable\. When you create a message that's based on the template, you can override these defaults with message\-specific and address\-specific variables and values\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HtmlPart`  <a name="cfn-pinpoint-emailtemplate-htmlpart"></a>
The message body, in HTML format, to use in email messages that are based on the message template\. We recommend using HTML format for email clients that render HTML content\. You can include links, formatted text, and more in an HTML message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subject`  <a name="cfn-pinpoint-emailtemplate-subject"></a>
The subject line, or title, to use in email messages that are based on the message template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-pinpoint-emailtemplate-tags"></a>
A string\-to\-string map of key\-value pairs that defines the tags to associate with the message template\. Each tag consists of a required tag key and an associated tag value\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateDescription`  <a name="cfn-pinpoint-emailtemplate-templatedescription"></a>
A custom description of the message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-pinpoint-emailtemplate-templatename"></a>
The name of the message template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TextPart`  <a name="cfn-pinpoint-emailtemplate-textpart"></a>
The message body, in plain text format, to use in email messages that are based on the message template\. We recommend using plain text format for email clients that don't render HTML content and clients that are connected to high\-latency networks, such as mobile devices\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-emailtemplate-return-values"></a>

### Ref<a name="aws-resource-pinpoint-emailtemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the message template \(`TemplateName`\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpoint-emailtemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pinpoint-emailtemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the message template\.