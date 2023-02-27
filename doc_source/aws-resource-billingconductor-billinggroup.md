# AWS::BillingConductor::BillingGroup<a name="aws-resource-billingconductor-billinggroup"></a>

 Creates a billing group that resembles a consolidated billing family that AWS charges, based off of the predefined pricing plan computation\. 

## Syntax<a name="aws-resource-billingconductor-billinggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-billingconductor-billinggroup-syntax.json"></a>

```
{
  "Type" : "AWS::BillingConductor::BillingGroup",
  "Properties" : {
      "[AccountGrouping](#cfn-billingconductor-billinggroup-accountgrouping)" : AccountGrouping,
      "[ComputationPreference](#cfn-billingconductor-billinggroup-computationpreference)" : ComputationPreference,
      "[Description](#cfn-billingconductor-billinggroup-description)" : String,
      "[Name](#cfn-billingconductor-billinggroup-name)" : String,
      "[PrimaryAccountId](#cfn-billingconductor-billinggroup-primaryaccountid)" : String,
      "[Tags](#cfn-billingconductor-billinggroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-billingconductor-billinggroup-syntax.yaml"></a>

```
Type: AWS::BillingConductor::BillingGroup
Properties: 
  [AccountGrouping](#cfn-billingconductor-billinggroup-accountgrouping): 
    AccountGrouping
  [ComputationPreference](#cfn-billingconductor-billinggroup-computationpreference): 
    ComputationPreference
  [Description](#cfn-billingconductor-billinggroup-description): String
  [Name](#cfn-billingconductor-billinggroup-name): String
  [PrimaryAccountId](#cfn-billingconductor-billinggroup-primaryaccountid): String
  [Tags](#cfn-billingconductor-billinggroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-billingconductor-billinggroup-properties"></a>

`AccountGrouping`  <a name="cfn-billingconductor-billinggroup-accountgrouping"></a>
 The set of accounts that will be under the billing group\. The set of accounts resemble the linked accounts in a consolidated family\.   
*Required*: Yes  
*Type*: [AccountGrouping](aws-properties-billingconductor-billinggroup-accountgrouping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputationPreference`  <a name="cfn-billingconductor-billinggroup-computationpreference"></a>
 The preferences and settings that will be used to compute the AWS charges for a billing group\.   
*Required*: Yes  
*Type*: [ComputationPreference](aws-properties-billingconductor-billinggroup-computationpreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-billingconductor-billinggroup-description"></a>
The description of the billing group\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-billingconductor-billinggroup-name"></a>
The billing group's name\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryAccountId`  <a name="cfn-billingconductor-billinggroup-primaryaccountid"></a>
The account ID that serves as the main account in a billing group\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-billingconductor-billinggroup-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-billingconductor-billinggroup-return-values"></a>

### Ref<a name="aws-resource-billingconductor-billinggroup-return-values-ref"></a>

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-billingconductor-billinggroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-billingconductor-billinggroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the created billing group\. 

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
 The time the billing group was created\. 

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
 The most recent time the billing group was modified\. 

`Size`  <a name="Size-fn::getatt"></a>
The number of accounts in the particular billing group\. 

`Status`  <a name="Status-fn::getatt"></a>
The billing group status\. Only one of the valid values can be used\. 

`StatusReason`  <a name="StatusReason-fn::getatt"></a>
The reason why the billing group is in its current status\. 

## Examples<a name="aws-resource-billingconductor-billinggroup--examples"></a>



### Create a billing group with a pricing plan<a name="aws-resource-billingconductor-billinggroup--examples--Create_a_billing_group_with_a_pricing_plan"></a>

The following example is a billing group that takes a list of linked account IDs and the primary account as input\. This example creates a billing group with a pricing plan that has no pricing rules\.

#### JSON<a name="aws-resource-billingconductor-billinggroup--examples--Create_a_billing_group_with_a_pricing_plan--json"></a>

```
{
  "Parameters": {
      "LinkedAccountIds": {
      "Type": "ListNumber"
      },
      "PrimaryAccountId": {
          "Type": "Number"
      }
  },
  "Resources": {
      "TestBillingGroup": {
          "Type": "AWS::BillingConductor::BillingGroup",
          "Properties": {
              "Name": "TestBillingGroup",
              "Description": "Test billing group created through CloudFormation with 1 linked account. The linked account is also the primary account.",
              "PrimaryAccountId": {
                  "Ref": "PrimaryAccountId"
              },
              "AccountGrouping": {
                  "LinkedAccountIds":{
                      "Ref": "LinkedAccountIds"
                  }
              },
              "ComputationPreference": {
                  "PricingPlanArn": {
                      "Fn::GetAtt": ["TestPricingPlan", "Arn"]
                  }
              }
          }
      }
  }
}
```

#### YAML<a name="aws-resource-billingconductor-billinggroup--examples--Create_a_billing_group_with_a_pricing_plan--yaml"></a>

```
Parameters:
  LinkedAccountIds:
  Type: ListNumber
  PrimaryAccountId:
      Type: Number
Resources:
  TestBillingGroup:
      Type: 'AWS::BillingConductor::BillingGroup'
      Properties:
        Name: 'TestBillingGroup'
        Description: 'Test billing group created through CloudFormation with 1 linked account. The linked account is also the primary account.'
        PrimaryAccountId: !Ref PrimaryAccountId
        AccountGrouping:
            LinkedAccountIds: !Ref LinkedAccountIds
        ComputationPreference:
            PricingPlanArn: !GetAtt TestPricingPlan.Arn
```