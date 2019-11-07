# AWS::Pinpoint::EmailTemplate<a name="aws-resource-pinpoint-emailtemplate"></a>

Creates a message template that you can use in messages that are sent through the email channel\. A *message template* is a set of content and settings that you can define, save, and reuse in messages for any of your Amazon Pinpoint applications\.

## Syntax<a name="aws-resource-pinpoint-emailtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-emailtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::EmailTemplate",
  "Properties" : {
      "[HtmlPart](#cfn-pinpoint-emailtemplate-htmlpart)" : String,
      "[Subject](#cfn-pinpoint-emailtemplate-subject)" : String,
      "[Tags](#cfn-pinpoint-emailtemplate-tags)" : Json,
      "[TemplateName](#cfn-pinpoint-emailtemplate-templatename)" : String,
      "[TextPart](#cfn-pinpoint-emailtemplate-textpart)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-emailtemplate-syntax.yaml"></a>

```
Type: AWS::Pinpoint::EmailTemplate
Properties: 
  [HtmlPart](#cfn-pinpoint-emailtemplate-htmlpart): String
  [Subject](#cfn-pinpoint-emailtemplate-subject): String
  [Tags](#cfn-pinpoint-emailtemplate-tags): Json
  [TemplateName](#cfn-pinpoint-emailtemplate-templatename): String
  [TextPart](#cfn-pinpoint-emailtemplate-textpart): String
```

## Properties<a name="aws-resource-pinpoint-emailtemplate-properties"></a>

`HtmlPart`  <a name="cfn-pinpoint-emailtemplate-htmlpart"></a>
The message body, in HTML format, to use in email messages that are based on the message template\. We recommend using HTML format for email clients that support HTML\. You can include links, formatted text, and more in an HTML message\.  
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

`TemplateName`  <a name="cfn-pinpoint-emailtemplate-templatename"></a>
The name of the message template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TextPart`  <a name="cfn-pinpoint-emailtemplate-textpart"></a>
The message body, in text format, to use in email messages that are based on the message template\. We recommend using text format for email clients that don't support HTML and clients that are connected to high\-latency networks, such as mobile devices\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-pinpoint-emailtemplate-return-values"></a>

### Ref<a name="aws-resource-pinpoint-emailtemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the message template \(`TemplateName`\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpoint-emailtemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pinpoint-emailtemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the message template\.