# AWS::BillingConductor::CustomLineItem CustomLineItemPercentageChargeDetails<a name="aws-properties-billingconductor-customlineitem-customlineitempercentagechargedetails"></a>

 A representation of the charge details associated with a percentage custom line item\. 

## Syntax<a name="aws-properties-billingconductor-customlineitem-customlineitempercentagechargedetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-billingconductor-customlineitem-customlineitempercentagechargedetails-syntax.json"></a>

```
{
  "[ChildAssociatedResources](#cfn-billingconductor-customlineitem-customlineitempercentagechargedetails-childassociatedresources)" : [ String, ... ],
  "[PercentageValue](#cfn-billingconductor-customlineitem-customlineitempercentagechargedetails-percentagevalue)" : Double
}
```

### YAML<a name="aws-properties-billingconductor-customlineitem-customlineitempercentagechargedetails-syntax.yaml"></a>

```
  [ChildAssociatedResources](#cfn-billingconductor-customlineitem-customlineitempercentagechargedetails-childassociatedresources): 
    - String
  [PercentageValue](#cfn-billingconductor-customlineitem-customlineitempercentagechargedetails-percentagevalue): Double
```

## Properties<a name="aws-properties-billingconductor-customlineitem-customlineitempercentagechargedetails-properties"></a>

`ChildAssociatedResources`  <a name="cfn-billingconductor-customlineitem-customlineitempercentagechargedetails-childassociatedresources"></a>
A list of resource ARNs to associate to the percentage custom line item\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PercentageValue`  <a name="cfn-billingconductor-customlineitem-customlineitempercentagechargedetails-percentagevalue"></a>
 The custom line item's percentage value\. This will be multiplied against the combined value of its associated resources to determine its charge value\.   
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)