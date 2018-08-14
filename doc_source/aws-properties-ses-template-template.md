# Amazon Simple Email Service Template Template<a name="aws-properties-ses-template-template"></a>

<a name="aws-properties-ses-template-template-description"></a>The `Template` property type specifies specify the content of the email \(composed of a subject line, an HTML part, and a text\-only part\) for Amazon SES\.

<a name="aws-properties-ses-template-template-inheritance"></a> `Template` is a property of the [AWS::SES::Template](aws-resource-ses-template.md) resource\.

## Syntax<a name="aws-properties-ses-template-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-template-template-syntax.json"></a>

```
{
  "[HtmlPart](#cfn-ses-template-template-htmlpart)" : String,
  "[TextPart](#cfn-ses-template-template-textpart)" : String,
  "[TemplateName](#cfn-ses-template-template-templatename)" : String,
  "[SubjectPart](#cfn-ses-template-template-subjectpart)" : String
}
```

### YAML<a name="aws-properties-ses-template-template-syntax.yaml"></a>

```
[HtmlPart](#cfn-ses-template-template-htmlpart): String
[TextPart](#cfn-ses-template-template-textpart): String
[TemplateName](#cfn-ses-template-template-templatename): String
[SubjectPart](#cfn-ses-template-template-subjectpart): String
```

## Properties<a name="aws-properties-ses-template-template-properties"></a>

`HtmlPart`  <a name="cfn-ses-template-template-htmlpart"></a>
The HTML body of the email\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubjectPart`  <a name="cfn-ses-template-template-subjectpart"></a>
The subject line of the email\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TextPart`  <a name="cfn-ses-template-template-textpart"></a>
The email body that will be visible to recipients whose email clients do not display HTML\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TemplateName`  <a name="cfn-ses-template-template-templatename"></a>
The name of the template\. You will refer to this name when you send email using the `SendTemplatedEmail` or `SendBulkTemplatedEmail` operations\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-ses-template-template-seealso"></a>
+ [Template](http://docs.aws.amazon.com/ses/latest/APIReference/API_Template.html) in the *Amazon Simple Email Service API Reference*
+ [SendTemplatedEmail](http://docs.aws.amazon.com/ses/latest/APIReference/API_SendTemplatedEmail.html) in the *Amazon Simple Email Service API Reference*
+ [SendBulkTemplatedEmail](http://docs.aws.amazon.com/ses/latest/APIReference/API_SendBulkTemplatedEmail.html) in the *Amazon Simple Email Service API Reference*