# AWS::InspectorV2::Filter MapFilter<a name="aws-properties-inspectorv2-filter-mapfilter"></a>

An object that describes details of a map filter\.

## Syntax<a name="aws-properties-inspectorv2-filter-mapfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-inspectorv2-filter-mapfilter-syntax.json"></a>

```
{
  "[Comparison](#cfn-inspectorv2-filter-mapfilter-comparison)" : String,
  "[Key](#cfn-inspectorv2-filter-mapfilter-key)" : String,
  "[Value](#cfn-inspectorv2-filter-mapfilter-value)" : String
}
```

### YAML<a name="aws-properties-inspectorv2-filter-mapfilter-syntax.yaml"></a>

```
  [Comparison](#cfn-inspectorv2-filter-mapfilter-comparison): String
  [Key](#cfn-inspectorv2-filter-mapfilter-key): String
  [Value](#cfn-inspectorv2-filter-mapfilter-value): String
```

## Properties<a name="aws-properties-inspectorv2-filter-mapfilter-properties"></a>

`Comparison`  <a name="cfn-inspectorv2-filter-mapfilter-comparison"></a>
The operator to use when comparing values in the filter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-inspectorv2-filter-mapfilter-key"></a>
The tag key used in the filter\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-inspectorv2-filter-mapfilter-value"></a>
The tag value used in the filter\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)