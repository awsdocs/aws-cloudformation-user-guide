# AWS::BillingConductor::PricingRule Tiering<a name="aws-properties-billingconductor-pricingrule-tiering"></a>

 The set of tiering configurations for the pricing rule\. 

## Syntax<a name="aws-properties-billingconductor-pricingrule-tiering-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-billingconductor-pricingrule-tiering-syntax.json"></a>

```
{
  "[FreeTier](#cfn-billingconductor-pricingrule-tiering-freetier)" : FreeTier
}
```

### YAML<a name="aws-properties-billingconductor-pricingrule-tiering-syntax.yaml"></a>

```
  [FreeTier](#cfn-billingconductor-pricingrule-tiering-freetier): 
    FreeTier
```

## Properties<a name="aws-properties-billingconductor-pricingrule-tiering-properties"></a>

`FreeTier`  <a name="cfn-billingconductor-pricingrule-tiering-freetier"></a>
 The possible AWS Free Tier configurations\.   
*Required*: No  
*Type*: [FreeTier](aws-properties-billingconductor-pricingrule-freetier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)