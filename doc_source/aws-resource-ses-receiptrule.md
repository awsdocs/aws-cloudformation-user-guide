# AWS::SES::ReceiptRule<a name="aws-resource-ses-receiptrule"></a>

Specifies a receipt rule\.

For information about setting up receipt rules, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-receipt-rules.html)\.

You can execute this operation no more than once per second\.

## Syntax<a name="aws-resource-ses-receiptrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-receiptrule-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ReceiptRule",
  "Properties" : {
      "[After](#cfn-ses-receiptrule-after)" : String,
      "[Rule](#cfn-ses-receiptrule-rule)" : Rule,
      "[RuleSetName](#cfn-ses-receiptrule-rulesetname)" : String
    }
}
```

### YAML<a name="aws-resource-ses-receiptrule-syntax.yaml"></a>

```
Type: AWS::SES::ReceiptRule
Properties: 
  [After](#cfn-ses-receiptrule-after): String
  [Rule](#cfn-ses-receiptrule-rule): 
    Rule
  [RuleSetName](#cfn-ses-receiptrule-rulesetname): String
```

## Properties<a name="aws-resource-ses-receiptrule-properties"></a>

`After`  <a name="cfn-ses-receiptrule-after"></a>
The name of the existing rule that you want to place the current rule after\. If this parameter is `null`, the new rule is added as the first entry in the receipt rule set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rule`  <a name="cfn-ses-receiptrule-rule"></a>
A data structure that contains the specified rule's name, actions, recipients, domains, enabled status, scan status, and TLS policy\.  
*Required*: Yes  
*Type*: [Rule](aws-properties-ses-receiptrule-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleSetName`  <a name="cfn-ses-receiptrule-rulesetname"></a>
The name of the rule set that you want to add the receipt rule to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ses-receiptrule-return-values"></a>

### Ref<a name="aws-resource-ses-receiptrule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ses-receiptrule--examples"></a>

Specifies a receipt rule for incoming email\.

### <a name="aws-resource-ses-receiptrule--examples--"></a>



#### JSON<a name="aws-resource-ses-receiptrule--examples----json"></a>

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

#### YAML<a name="aws-resource-ses-receiptrule--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS SES ReceiptRule Sample Template
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
    Type: 'AWS::SES::ReceiptRule'
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
    Type: 'AWS::SES::ReceiptRule'
    Properties:
      RuleSetName: !Ref RuleSetName
      After: !Ref ReceiptRule1
      Rule:
        Name: !Ref ReceiptRuleName2
```