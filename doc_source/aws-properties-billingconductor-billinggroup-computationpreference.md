# AWS::BillingConductor::BillingGroup ComputationPreference<a name="aws-properties-billingconductor-billinggroup-computationpreference"></a>

 The preferences and settings that will be used to compute the AWS charges for a billing group\. 

## Syntax<a name="aws-properties-billingconductor-billinggroup-computationpreference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-billingconductor-billinggroup-computationpreference-syntax.json"></a>

```
{
  "[PricingPlanArn](#cfn-billingconductor-billinggroup-computationpreference-pricingplanarn)" : String
}
```

### YAML<a name="aws-properties-billingconductor-billinggroup-computationpreference-syntax.yaml"></a>

```
  [PricingPlanArn](#cfn-billingconductor-billinggroup-computationpreference-pricingplanarn): String
```

## Properties<a name="aws-properties-billingconductor-billinggroup-computationpreference-properties"></a>

`PricingPlanArn`  <a name="cfn-billingconductor-billinggroup-computationpreference-pricingplanarn"></a>
 The Amazon Resource Name \(ARN\) of the pricing plan used to compute the AWS charges for a billing group\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)