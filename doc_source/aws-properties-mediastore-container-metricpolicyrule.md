# AWS::MediaStore::Container MetricPolicyRule<a name="aws-properties-mediastore-container-metricpolicyrule"></a>

A setting that enables metrics at the object level\. Each rule contains an object group and an object group name\. If the policy includes the MetricPolicyRules parameter, you must include at least one rule\. Each metric policy can include up to five rules by default\. You can also [request a quota increase](https://console.aws.amazon.com/servicequotas/home?region=us-east-1#!/services/mediastore/quotas) to allow up to 300 rules per policy\.

## Syntax<a name="aws-properties-mediastore-container-metricpolicyrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediastore-container-metricpolicyrule-syntax.json"></a>

```
{
  "[ObjectGroup](#cfn-mediastore-container-metricpolicyrule-objectgroup)" : String,
  "[ObjectGroupName](#cfn-mediastore-container-metricpolicyrule-objectgroupname)" : String
}
```

### YAML<a name="aws-properties-mediastore-container-metricpolicyrule-syntax.yaml"></a>

```
  [ObjectGroup](#cfn-mediastore-container-metricpolicyrule-objectgroup): String
  [ObjectGroupName](#cfn-mediastore-container-metricpolicyrule-objectgroupname): String
```

## Properties<a name="aws-properties-mediastore-container-metricpolicyrule-properties"></a>

`ObjectGroup`  <a name="cfn-mediastore-container-metricpolicyrule-objectgroup"></a>
A path or file name that defines which objects to include in the group\. Wildcards \(\*\) are acceptable\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `900`  
*Pattern*: `/?(?:[A-Za-z0-9_=:\.\-\~\*]+/){0,10}(?:[A-Za-z0-9_=:\.\-\~\*]+)?/?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectGroupName`  <a name="cfn-mediastore-container-metricpolicyrule-objectgroupname"></a>
A name that allows you to refer to the object group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `30`  
*Pattern*: `[a-zA-Z0-9_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)