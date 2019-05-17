# AWS::SES::Template Template<a name="aws-properties-ses-template-template"></a>

The content of the email, composed of a subject line, an HTML part, and a text\-only part\.

## Syntax<a name="aws-properties-ses-template-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-template-template-syntax.json"></a>

```
{
  "[HtmlPart](#cfn-ses-template-template-htmlpart)" : String,
  "[SubjectPart](#cfn-ses-template-template-subjectpart)" : String,
  "[TemplateName](#cfn-ses-template-template-templatename)" : String,
  "[TextPart](#cfn-ses-template-template-textpart)" : String
}
```

### YAML<a name="aws-properties-ses-template-template-syntax.yaml"></a>

```
  [HtmlPart](#cfn-ses-template-template-htmlpart): String
  [SubjectPart](#cfn-ses-template-template-subjectpart): String
  [TemplateName](#cfn-ses-template-template-templatename): String
  [TextPart](#cfn-ses-template-template-textpart): String
```

## Properties<a name="aws-properties-ses-template-template-properties"></a>

`HtmlPart`  <a name="cfn-ses-template-template-htmlpart"></a>
The HTML body of the email\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubjectPart`  <a name="cfn-ses-template-template-subjectpart"></a>
The subject line of the email\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-ses-template-template-templatename"></a>
The name of the template\. You specify this name when you send email using the `SendTemplatedEmail` or `SendBulkTemplatedEmail` operations\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TextPart`  <a name="cfn-ses-template-template-textpart"></a>
The email body that is visible to recipients whose email clients don't display HTML content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)