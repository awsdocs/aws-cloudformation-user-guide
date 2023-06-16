# AWS::Pinpoint::Campaign Template<a name="aws-properties-pinpoint-campaign-template"></a>

Specifies the name and version of the message template to use for the message\.

## Syntax<a name="aws-properties-pinpoint-campaign-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-template-syntax.json"></a>

```
{
  "[Name](#cfn-pinpoint-campaign-template-name)" : String,
  "[Version](#cfn-pinpoint-campaign-template-version)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-template-syntax.yaml"></a>

```
  [Name](#cfn-pinpoint-campaign-template-name): String
  [Version](#cfn-pinpoint-campaign-template-version): String
```

## Properties<a name="aws-properties-pinpoint-campaign-template-properties"></a>

`Name`  <a name="cfn-pinpoint-campaign-template-name"></a>
The name of the message template to use for the message\. If specified, this value must match the name of an existing message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-pinpoint-campaign-template-version"></a>
The unique identifier for the version of the message template to use for the message\. If specified, this value must match the identifier for an existing template version\. To retrieve a list of versions and version identifiers for a template, use the [Template Versions](https://docs.aws.amazon.com/pinpoint/latest/apireference/templates-template-name-template-type-versions.html) resource\.  
If you don't specify a value for this property, Amazon Pinpoint uses the *active version* of the template\. The *active version* is typically the version of a template that's been most recently reviewed and approved for use, depending on your workflow\. It isn't necessarily the latest version of a template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)