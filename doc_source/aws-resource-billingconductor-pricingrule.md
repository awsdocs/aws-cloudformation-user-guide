# AWS::BillingConductor::PricingRule<a name="aws-resource-billingconductor-pricingrule"></a>

 Creates a pricing rule which can be associated with a pricing plan, or a set of pricing plans\.

## Syntax<a name="aws-resource-billingconductor-pricingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-billingconductor-pricingrule-syntax.json"></a>

```
{
  "Type" : "AWS::BillingConductor::PricingRule",
  "Properties" : {
      "[BillingEntity](#cfn-billingconductor-pricingrule-billingentity)" : String,
      "[Description](#cfn-billingconductor-pricingrule-description)" : String,
      "[ModifierPercentage](#cfn-billingconductor-pricingrule-modifierpercentage)" : Double,
      "[Name](#cfn-billingconductor-pricingrule-name)" : String,
      "[Operation](#cfn-billingconductor-pricingrule-operation)" : String,
      "[Scope](#cfn-billingconductor-pricingrule-scope)" : String,
      "[Service](#cfn-billingconductor-pricingrule-service)" : String,
      "[Tags](#cfn-billingconductor-pricingrule-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Tiering](#cfn-billingconductor-pricingrule-tiering)" : Tiering,
      "[Type](#cfn-billingconductor-pricingrule-type)" : String,
      "[UsageType](#cfn-billingconductor-pricingrule-usagetype)" : String
    }
}
```

### YAML<a name="aws-resource-billingconductor-pricingrule-syntax.yaml"></a>

```
Type: AWS::BillingConductor::PricingRule
Properties: 
  [BillingEntity](#cfn-billingconductor-pricingrule-billingentity): String
  [Description](#cfn-billingconductor-pricingrule-description): String
  [ModifierPercentage](#cfn-billingconductor-pricingrule-modifierpercentage): Double
  [Name](#cfn-billingconductor-pricingrule-name): String
  [Operation](#cfn-billingconductor-pricingrule-operation): String
  [Scope](#cfn-billingconductor-pricingrule-scope): String
  [Service](#cfn-billingconductor-pricingrule-service): String
  [Tags](#cfn-billingconductor-pricingrule-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Tiering](#cfn-billingconductor-pricingrule-tiering): 
    Tiering
  [Type](#cfn-billingconductor-pricingrule-type): String
  [UsageType](#cfn-billingconductor-pricingrule-usagetype): String
```

## Properties<a name="aws-resource-billingconductor-pricingrule-properties"></a>

`BillingEntity`  <a name="cfn-billingconductor-pricingrule-billingentity"></a>
 The seller of services provided by AWS, their affiliates, or third\-party providers selling services via AWS Marketplace\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-billingconductor-pricingrule-description"></a>
 The pricing rule description\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModifierPercentage`  <a name="cfn-billingconductor-pricingrule-modifierpercentage"></a>
 A percentage modifier applied on the public pricing rates\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-billingconductor-pricingrule-name"></a>
 The name of a pricing rule\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operation`  <a name="cfn-billingconductor-pricingrule-operation"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Scope`  <a name="cfn-billingconductor-pricingrule-scope"></a>
 The scope of pricing rule that indicates if it is globally applicable, or if it is service\-specific\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Service`  <a name="cfn-billingconductor-pricingrule-service"></a>
 If the `Scope` attribute is `SERVICE`, this attribute indicates which service the `PricingRule` is applicable for\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-billingconductor-pricingrule-tags"></a>
A map that contains tag keys and tag values that are attached to a pricing rule\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tiering`  <a name="cfn-billingconductor-pricingrule-tiering"></a>
The set of tiering configurations for the pricing rule\.  
*Required*: No  
*Type*: [Tiering](aws-properties-billingconductor-pricingrule-tiering.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-billingconductor-pricingrule-type"></a>
 The type of pricing rule\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsageType`  <a name="cfn-billingconductor-pricingrule-usagetype"></a>
Usage Type is the unit that each service uses to measure the usage of a specific type of resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-billingconductor-pricingrule-return-values"></a>

### Ref<a name="aws-resource-billingconductor-pricingrule-return-values-ref"></a>

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-billingconductor-pricingrule-return-values-fn--getatt"></a>

#### <a name="aws-resource-billingconductor-pricingrule-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) used to uniquely identify a pricing rule\. 

`AssociatedPricingPlanCount`  <a name="AssociatedPricingPlanCount-fn::getatt"></a>
 The pricing plans count that this pricing rule is associated with\. 

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
 The time the pricing rule was created\. 

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
 The most recent time the pricing rule was modified\. 

## Examples<a name="aws-resource-billingconductor-pricingrule--examples"></a>



### Simple pricing rule<a name="aws-resource-billingconductor-pricingrule--examples--Simple_pricing_rule"></a>

The following example shows a pricing rule that applies a %10 global markup\.

#### JSON<a name="aws-resource-billingconductor-pricingrule--examples--Simple_pricing_rule--json"></a>

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
      }
    }
  }
```

#### YAML<a name="aws-resource-billingconductor-pricingrule--examples--Simple_pricing_rule--yaml"></a>

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
```

### AWS Marketplace pricing rule<a name="aws-resource-billingconductor-pricingrule--examples--_pricing_rule"></a>

The following example shows a pricing rule that targets only AWS Marketplace charges\.

#### JSON<a name="aws-resource-billingconductor-pricingrule--examples--_pricing_rule--json"></a>

```
{
  "Resources": {
      "TestPricingRule": {
          "Type": "AWS::BillingConductor::PricingRule",
          "Properties": {
              "Name": "TestPricingRule",
              "Description": "Test pricing rule created through CloudFormation. Keep all MP charges at public on demand rate. "
              "Type": "MARKUP",
              "Scope": "BILLING_ENTITY",
              "BillingEntity": "AWS Marketplace",
              "ModifierPercentage": 0
            }
        }
    }
  }
```

#### YAML<a name="aws-resource-billingconductor-pricingrule--examples--_pricing_rule--yaml"></a>

```
Resources:
  TestPricingRule:
    Type: 'AWS::BillingConductor::PricingRule'
    Properties:
        Name: 'TestPricingRule'
        Description: 'Test pricing rule created through CloudFormation. Keep all MP charges at public on demand rate.'
        Type: 'MARKUP'
        Scope: 'BILLING_ENTITY'
        BillingEntity: 'AWS Marketplace'
        ModifierPercentage: 0
```