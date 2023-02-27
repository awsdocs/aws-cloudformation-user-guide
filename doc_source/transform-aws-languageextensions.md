# AWS::LanguageExtensions transform<a name="transform-aws-languageextensions"></a>

The `AWS::LanguageExtensions` transform is a macro hosted by AWS CloudFormation that lets you use intrinsic functions and other functionalities not included by default in AWS CloudFormation\. When a template references `AWS::LanguageExtensions`, and you're creating or updating stacks using change sets, AWS CloudFormation updates any intrinsic function defined by the transform to its resolved value within the template\. 

The `AWS::LanguageExtensions` transform supports the following functions and attributes:
+ [`Fn::Length`](intrinsic-function-reference-length.md)
+ [`Fn::ToJsonString`](intrinsic-function-reference-ToJsonString.md)
+ [Intrinsic function references in DeletionPolicy and UpdateReplacePolicy attributes](function-refs-in-policy-attributes.md)
+ [`Fn::FindInMap enhancements`](intrinsic-function-reference-findinmap-enhancements.md)

## Usage<a name="transform-aws-languageextensions-usage"></a>

The value for the transform declaration must be a literal string\. You can't use a parameter or function to specify a transform value\. See this snippet for an example of a transform declaration:

### Syntax at the top level of a template<a name="transform-aws-languageextensions-usage-subsection"></a>

Use the `AWS::LanguageExtensions` transform at the top level of a template\. You can't use the `AWS::LanguageExtensions` transform as an embedded transform in any other template section\.

### JSON<a name="transform-aws-languageextensions-usage.json"></a>

```
"Transform": "AWS::LanguageExtensions"
```

### YAML<a name="transform-aws-languageextensions-usage.yaml"></a>

```
Transform: AWS::LanguageExtensions
```

## Parameters<a name="transform-aws-languageextensions-parameters"></a>

The `AWS::LanguageExtensions` transform doesn't accept parameters\.

## Remarks<a name="transform-aws-languageextensions-remarks"></a>

When using the `AWS::LanguageExtensions` transform, keep the following considerations in mind:
+ If you update a stack using a different parameter value, don't use the `--use-previous-template` option where the original template contains the transform\. Use the original template, before transformation, in the `UpdateStack` call\. The stack will update with the new parameter values\.
+ Short\-form YAML syntax isn't supported within a template for intrinsic functions provided by the `AWS::LanguageExtensions` transform\. Use explicit references to functions\. For example, use `Fn::Length` instead of `!Length`\.
+ If you're using multiple transforms, use a list format\. If you're using custom macros, place AWS\-provided transforms after your custom macros\. If you're using both the `AWS::LanguageExtensions` and `AWS::Serverless` transforms, the `AWS::LanguageExtensions` transform must come before the `AWS::Serverless` transform in the list\.
+ Functions and attributes provided by the `AWS::LanguageExtensions` transform are only supported in the `Resources`, `Conditions`, and `Outputs` sections of a template\.

For more information on using macros, see [Creating an AWS CloudFormation macro definition](template-macros.md#template-macros-author)\.

## Example<a name="transform-aws-languageextensions-example"></a>

The following example shows how to use the `AWS::LanguageExtensions` transform to use the `Fn::Length` intrinsic function, defined by the transform\.

### JSON<a name="transform-aws-languageextensions-example.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Transform": "AWS::LanguageExtensions",
    "Parameters": {
        "QueueList": {
            "Type": "CommaDelimitedList"
        },
        "QueueNameParam": {
            "Description": "Name for your SQS queue",
            "Type": "String"
        }
    },
    "Resources": {
        "Queue": {
            "Type": "AWS::SQS::Queue",
            "Properties": {
                "QueueName": {
                    "Ref": "QueueNameParam"
                },
                "DelaySeconds": {
                    "Fn::Length": {
                        "Ref": "QueueList"
                    }
                }
            }
        }
    }
}
```

### YAML<a name="transform-aws-languageextensions-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Parameters:
  QueueList:
    Type: CommaDelimitedList
  QueueNameParam:
    Description: Name for your SQS queue
    Type: String
Resources:
  Queue:
    Type: 'AWS::SQS::Queue'
    Properties:
      QueueName: !Ref QueueNameParam
      DelaySeconds:
        'Fn::Length': !Ref QueueList
```