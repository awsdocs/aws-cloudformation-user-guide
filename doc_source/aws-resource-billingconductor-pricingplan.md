# AWS::BillingConductor::PricingPlan<a name="aws-resource-billingconductor-pricingplan"></a>

Creates a pricing plan that is used for computing AWS charges for billing groups\. 

## Syntax<a name="aws-resource-billingconductor-pricingplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-billingconductor-pricingplan-syntax.json"></a>

```
{
  "Type" : "AWS::BillingConductor::PricingPlan",
  "Properties" : {
      "[Description](#cfn-billingconductor-pricingplan-description)" : String,
      "[Name](#cfn-billingconductor-pricingplan-name)" : String,
      "[PricingRuleArns](#cfn-billingconductor-pricingplan-pricingrulearns)" : [ String, ... ],
      "[Tags](#cfn-billingconductor-pricingplan-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-billingconductor-pricingplan-syntax.yaml"></a>

```
Type: AWS::BillingConductor::PricingPlan
Properties: 
  [Description](#cfn-billingconductor-pricingplan-description): String
  [Name](#cfn-billingconductor-pricingplan-name): String
  [PricingRuleArns](#cfn-billingconductor-pricingplan-pricingrulearns): 
    - String
  [Tags](#cfn-billingconductor-pricingplan-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-billingconductor-pricingplan-properties"></a>

`Description`  <a name="cfn-billingconductor-pricingplan-description"></a>
The pricing plan description\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-billingconductor-pricingplan-name"></a>
The name of a pricing plan\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PricingRuleArns`  <a name="cfn-billingconductor-pricingplan-pricingrulearns"></a>
 The `PricingRuleArns` that are associated with the Pricing Plan\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-billingconductor-pricingplan-tags"></a>
A map that contains tag keys and tag values that are attached to a pricing plan\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-billingconductor-pricingplan-return-values"></a>

### Ref<a name="aws-resource-billingconductor-pricingplan-return-values-ref"></a>

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-billingconductor-pricingplan-return-values-fn--getatt"></a>

#### <a name="aws-resource-billingconductor-pricingplan-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the created pricing plan\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
 The time the pricing plan was created\. 

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
 The most recent time the pricing plan was modified\. 

`Size`  <a name="Size-fn::getatt"></a>
 The pricing rules count currently associated with this pricing plan list element\. 

## Examples<a name="aws-resource-billingconductor-pricingplan--examples"></a>



### Pricing plan with a pricing rule attached<a name="aws-resource-billingconductor-pricingplan--examples--Pricing_plan_with_a_pricing_rule_attached"></a>

The following example creates a pricing plan with a 10% global mark up pricing rule attached\.

#### JSON<a name="aws-resource-billingconductor-pricingplan--examples--Pricing_plan_with_a_pricing_rule_attached--json"></a>

```
{
  "Resources": {
      "TestPricingRule": {
          "Type": "AWS::BillingConductor::PricingRule",
          "Properties": {
              "Name": "TestPricingRule",
              "Description": "Test pricing rule created through CloudFormation. Mark everything by 10%.",
              "Type": "MARKUP",
              "Scope": "GLOBAL",
              "ModifierPercentage": 10
          }
      },
      "TestPricingPlan": {
          "Type": "AWS::BillingConductor::PricingPlan",
          "Properties": {
              "Name": "TestPricingPlan",
              "Description": "Test pricing plan created through CloudFormation.",
              "PricingRuleArns": [
                  {"Fn::GetAtt": ["TestPricingRule", "Arn"]}
              ]
          }
      }
  }
}
```

#### YAML<a name="aws-resource-billingconductor-pricingplan--examples--Pricing_plan_with_a_pricing_rule_attached--yaml"></a>

```
Resources:
  TestPricingRule:
      Type: 'AWS::BillingConductor::PricingRule'
      Properties:
        Name: 'TestPricingRule'
        Description: 'Test pricing rule created through CloudFormation. Mark everything by 10%.'
        Type: 'MARKUP'
        Scope: 'GLOBAL'
        ModifierPercentage: 10
  TestPricingPlan:
    Type: 'AWS::BillingConductor::PricingPlan'
    Properties:
      Name: 'TestPricingPlan'
      Description: 'Test pricing plan created through CloudFormation.'
      PricingRuleArns:
        - !GetAtt TestPricingRule.Arn
```