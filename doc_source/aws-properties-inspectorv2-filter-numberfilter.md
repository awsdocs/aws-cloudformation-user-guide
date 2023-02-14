# AWS::InspectorV2::Filter NumberFilter<a name="aws-properties-inspectorv2-filter-numberfilter"></a>

An object that describes the details of a number filter\.

## Syntax<a name="aws-properties-inspectorv2-filter-numberfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-inspectorv2-filter-numberfilter-syntax.json"></a>

```
{
  "[LowerInclusive](#cfn-inspectorv2-filter-numberfilter-lowerinclusive)" : Double,
  "[UpperInclusive](#cfn-inspectorv2-filter-numberfilter-upperinclusive)" : Double
}
```

### YAML<a name="aws-properties-inspectorv2-filter-numberfilter-syntax.yaml"></a>

```
  [LowerInclusive](#cfn-inspectorv2-filter-numberfilter-lowerinclusive): Double
  [UpperInclusive](#cfn-inspectorv2-filter-numberfilter-upperinclusive): Double
```

## Properties<a name="aws-properties-inspectorv2-filter-numberfilter-properties"></a>

`LowerInclusive`  <a name="cfn-inspectorv2-filter-numberfilter-lowerinclusive"></a>
The lowest number to be included in the filter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpperInclusive`  <a name="cfn-inspectorv2-filter-numberfilter-upperinclusive"></a>
The highest number to be included in the filter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)