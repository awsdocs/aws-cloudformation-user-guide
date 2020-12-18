# AWS::SES::ReceiptRuleSet<a name="aws-resource-ses-receiptruleset"></a>

Specifies an empty receipt rule set\.

For information about setting up receipt rule sets, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-receipt-rule-set.html)\.

You can execute this operation no more than once per second\.

## Syntax<a name="aws-resource-ses-receiptruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-receiptruleset-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ReceiptRuleSet",
  "Properties" : {
      "[RuleSetName](#cfn-ses-receiptruleset-rulesetname)" : String
    }
}
```

### YAML<a name="aws-resource-ses-receiptruleset-syntax.yaml"></a>

```
Type: AWS::SES::ReceiptRuleSet
Properties: 
  [RuleSetName](#cfn-ses-receiptruleset-rulesetname): String
```

## Properties<a name="aws-resource-ses-receiptruleset-properties"></a>

`RuleSetName`  <a name="cfn-ses-receiptruleset-rulesetname"></a>
The name of the receipt rule set that you want to reorder\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ses-receiptruleset-return-values"></a>

### Ref<a name="aws-resource-ses-receiptruleset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ses-receiptruleset--examples"></a>

Specifies a collection of receipt rules that are applied to incoming email\.

### <a name="aws-resource-ses-receiptruleset--examples--"></a>



#### JSON<a name="aws-resource-ses-receiptruleset--examples----json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES ReceiptRuleSet Sample Template",
    "Parameters": {
        "ReceiptRuleSetName": {
            "Type": "String"
        }
    },
    "Resources": {
        "ReceiptRuleSet": {
            "Type": "AWS::SES::ReceiptRuleSet",
            "Properties": {
                "RuleSetName": {
                    "Ref": "ReceiptRuleSetName"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-receiptruleset--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS SES ReceiptRuleSet Sample Template
Parameters:
  ReceiptRuleSetName:
    Type: String
Resources:
  ReceiptRuleSet:
    Type: 'AWS::SES::ReceiptRuleSet'
    Properties:
      RuleSetName: !Ref ReceiptRuleSetName
```