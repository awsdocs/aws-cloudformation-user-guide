# AWS::QuickSight::Template CustomActionFilterOperation<a name="aws-properties-quicksight-template-customactionfilteroperation"></a>

The filter operation that filters data included in a visual or in an entire sheet\.

## Syntax<a name="aws-properties-quicksight-template-customactionfilteroperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-customactionfilteroperation-syntax.json"></a>

```
{
  "[SelectedFieldsConfiguration](#cfn-quicksight-template-customactionfilteroperation-selectedfieldsconfiguration)" : FilterOperationSelectedFieldsConfiguration,
  "[TargetVisualsConfiguration](#cfn-quicksight-template-customactionfilteroperation-targetvisualsconfiguration)" : FilterOperationTargetVisualsConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-customactionfilteroperation-syntax.yaml"></a>

```
  [SelectedFieldsConfiguration](#cfn-quicksight-template-customactionfilteroperation-selectedfieldsconfiguration): 
    FilterOperationSelectedFieldsConfiguration
  [TargetVisualsConfiguration](#cfn-quicksight-template-customactionfilteroperation-targetvisualsconfiguration): 
    FilterOperationTargetVisualsConfiguration
```

## Properties<a name="aws-properties-quicksight-template-customactionfilteroperation-properties"></a>

`SelectedFieldsConfiguration`  <a name="cfn-quicksight-template-customactionfilteroperation-selectedfieldsconfiguration"></a>
The configuration that chooses the fields to be filtered\.  
*Required*: Yes  
*Type*: [FilterOperationSelectedFieldsConfiguration](aws-properties-quicksight-template-filteroperationselectedfieldsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetVisualsConfiguration`  <a name="cfn-quicksight-template-customactionfilteroperation-targetvisualsconfiguration"></a>
The configuration that chooses the target visuals to be filtered\.  
*Required*: Yes  
*Type*: [FilterOperationTargetVisualsConfiguration](aws-properties-quicksight-template-filteroperationtargetvisualsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)