# AWS::BillingConductor::CustomLineItem CustomLineItemFlatChargeDetails<a name="aws-properties-billingconductor-customlineitem-customlineitemflatchargedetails"></a>

 The charge details of a custom line item\. It should contain only one of `Flat` or `Percentage`\. 

## Syntax<a name="aws-properties-billingconductor-customlineitem-customlineitemflatchargedetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-billingconductor-customlineitem-customlineitemflatchargedetails-syntax.json"></a>

```
{
  "[ChargeValue](#cfn-billingconductor-customlineitem-customlineitemflatchargedetails-chargevalue)" : Double
}
```

### YAML<a name="aws-properties-billingconductor-customlineitem-customlineitemflatchargedetails-syntax.yaml"></a>

```
  [ChargeValue](#cfn-billingconductor-customlineitem-customlineitemflatchargedetails-chargevalue): Double
```

## Properties<a name="aws-properties-billingconductor-customlineitem-customlineitemflatchargedetails-properties"></a>

`ChargeValue`  <a name="cfn-billingconductor-customlineitem-customlineitemflatchargedetails-chargevalue"></a>
 The custom line item's fixed charge value in USD\.   
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)