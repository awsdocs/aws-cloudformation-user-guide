# AWS::SES::Template<a name="aws-resource-ses-template"></a>

Specifies an email template\. Email templates enable you to send personalized email to one or more destinations in a single API operation\.

## Syntax<a name="aws-resource-ses-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-template-syntax.json"></a>

```
{
  "Type" : "AWS::SES::Template",
  "Properties" : {
      "[Template](#cfn-ses-template-template)" : Template
    }
}
```

### YAML<a name="aws-resource-ses-template-syntax.yaml"></a>

```
Type: AWS::SES::Template
Properties: 
  [Template](#cfn-ses-template-template): 
    Template
```

## Properties<a name="aws-resource-ses-template-properties"></a>

`Template`  <a name="cfn-ses-template-template"></a>
The content of the email, composed of a subject line and either an HTML part or a text\-only part\.  
*Required*: No  
*Type*: [Template](aws-properties-ses-template-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ses-template-return-values"></a>

### Fn::GetAtt<a name="aws-resource-ses-template-return-values-fn--getatt"></a>

#### <a name="aws-resource-ses-template-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
Property description not available\.

## Examples<a name="aws-resource-ses-template--examples"></a>

Specifies an email template, which is used when sending templated email messages\.

### <a name="aws-resource-ses-template--examples--"></a>



#### JSON<a name="aws-resource-ses-template--examples----json"></a>

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

#### YAML<a name="aws-resource-ses-template--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS SES Template Sample Template
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