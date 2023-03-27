# AWS::CE::AnomalySubscription ResourceTag<a name="aws-properties-ce-anomalysubscription-resourcetag"></a>

The tag structure that contains a tag key and value\. 

**Note**  
Tagging is supported only for the following Cost Explorer resource types: [https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_AnomalyMonitor.html](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_AnomalyMonitor.html), [https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_AnomalySubscription.html](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_AnomalySubscription.html), [https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_CostCategory.html](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_CostCategory.html)\.

## Syntax<a name="aws-properties-ce-anomalysubscription-resourcetag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ce-anomalysubscription-resourcetag-syntax.json"></a>

```
{
  "[Key](#cfn-ce-anomalysubscription-resourcetag-key)" : String,
  "[Value](#cfn-ce-anomalysubscription-resourcetag-value)" : String
}
```

### YAML<a name="aws-properties-ce-anomalysubscription-resourcetag-syntax.yaml"></a>

```
  [Key](#cfn-ce-anomalysubscription-resourcetag-key): String
  [Value](#cfn-ce-anomalysubscription-resourcetag-value): String
```

## Properties<a name="aws-properties-ce-anomalysubscription-resourcetag-properties"></a>

`Key`  <a name="cfn-ce-anomalysubscription-resourcetag-key"></a>
The key that's associated with the tag\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-ce-anomalysubscription-resourcetag-value"></a>
The value that's associated with the tag\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)