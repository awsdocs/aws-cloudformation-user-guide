# AWS::QuickSight::Template TableUnaggregatedFieldWells<a name="aws-properties-quicksight-template-tableunaggregatedfieldwells"></a>

The unaggregated field well for the table\.

## Syntax<a name="aws-properties-quicksight-template-tableunaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tableunaggregatedfieldwells-syntax.json"></a>

```
{
  "[Values](#cfn-quicksight-template-tableunaggregatedfieldwells-values)" : [ UnaggregatedField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-tableunaggregatedfieldwells-syntax.yaml"></a>

```
  [Values](#cfn-quicksight-template-tableunaggregatedfieldwells-values): 
    - UnaggregatedField
```

## Properties<a name="aws-properties-quicksight-template-tableunaggregatedfieldwells-properties"></a>

`Values`  <a name="cfn-quicksight-template-tableunaggregatedfieldwells-values"></a>
The values field well for a pivot table\. Values are unaggregated for an unaggregated table\.  
*Required*: No  
*Type*: List of [UnaggregatedField](aws-properties-quicksight-template-unaggregatedfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)