# AWS::SES::ReceiptRule<a name="aws-resource-ses-receiptrule"></a>

The `AWS::SES::ReceiptRule` resource specifies which actions Amazon SES should take when it receives mail on behalf of one or more email addresses or domains that you own\. For more information, see [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-ses-receiptrule-syntax)
+ [Properties](#aws-resource-ses-receiptrule-properties)
+ [Example](#aws-resource-ses-receiptrule-examples)
+ [See Also](#aws-resource-ses-receiptrule-seealso)

## Syntax<a name="aws-resource-ses-receiptrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-receiptrule-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ReceiptRule",
  "Properties" : {
    "[After](#cfn-ses-receiptrule-after)" : String,
    "[Rule](#cfn-ses-receiptrule-rule)" : [*Rule*](aws-properties-ses-receiptrule-rule.md),
    "[RuleSetName](#cfn-ses-receiptrule-rulesetname)" : String
  }
}
```

### YAML<a name="aws-resource-ses-receiptrule-syntax.yaml"></a>

```
Type: "AWS::SES::ReceiptRule"
Properties:
  [After](#cfn-ses-receiptrule-after): String
  [Rule](#cfn-ses-receiptrule-rule): [*Rule*](aws-properties-ses-receiptrule-rule.md)
  [RuleSetName](#cfn-ses-receiptrule-rulesetname): String
```

## Properties<a name="aws-resource-ses-receiptrule-properties"></a>

`After`  <a name="cfn-ses-receiptrule-after"></a>
The name of an existing rule after which the new rule will be placed\. If this parameter is null, the new rule will be inserted at the beginning of the rule list\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Rule`  <a name="cfn-ses-receiptrule-rule"></a>
The specified rule's name, actions, recipients, domains, enabled status, scan status, and TLS policy\.  
 *Required*: Yes  
 *Type*: [Amazon SES ReceiptRule Rule](aws-properties-ses-receiptrule-rule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RuleSetName`  <a name="cfn-ses-receiptrule-rulesetname"></a>
The name of the rule set that the receipt rule will be added to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Example<a name="aws-resource-ses-receiptrule-examples"></a>

### <a name="aws-resource-ses-receiptrule-example1"></a>

#### JSON<a name="aws-resource-ses-receiptrule-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES ReceiptRule Sample Template",
    "Parameters": {
        "RuleSetName": {
            "Type": "String"
        },
        "ReceiptRuleName1": {
            "Type": "String"
        },
        "ReceiptRuleName2": {
            "Type": "String"
        },
        "TlsPolicy": {
            "Type": "String"
        },
        "HeaderName": {
            "Type": "String"
        },
        "HeaderValue": {
            "Type": "String"
        }
    },
    "Resources": {
        "ReceiptRule1": {
            "Type": "AWS::SES::ReceiptRule",
            "Properties": {
                "RuleSetName": {
                    "Ref": "RuleSetName"
                },
                "Rule": {
                    "Name": {
                        "Ref": "ReceiptRuleName1"
                    },
                    "Enabled": true,
                    "ScanEnabled": true,
                    "TlsPolicy": {
                        "Ref": "TlsPolicy"
                    },
                    "Actions": [
                        {
                            "AddHeaderAction": {
                                "HeaderName": {
                                    "Ref": "HeaderName"
                                },
                                "HeaderValue": {
                                    "Ref": "HeaderValue"
                                }
                            }
                        }
                    ]
                }
            }
        },
        "ReceiptRule2": {
            "Type": "AWS::SES::ReceiptRule",
            "Properties": {
                "RuleSetName": {
                    "Ref": "RuleSetName"
                },
                "After": {
                    "Ref": "ReceiptRule1"
                },
                "Rule": {
                    "Name": {
                        "Ref": "ReceiptRuleName2"
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-receiptrule-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'AWS SES ReceiptRule Sample Template'
Parameters:
  RuleSetName:
    Type: String
  ReceiptRuleName1:
    Type: String
  ReceiptRuleName2:
    Type: String
  TlsPolicy:
    Type: String
  HeaderName:
    Type: String
  HeaderValue:
    Type: String

Resources:
  ReceiptRule1:
    Type: "AWS::SES::ReceiptRule"
    Properties:
      RuleSetName: !Ref RuleSetName
      Rule:
        Name: !Ref ReceiptRuleName1
        Enabled: true
        ScanEnabled: true
        TlsPolicy: !Ref TlsPolicy
        Actions:
          - AddHeaderAction:
              HeaderName: !Ref HeaderName
              HeaderValue: !Ref HeaderValue

  ReceiptRule2:
    Type: "AWS::SES::ReceiptRule"
    Properties:
      RuleSetName: !Ref RuleSetName
      After: !Ref ReceiptRule1
      Rule:
        Name: !Ref ReceiptRuleName2
```

## See Also<a name="aws-resource-ses-receiptrule-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [CreateReceiptRule](url-ses-api;API_CreateReceiptRule.html) in the *Amazon Simple Email Service API Reference*
+ [ReceiptRule](url-ses-api;API_ReceiptRule.html) in the *Amazon Simple Email Service API Reference*