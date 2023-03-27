# AWS::BillingConductor::CustomLineItem BillingPeriodRange<a name="aws-properties-billingconductor-customlineitem-billingperiodrange"></a>

 The billing period range in which the custom line item request will be applied\. 

## Syntax<a name="aws-properties-billingconductor-customlineitem-billingperiodrange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-billingconductor-customlineitem-billingperiodrange-syntax.json"></a>

```
{
  "[ExclusiveEndBillingPeriod](#cfn-billingconductor-customlineitem-billingperiodrange-exclusiveendbillingperiod)" : String,
  "[InclusiveStartBillingPeriod](#cfn-billingconductor-customlineitem-billingperiodrange-inclusivestartbillingperiod)" : String
}
```

### YAML<a name="aws-properties-billingconductor-customlineitem-billingperiodrange-syntax.yaml"></a>

```
  [ExclusiveEndBillingPeriod](#cfn-billingconductor-customlineitem-billingperiodrange-exclusiveendbillingperiod): String
  [InclusiveStartBillingPeriod](#cfn-billingconductor-customlineitem-billingperiodrange-inclusivestartbillingperiod): String
```

## Properties<a name="aws-properties-billingconductor-customlineitem-billingperiodrange-properties"></a>

`ExclusiveEndBillingPeriod`  <a name="cfn-billingconductor-customlineitem-billingperiodrange-exclusiveendbillingperiod"></a>
 The exclusive end billing period that defines a billing period range where a custom line is applied\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InclusiveStartBillingPeriod`  <a name="cfn-billingconductor-customlineitem-billingperiodrange-inclusivestartbillingperiod"></a>
 The inclusive start billing period that defines a billing period range where a custom line is applied\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)