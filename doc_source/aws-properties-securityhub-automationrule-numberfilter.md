# AWS::SecurityHub::AutomationRule NumberFilter<a name="aws-properties-securityhub-automationrule-numberfilter"></a>

A number filter for querying findings\.

## Syntax<a name="aws-properties-securityhub-automationrule-numberfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-numberfilter-syntax.json"></a>

```
{
  "[Eq](#cfn-securityhub-automationrule-numberfilter-eq)" : Double,
  "[Gte](#cfn-securityhub-automationrule-numberfilter-gte)" : Double,
  "[Lte](#cfn-securityhub-automationrule-numberfilter-lte)" : Double
}
```

### YAML<a name="aws-properties-securityhub-automationrule-numberfilter-syntax.yaml"></a>

```
  [Eq](#cfn-securityhub-automationrule-numberfilter-eq): Double
  [Gte](#cfn-securityhub-automationrule-numberfilter-gte): Double
  [Lte](#cfn-securityhub-automationrule-numberfilter-lte): Double
```

## Properties<a name="aws-properties-securityhub-automationrule-numberfilter-properties"></a>

`Eq`  <a name="cfn-securityhub-automationrule-numberfilter-eq"></a>
The equal\-to condition to be applied to a single field when querying for findings\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Gte`  <a name="cfn-securityhub-automationrule-numberfilter-gte"></a>
The greater\-than\-equal condition to be applied to a single field when querying for findings\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lte`  <a name="cfn-securityhub-automationrule-numberfilter-lte"></a>
The less\-than\-equal condition to be applied to a single field when querying for findings\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)