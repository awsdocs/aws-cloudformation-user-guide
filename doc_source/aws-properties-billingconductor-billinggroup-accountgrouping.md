# AWS::BillingConductor::BillingGroup AccountGrouping<a name="aws-properties-billingconductor-billinggroup-accountgrouping"></a>

 The set of accounts that will be under the billing group\. The set of accounts resemble the linked accounts in a consolidated family\. 

## Syntax<a name="aws-properties-billingconductor-billinggroup-accountgrouping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-billingconductor-billinggroup-accountgrouping-syntax.json"></a>

```
{
  "[LinkedAccountIds](#cfn-billingconductor-billinggroup-accountgrouping-linkedaccountids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-billingconductor-billinggroup-accountgrouping-syntax.yaml"></a>

```
  [LinkedAccountIds](#cfn-billingconductor-billinggroup-accountgrouping-linkedaccountids): 
    - String
```

## Properties<a name="aws-properties-billingconductor-billinggroup-accountgrouping-properties"></a>

`LinkedAccountIds`  <a name="cfn-billingconductor-billinggroup-accountgrouping-linkedaccountids"></a>
 The account IDs that make up the billing group\. Account IDs must be a part of the consolidated billing family, and not associated with another billing group\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)