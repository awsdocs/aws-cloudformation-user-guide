# AWS::FMS::Policy PolicyTag<a name="aws-properties-fms-policy-policytag"></a>

A collection of key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\. 

## Syntax<a name="aws-properties-fms-policy-policytag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fms-policy-policytag-syntax.json"></a>

```
{
  "[Key](#cfn-fms-policy-policytag-key)" : String,
  "[Value](#cfn-fms-policy-policytag-value)" : String
}
```

### YAML<a name="aws-properties-fms-policy-policytag-syntax.yaml"></a>

```
  [Key](#cfn-fms-policy-policytag-key): String
  [Value](#cfn-fms-policy-policytag-value): String
```

## Properties<a name="aws-properties-fms-policy-policytag-properties"></a>

`Key`  <a name="cfn-fms-policy-policytag-key"></a>
Part of the key:value pair that defines a tag\. You can use a tag key to describe a category of information, such as "customer\." Tag keys are case\-sensitive\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-fms-policy-policytag-value"></a>
Part of the key:value pair that defines a tag\. You can use a tag value to describe a specific value within a category, such as "companyA" or "companyB\." Tag values are case\-sensitive\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)