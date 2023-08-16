# AWS::QuickSight::Analysis CustomActionFilterOperation<a name="aws-properties-quicksight-analysis-customactionfilteroperation"></a>

The filter operation that filters data included in a visual or in an entire sheet\.

## Syntax<a name="aws-properties-quicksight-analysis-customactionfilteroperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-customactionfilteroperation-syntax.json"></a>

```
{
  "[SelectedFieldsConfiguration](#cfn-quicksight-analysis-customactionfilteroperation-selectedfieldsconfiguration)" : FilterOperationSelectedFieldsConfiguration,
  "[TargetVisualsConfiguration](#cfn-quicksight-analysis-customactionfilteroperation-targetvisualsconfiguration)" : FilterOperationTargetVisualsConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-customactionfilteroperation-syntax.yaml"></a>

```
  [SelectedFieldsConfiguration](#cfn-quicksight-analysis-customactionfilteroperation-selectedfieldsconfiguration): 
    FilterOperationSelectedFieldsConfiguration
  [TargetVisualsConfiguration](#cfn-quicksight-analysis-customactionfilteroperation-targetvisualsconfiguration): 
    FilterOperationTargetVisualsConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-customactionfilteroperation-properties"></a>

`SelectedFieldsConfiguration`  <a name="cfn-quicksight-analysis-customactionfilteroperation-selectedfieldsconfiguration"></a>
The configuration that chooses the fields to be filtered\.  
*Required*: Yes  
*Type*: [FilterOperationSelectedFieldsConfiguration](aws-properties-quicksight-analysis-filteroperationselectedfieldsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetVisualsConfiguration`  <a name="cfn-quicksight-analysis-customactionfilteroperation-targetvisualsconfiguration"></a>
The configuration that chooses the target visuals to be filtered\.  
*Required*: Yes  
*Type*: [FilterOperationTargetVisualsConfiguration](aws-properties-quicksight-analysis-filteroperationtargetvisualsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)