# AWS::InspectorV2::Filter StringFilter<a name="aws-properties-inspectorv2-filter-stringfilter"></a>

An object that describes the details of a string filter\.

## Syntax<a name="aws-properties-inspectorv2-filter-stringfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-inspectorv2-filter-stringfilter-syntax.json"></a>

```
{
  "[Comparison](#cfn-inspectorv2-filter-stringfilter-comparison)" : String,
  "[Value](#cfn-inspectorv2-filter-stringfilter-value)" : String
}
```

### YAML<a name="aws-properties-inspectorv2-filter-stringfilter-syntax.yaml"></a>

```
  [Comparison](#cfn-inspectorv2-filter-stringfilter-comparison): String
  [Value](#cfn-inspectorv2-filter-stringfilter-value): String
```

## Properties<a name="aws-properties-inspectorv2-filter-stringfilter-properties"></a>

`Comparison`  <a name="cfn-inspectorv2-filter-stringfilter-comparison"></a>
The operator to use when comparing values in the filter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-inspectorv2-filter-stringfilter-value"></a>
The value to filter on\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)