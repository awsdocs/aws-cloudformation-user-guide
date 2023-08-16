# AWS::QuickSight::Dashboard DecimalDefaultValues<a name="aws-properties-quicksight-dashboard-decimaldefaultvalues"></a>

The default values of the `DecimalParameterDeclaration`\.

## Syntax<a name="aws-properties-quicksight-dashboard-decimaldefaultvalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-decimaldefaultvalues-syntax.json"></a>

```
{
  "[DynamicValue](#cfn-quicksight-dashboard-decimaldefaultvalues-dynamicvalue)" : DynamicDefaultValue,
  "[StaticValues](#cfn-quicksight-dashboard-decimaldefaultvalues-staticvalues)" : [ Double, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-decimaldefaultvalues-syntax.yaml"></a>

```
  [DynamicValue](#cfn-quicksight-dashboard-decimaldefaultvalues-dynamicvalue): 
    DynamicDefaultValue
  [StaticValues](#cfn-quicksight-dashboard-decimaldefaultvalues-staticvalues): 
    - Double
```

## Properties<a name="aws-properties-quicksight-dashboard-decimaldefaultvalues-properties"></a>

`DynamicValue`  <a name="cfn-quicksight-dashboard-decimaldefaultvalues-dynamicvalue"></a>
The dynamic value of the `DecimalDefaultValues`\. Different defaults are displayed according to users, groups, and values mapping\.  
*Required*: No  
*Type*: [DynamicDefaultValue](aws-properties-quicksight-dashboard-dynamicdefaultvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticValues`  <a name="cfn-quicksight-dashboard-decimaldefaultvalues-staticvalues"></a>
The static values of the `DecimalDefaultValues`\.  
*Required*: No  
*Type*: List of Double  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)