# AWS::SES::Template<a name="aws-resource-ses-template"></a>

The `AWS::SES::Template` resource specifies the content of an email \(composed of a subject line, an HTML part, and a text\-only part\) for Amazon SES\. For more information, see [Template](http://docs.aws.amazon.com/ses/latest/APIReference/API_Template.html) in the *Amazon Simple Email Service API Reference*\. 

**Topics**
+ [Syntax](#aws-resource-ses-template-syntax)
+ [Properties](#aws-resource-ses-template-properties)
+ [Example](#aws-resource-ses-template-examples)
+ [See Also](#aws-resource-ses-template-seealso)

## Syntax<a name="aws-resource-ses-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-template-syntax.json"></a>

```
{
  "Type" : "AWS::SES::Template",
  "Properties" : {
    "[Template](#cfn-ses-template-template)" : [*Template*](aws-properties-ses-template-template.md)
  }
}
```

### YAML<a name="aws-resource-ses-template-syntax.yaml"></a>

```
Type: "AWS::SES::Template"
Properties:
  [Template](#cfn-ses-template-template): [*Template*](aws-properties-ses-template-template.md)
```

## Properties<a name="aws-resource-ses-template-properties"></a>

`Template`  <a name="cfn-ses-template-template"></a>
The content of the email, composed of a subject line, an HTML part, and a text\-only part\.  
 *Required*: No  
 *Type*: [Amazon SES Template Template](aws-properties-ses-template-template.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Example<a name="aws-resource-ses-template-examples"></a>

### <a name="aws-resource-ses-template-example1"></a>

#### JSON<a name="aws-resource-ses-template-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES Template Sample Template",
    "Parameters": {
        "TemplateName": {
            "Type": "String"
        },
        "SubjectPart": {
            "Type": "String"
        },
        "TextPart": {
            "Type": "String"
        },
        "HtmlPart": {
            "Type": "String"
        }
    },
    "Resources": {
        "Template": {
            "Type": "AWS::SES::Template",
            "Properties": {
                "Template": {
                    "TemplateName": {
                        "Ref": "TemplateName"
                    },
                    "SubjectPart": {
                        "Ref": "SubjectPart"
                    },
                    "TextPart": {
                        "Ref": "TextPart"
                    },
                    "HtmlPart": {
                        "Ref": "HtmlPart"
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-template-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'AWS SES Template Sample Template'
Parameters:
  TemplateName:
    Type: String
  SubjectPart:
    Type: String
  TextPart:
    Type: String
  HtmlPart:
    Type: String
Resources:
  Template:
    Type: 'AWS::SES::Template'
    Properties:
      Template:
        TemplateName: !Ref TemplateName
        SubjectPart: !Ref SubjectPart
        TextPart: !Ref TextPart
        HtmlPart: !Ref HtmlPart
```

## See Also<a name="aws-resource-ses-template-seealso"></a>
+ [Template](http://docs.aws.amazon.com/ses/latest/APIReference/API_Template.html) in the *Amazon Simple Email Service API Reference*