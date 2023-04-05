# AWS::QuickSight::Dashboard StringDefaultValues<a name="aws-properties-quicksight-dashboard-stringdefaultvalues"></a>

The default values of the `StringParameterDeclaration`\.

## Syntax<a name="aws-properties-quicksight-dashboard-stringdefaultvalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-stringdefaultvalues-syntax.json"></a>

```
{
  "[DynamicValue](#cfn-quicksight-dashboard-stringdefaultvalues-dynamicvalue)" : DynamicDefaultValue,
  "[StaticValues](#cfn-quicksight-dashboard-stringdefaultvalues-staticvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-stringdefaultvalues-syntax.yaml"></a>

```
  [DynamicValue](#cfn-quicksight-dashboard-stringdefaultvalues-dynamicvalue): 
    DynamicDefaultValue
  [StaticValues](#cfn-quicksight-dashboard-stringdefaultvalues-staticvalues): 
    - String
```

## Properties<a name="aws-properties-quicksight-dashboard-stringdefaultvalues-properties"></a>

`DynamicValue`  <a name="cfn-quicksight-dashboard-stringdefaultvalues-dynamicvalue"></a>
The dynamic value of the `StringDefaultValues`\. Different defaults displayed according to users, groups, and values mapping\.  
*Required*: No  
*Type*: [DynamicDefaultValue](aws-properties-quicksight-dashboard-dynamicdefaultvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticValues`  <a name="cfn-quicksight-dashboard-stringdefaultvalues-staticvalues"></a>
The static values of the `DecimalDefaultValues`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)