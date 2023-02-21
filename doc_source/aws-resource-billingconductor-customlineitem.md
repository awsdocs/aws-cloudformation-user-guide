# AWS::BillingConductor::CustomLineItem<a name="aws-resource-billingconductor-customlineitem"></a>

 Creates a custom line item that can be used to create a one\-time or recurring, fixed or percentage\-based charge that you can apply to a single billing group\. You can apply custom line items to the current or previous billing period\. You can create either a fee or a discount custom line item\.

## Syntax<a name="aws-resource-billingconductor-customlineitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-billingconductor-customlineitem-syntax.json"></a>

```
{
  "Type" : "AWS::BillingConductor::CustomLineItem",
  "Properties" : {
      "[BillingGroupArn](#cfn-billingconductor-customlineitem-billinggrouparn)" : String,
      "[BillingPeriodRange](#cfn-billingconductor-customlineitem-billingperiodrange)" : BillingPeriodRange,
      "[CustomLineItemChargeDetails](#cfn-billingconductor-customlineitem-customlineitemchargedetails)" : CustomLineItemChargeDetails,
      "[Description](#cfn-billingconductor-customlineitem-description)" : String,
      "[Name](#cfn-billingconductor-customlineitem-name)" : String,
      "[Tags](#cfn-billingconductor-customlineitem-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-billingconductor-customlineitem-syntax.yaml"></a>

```
Type: AWS::BillingConductor::CustomLineItem
Properties: 
  [BillingGroupArn](#cfn-billingconductor-customlineitem-billinggrouparn): String
  [BillingPeriodRange](#cfn-billingconductor-customlineitem-billingperiodrange): 
    BillingPeriodRange
  [CustomLineItemChargeDetails](#cfn-billingconductor-customlineitem-customlineitemchargedetails): 
    CustomLineItemChargeDetails
  [Description](#cfn-billingconductor-customlineitem-description): String
  [Name](#cfn-billingconductor-customlineitem-name): String
  [Tags](#cfn-billingconductor-customlineitem-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-billingconductor-customlineitem-properties"></a>

`BillingGroupArn`  <a name="cfn-billingconductor-customlineitem-billinggrouparn"></a>
 The Amazon Resource Name \(ARN\) that references the billing group where the custom line item applies to\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BillingPeriodRange`  <a name="cfn-billingconductor-customlineitem-billingperiodrange"></a>
 A time range for which the custom line item is effective\.   
*Required*: No  
*Type*: [BillingPeriodRange](aws-properties-billingconductor-customlineitem-billingperiodrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomLineItemChargeDetails`  <a name="cfn-billingconductor-customlineitem-customlineitemchargedetails"></a>
 The charge details of a custom line item\. It should contain only one of `Flat` or `Percentage`\.   
*Required*: No  
*Type*: [CustomLineItemChargeDetails](aws-properties-billingconductor-customlineitem-customlineitemchargedetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-billingconductor-customlineitem-description"></a>
 The custom line item's description\. This is shown on the Bills page in association with the charge value\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-billingconductor-customlineitem-name"></a>
 The custom line item's name\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-billingconductor-customlineitem-tags"></a>
A map that contains tag keys and tag values that are attached to a custom line item\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-billingconductor-customlineitem-return-values"></a>

### Ref<a name="aws-resource-billingconductor-customlineitem-return-values-ref"></a>

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-billingconductor-customlineitem-return-values-fn--getatt"></a>

#### <a name="aws-resource-billingconductor-customlineitem-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) that references the billing group where the custom line item applies to\. 

`AssociationSize`  <a name="AssociationSize-fn::getatt"></a>
 The number of resources that are associated to the custom line item\. 

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
 The time created\. 

`CurrencyCode`  <a name="CurrencyCode-fn::getatt"></a>
 The custom line item's charge value currency\. Only one of the valid values can be used\. 

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
 The most recent time the custom line item was modified\. 

`ProductCode`  <a name="ProductCode-fn::getatt"></a>
 The product code associated with the custom line item\. 

## Examples<a name="aws-resource-billingconductor-customlineitem--examples"></a>



### Flat custom line item<a name="aws-resource-billingconductor-customlineitem--examples--Flat_custom_line_item"></a>

The following example shows a flat charge custom line item of $10 attached to a billing group\.

#### JSON<a name="aws-resource-billingconductor-customlineitem--examples--Flat_custom_line_item--json"></a>

```
{
  "Resources": {
      "TestFlatCustomLineItem": {
          "Type": "AWS::BillingConductor::CustomLineItem",
          "Properties": {
              "Name": "TestFlatCustomLineItem",
              "Description": "Test flat custom line item created through CloudFormation for a $10 charge.",
              "BillingGroupArn": {
                  "Fn::GetAtt": ["TestBillingGroup", "Arn"]
              },
              "CustomLineItemChargeDetails": {
                  "Flat": {
                      "ChargeValue": 10
                  },
                  "Type": "FEE"
              },
              "BillingPeriodRange": {
              "InclusiveStartBillingPeriod": "2022-11"
              }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-billingconductor-customlineitem--examples--Flat_custom_line_item--yaml"></a>

```
Resources:
  TestFlatCustomLineItem:
      Type: 'AWS::BillingConductor::CustomLineItem'
      Properties:
          Name: 'TestFlatCustomLineItem'
          Description: 'Test flat custom line item created through CloudFormation for a $10 charge.'
          BillingGroupArn: !GetAtt TestBillingGroup.Arn
          CustomLineItemChargeDetails:
              Flat:
                  ChargeValue: 10
              Type: 'FEE'
          BillingPeriodRange:
            InclusiveStartBillingPeriod: 2022-11
```

### Percentage custom line item<a name="aws-resource-billingconductor-customlineitem--examples--Percentage_custom_line_item"></a>

The following example shows a percentage charge custom line item that is 10% of the billing group total cost\.

#### JSON<a name="aws-resource-billingconductor-customlineitem--examples--Percentage_custom_line_item--json"></a>

```
{
  "Resources": {
      "TestPercentageCustomLineItem": {
          "Type": "AWS::BillingConductor::CustomLineItem",
          "Properties": {
              "Name": "TestPercentageCustomLineItem",
              "Description": "Test percentage custom line item created through CloudFormation for a %10 additional charge on the overall total bill of the billing group.",
              "BillingGroupArn": {
                  "Fn::GetAtt": ["TestBillingGroup", "Arn"]
              },
              "CustomLineItemChargeDetails": {
                  "Percentage": {
                      "PercentageValue": 10,
                      "ChildAssociatedResources": [
                          {"Fn::GetAtt": ["TestBillingGroup", "Arn"]}
                      ]
                  },
                  "Type": "FEE"
              }
          }
      }
  }
}
```

#### YAML<a name="aws-resource-billingconductor-customlineitem--examples--Percentage_custom_line_item--yaml"></a>

```
Resources:
        TestPercentageCustomLineItem:
        Type: 'AWS::BillingConductor::CustomLineItem'
        Properties:
        Name: 'TestPercentageCustomLineItem'
        Description: 'Test percentage custom line item created through CloudFormation for a %10 additional charge on the overall total bill of the billing group.'
        BillingGroupArn: !GetAtt TestBillingGroup.Arn
        CustomLineItemChargeDetails:
        Percentage:
        PercentageValue: 10
        ChildAssociatedResources:
        - !GetAtt TestBillingGroup.Arn
        Type: 'FEE'
```